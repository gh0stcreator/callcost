# Meeting Cost — Zoom App

Счётчик стоимости звонка в виде боковой панели Zoom.

---

## Деплой на Vercel (5 минут)

1. Зайди на vercel.com → New Project
2. Загрузи папку `zoom-app` (или подключи GitHub репо)
3. Deploy — получишь URL вида `https://your-app.vercel.app`
4. Скопируй этот URL — он нужен для Zoom Marketplace

---

## Регистрация в Zoom Marketplace (~15 минут)

### 1. Создать приложение
- Зайди на marketplace.zoom.us → Develop → Build App
- Выбери **General App**
- Назови: Meeting Cost

### 2. Basic Information
- Short Description: Счётчик стоимости звонка в реальном времени
- Category: Productivity

### 3. App Credentials
- Скопируй **Client ID** и **Client Secret** — они нужны для OAuth

### 4. Surface (важно!)
- Добавь Surface: **In-Meeting Apps**
- Home URL: `https://your-app.vercel.app/index.html`

### 5. Scopes (разрешения)
Добавь следующие scopes:
- `meeting:read:meeting_participants:local`
- `meeting:read:meeting_context:local`

### 6. Redirect URL для OAuth
`https://your-app.vercel.app/index.html`

### 7. Публикация
- Для личного использования: нажми **Add** (без публикации в маркетплейс)
- Для команды: Submit for Review

---

## Использование в звонке

1. Открой Zoom-звонок
2. Нажми Apps (в панели управления звонком)
3. Найди Meeting Cost → Open
4. Панель откроется справа (~360px)
5. Приложение автоматически подтянет участников звонка
6. Укажи ставки → Старт

---

## Файлы

```
zoom-app/
├── index.html   — само приложение
└── vercel.json  — настройки CORS для Zoom
```
