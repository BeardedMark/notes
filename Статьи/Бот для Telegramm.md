1. Создать бота через [BotFather](https://t.me/BotFather)
2. Сохранить ключ (`1234567890:AAHFlZGGGG_BBBT00EE08_HHPCOCCC_CLCC`)
3. Создать публичный файл обработки запросов
``` php
<?php

define('BOT_TOKEN', '1234567890:AAHFlZGGGG_BBBT00EE08_HHPCOCCC_CLCC');

$update = json_decode(file_get_contents('php://input'), true);
$chat_id = $update['message']['chat']['id'] ?? null;
$text = $update['message']['text'] ?? '';

if ($chat_id) {
	file_get_contents("https://api.telegram.org/bot".BOT_TOKEN."/sendMessage?".http_build_query([
		'chat_id' => $chat_id,
		'text' => "Ты написал: $text"
	]));
}

echo "ok";

```
4. Опубликовать файл для доступа к нему (Timeweb.hosting)
5. Применить обработчик (`https://api.telegram.org/bot<key>/setWebhook?url=<link>`)