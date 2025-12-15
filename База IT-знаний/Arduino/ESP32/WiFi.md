``` c++
#include <WiFi.h>

void setupWiFi(const char* name, const char* pass, const int await = 1000) {
  // WiFi.mode(WIFI_STA);
  WiFi.begin(name, pass);
  while (WiFi.status() != WL_CONNECTED) { delay(await); }
}

void setup() {
  Serial.begin(115200);
    
  setupWiFi("M3G", "20101995");
  
  Serial.println("🟢 WiFi подключен: " + String(wifiLogin));
  Serial.println("🔵 IP устройства: " + WiFi.localIP().toString());
  Serial.println("🔵 MAC устройства: " + String(WiFi.macAddress()));
}

void loop() {}
```