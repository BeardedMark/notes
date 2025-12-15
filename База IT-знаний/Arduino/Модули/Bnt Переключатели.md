[# Кнопка 6*6*5мм](https://arduino54.ru/catalog/radiodetali/knopki-pereklyuchateli/knopka-6-6-5mm/)
[# Кнопка 6*6*12мм](https://arduino54.ru/catalog/radiodetali/knopki-pereklyuchateli/knopka-6-6-12mm/)
[# Кнопка красная, выключатель, тумблер 2 положения, 2 контакта](https://arduino54.ru/catalog/radiodetali/knopki-pereklyuchateli/knopka-krasnaya-vyklyuchatel-tumbler-2-polozheniya-2-kontakta/)
``` c++
const int btnPin = 0;

void setup() {
  pinMode(btnPin, INPUT_PULLUP);
}

void loop() {
  if (digitalRead(btnPin) == LOW) {
  } else {}
}
```