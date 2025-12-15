---
Method: GET
Endpoint: /offers/{offerGuid}
Authorization:
  - none
  - token
Content-Type: application/json
Responce-Type: object
---
#1С/API
## Параметры запроса

| key       | type    | default | enum | note |
| --------- | ------- | ------- | ---- | ---- |
| offerGuid | !string |         |      |      |

## Структура ответа

| key      | type   | value                         | note |
| -------- | ------ | ----------------------------- | ---- |
| offer    | object | [[Информация о номенклатуре]] |      |
| variants | array  | [[Характеристики по номенклатуре]]          |      |
| catalog  | object | [[Информация о каталоге]]     |      |
