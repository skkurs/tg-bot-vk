# Вячеслав Курсеев — Telegram Mini App (статическая версия)

## Что внутри
- Один автономный `index.html`: HTML, CSS и JavaScript уже внутри.
- Не нужны Node.js, сервер, база данных или платный хостинг.
- Опросы и формирование текста происходят в браузере.
- Заявки не отправляются и нигде не сохраняются.
- Кнопка Telegram открывает чат с подготовленным текстом. Отправку пользователь подтверждает сам.

## Перед публикацией
Откройте `index.html` и в начале JavaScript замените:
`const CONTACT_USERNAME = "YOUR_TELEGRAM_USERNAME";`
на ваш username Telegram без `@`, например:
`const CONTACT_USERNAME = "username";`

## Публикация через GitHub Pages
1. Войдите на https://github.com/ или создайте аккаунт.
2. Нажмите **New repository**.
3. Назовите репозиторий, например `vyacheslav-kurseev`.
4. Выберите **Public**, затем **Create repository**.
5. Нажмите **Add file → Upload files**.
6. Загрузите `index.html` из этого архива в корень репозитория (не всю ZIP-папку).
7. Нажмите **Commit changes**.
8. Откройте **Settings → Pages**.
9. В блоке **Build and deployment** выберите **Deploy from a branch**.
10. В Branch выберите **main**, папку **/(root)**, нажмите **Save**.
11. Через минуту-две адрес сайта появится на странице Pages. Обычно он выглядит так:
    `https://ВАШ-ЛОГИН.github.io/vyacheslav-kurseev/`

## Подключение к Telegram
После публикации:
1. Откройте https://t.me/BotFather и создайте бота командой `/newbot`, если бота ещё нет.
2. Настройте кнопку Mini App через меню BotFather, указав HTTPS-адрес GitHub Pages.
3. Токен бота никому не отправляйте и не вставляйте в HTML. Для простой кнопки-ссылки на Mini App сервер не нужен.

Важно: GitHub Pages публикует сайт, но не создаёт Telegram-бота автоматически. Ссылка на чат и имя получателя задаются в `CONTACT_USERNAME`.
