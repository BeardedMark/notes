---
Method: GET
Endpoint: /orders/{orderGuid}
Authorization:
  - token
Content-Type: application/json
Responce-Type: object
---
#1С/API
## Входящие параметры

| key       | type   | default | enum | note |
| --------- | ------ | ------- | ---- | ---- |
| orderGuid | string |         |      |      |

## Структура ответа

| key          | type   | value                         | note |
| ------------ | ------ | ----------------------------- | ---- |
| order        | object | [[Информация о заказе]]       |      |
| manager      | object | [[Информация о менеджере]]    |      |
| organisation | object | [[Информация об организации]] |      |

