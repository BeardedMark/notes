# Управление диодом на устройстве
``` c++
const int ledPin = 2;

void setup() {
  pinMode(ledPin, OUTPUT);
}

void loop() {  
  digitalWrite(ledPin, HIGH);
  delay(1000);
  digitalWrite(ledPin, LOW);
}
```