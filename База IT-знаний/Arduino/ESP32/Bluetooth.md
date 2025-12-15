# Реклама для связи между устройствами
## Отправка
``` c++ 
#include <BLEDevice.h>
#include <BLEUtils.h>
#include <BLEAdvertising.h>

BLEAdvertising *advertising;

void setup() {
  BLEDevice::init("ESP32_BEACON");
  advertising = BLEDevice::getAdvertising();
  BLEAdvertisementData advData;
  advData.setName("NAME");
  advData.setManufacturerData("MESSAGE");

  advertising->setAdvertisementData(advData);
  advertising->start(); // stop();
}

void loop() {}
```
## Сканирование
``` c++
#include <BLEDevice.h>
#include <BLEUtils.h>
#include <BLEScan.h>

BLEScan* scan;

void setupBleScaner() {
  BLEDevice::init("");
  scan = BLEDevice::getScan();
  scan->setActiveScan(true);
  scan->setAdvertisedDeviceCallbacks(new Callbacks(), true);
}

float calculateDistance(int rssi) {
  int txPower = -59
  float n = 2.0;
  
  return pow(10, ((txPower - rssi) / (10 * n)));
}

class Callbacks : public BLEAdvertisedDeviceCallbacks {
  void onResult(BLEAdvertisedDevice device) {
    if (device.getName() == "GHOST") {
      int rssi = device.getRSSI();
      float dist = pow(10, ((-59 - rssi) / (10 * 2.0)));
      String message = device.getManufacturerData().c_str();
  
      Serial.print(dist);
      Serial.println(message);
    }
  }
};

void setup() {
	setupBleScaner()
	scan->start(0, nullptr, false); // start(300, false)
}

void loop() {}
```

## Отправка
``` c++ 
#include <NimBLEDevice.h>

NimBLEAdvertising* advertising;
  
void setBleSignal(const char* name, const char* message) {
  NimBLEAdvertisementData advData;
  advData.setName(name);
  advData.setManufacturerData(message);
  advertising->setAdvertisementData(advData);
}

void setupBleSignal() {
  NimBLEDevice::init("ESP32_BEACON");
  advertising = NimBLEDevice::getAdvertising();

}

void setup() {
  setupBleSignal();
  setBleSignal("GHOST", "1");
  advertising->start();
  advertising->stop();
}

void loop() {
  // пример динамической смены данных
  static unsigned long last = 0;
  if (millis() - last > 5000) {
    last = millis();
    
    // меняем manufacturer data каждые 5 секунд
    NimBLEAdvertisementData advData;
    advData.setName("ESP32_" + String(millis()/1000));
    advData.setManufacturerData("MSG_" + String(millis()/1000));
    advertising->setAdvertisementData(advData);
  }
}
```
