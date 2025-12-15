---
Method: POST
Endpoint: /basket/{offerGuid}
Authorization:
  - token
Content-Type: application/text
Responce-Type: string
---
# Добавление нового товара в корзину
## Параметры запроса

| key         | type    | default | enum | note |
| ----------- | ------- | ------- | ---- | ---- |
| userGuid    | string  |         |      |      |
| offerGuid   | string  |         |      |      |
| variantGuid | ?string |         |      |      |
| count       | int     |         |      |      |
## Структура ответа

| key      | type   | value | note |
| -------- | ------ | ----- | ---- |
| itemGuid | string |       |      |
## Коды ответов

| code | description |
| ---- | ----------- |
|      |             |
