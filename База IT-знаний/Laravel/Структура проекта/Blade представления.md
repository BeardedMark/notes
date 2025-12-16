# Структура директории Blade шаблонов

- **layouts** – базовые слои
- **pages** – статичные страницы
- **components** – компоненты для страниц
- **partials** – мелкие куски страницы
- **???** – динамичные страницы сайта
## Базовые слои
- `app.blade.php` – главная обертка страницы (подключения, общий HTML)
- `container.blade.php` – основной шаблон содержимого
## Статичные страницы
- `main.blade.php` – главная
- `about.blade.php` – описание
- `contacts.blade.php` – контакты
## Области страницы
- `header.blade.php` – шапка
- `alerts.blade.php` – уведомления (`success`, `error`, `warning`)
- `footer.blade.php` – подвал