https://arduino54.ru/catalog/displei/lcd/lcd-16x2-1602-displej-sinij-lcd-konvertor-v-iic-i2c-spi/
# Распиновка
|LCD/I2C|ESP32 DevKit|
|---|---|
|GND|GND|
|VCC|3.3V или 5V*|
|SDA|GPIO 21|
|SCL|GPIO 22|

``` c++
#include <Wire.h>
#include <LiquidCrystal_I2C.h>

LiquidCrystal_I2C lcd(0x27, 16, 2);

void setup() {
  lcd.init();
  lcd.backlight();
}

void loop() {
  lcd.setCursor(0, 0);
  lcd.print("Hello world!");
  delay(1000);
}
```
