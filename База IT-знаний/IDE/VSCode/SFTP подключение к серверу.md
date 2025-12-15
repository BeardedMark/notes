1. Установить расширение [SFTP](https://marketplace.visualstudio.com/items?itemName=Natizyskunk.sftp)
2. Нажать сочетание клавиш `ctrl + shift + p`
3. Выбрать пункт `SFTP: Config`
4. Заполнить настройки подключения и сохранить файл

```json
{
    "name": "projectName",
    "host": "projectHosting.ru",
    "remotePath": "",

    "username": "username",
    "password": "123456",

    "protocol": "sftp",
    "port": 22,
    "uploadOnSave": true,
    "useTempFile": false,
    "openSsh": false
}
```