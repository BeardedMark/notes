---
Method: GET
Endpoint: /baskets/{userGuid}
Authorization:
  - token
Content-Type: application/json
Responce-Type: array
tags:
  - 1С/API
---
# Получить товары корзины
## Параметры запроса

| key      | type   | default | enum | note |
| -------- | ------ | ------- | ---- | ---- |
| userGuid | string |         |      |      |

## Структура ответа

| key       | type    | value | note           |
| --------- | ------- | ----- | -------------- |
| guid      | string  |       | идентификатор  |
| offer     | object  |       | номенклатура   |
| ↳ guid    | string  |       |                |
| ↳ name    | string  |       |                |
| variant   | ?object |       | характеристика |
| ↳ guid    | string  |       |                |
| ↳ name    | string  |       |                |
| price     | float   |       | цена продажи   |
| oldPrice  | ?float  |       | старая цена    |
| postponed | boolean |       | отложенный     |
