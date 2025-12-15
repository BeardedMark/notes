---
Method: POST
Endpoint: /orders
Authorization:
  - token
Content-Type: application/json
Responce: "[[Создать заказ]]"
---
#1С/API
## Входящие параметры

| key            | type    | default | enum             | note         |
| -------------- | ------- | ------- | ---------------- | ------------ |
| contractorGuid | string  |         |                  |              |
| deliveryType   | enum    | pickup  | pickup, delivery |              |
| addres         | string  |         |                  |              |
| commentary     | ?string |         |                  |              |
| deliveryDate   | date    |         |                  |              |
| fromTime       | time    |         |                  |              |
| toTime         | time    |         |                  |              |
| offers         | array   |         |                  |              |
| ↳ offerGuid    | string  |         |                  |              |
| ↳ variantGuid  | ?string | null    |                  |              |
| ↳ count        | int     | 1       |                  |              |
| ↳ price        | ?float  |         |                  | цена с сайта |
