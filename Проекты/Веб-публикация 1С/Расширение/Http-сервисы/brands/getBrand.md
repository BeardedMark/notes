---
Method: GET
Endpoint: /brands/{brandGuid}
Authorization:
  - token
Content-Type: application/json
Responce-Type: object
---
#1С/API
## Параметры запроса

| key       | type   | default | enum | note |
| --------- | ------ | ------- | ---- | ---- |
| brandGuid | string |         |      |      |

## Структура ответа

| key    | type   | value                      | note |
| ------ | ------ | -------------------------- | ---- |
| brand  | object | [[Информация о бренде]]    |      |
| offers | array  | [[Номенклатура по бренду]] |      |
