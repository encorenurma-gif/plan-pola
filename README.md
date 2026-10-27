# Plan Pola Di Dveri — Лендинги для TikTok

Три лендинга для трафика из TikTok → WhatsApp.

## 📁 Структура

```
├── css/style.css        # Общие стили
├── img/                 # Логотип и фото дверей
├── astana-1.html        # Астана — Кабанбай батыр 5/3 (+7 700 404 40 16)
├── astana-2.html        # Астана — Мангилик Ел 50 (+7 705 430 58 60)
├── karaganda.html       # Караганда — Республики, 7 (+7 700 404 40 12)
├── netlify.toml         # Конфигурация деплоя
└── README.md            # Этот файл
```

## 🚀 Деплой на Netlify

### Вариант 1: Drag & Drop (быстрый)
1. Зайдите на [app.netlify.com](https://app.netlify.com)
2. Нажмите **"Add new site"** → **"Deploy manually"**
3. Перетащите всю папку `Tik-Tok Plan Pola` в область загрузки
4. Через 30 секунд сайт будет доступен по ссылке вида `random-name.netlify.app`

### Вариант 2: Через GitHub (с автообновлением)
1. Создайте репозиторий на GitHub и загрузите файлы
2. На Netlify: **"Add new site"** → **"Import an existing project"** → выберите репозиторий
3. Оставьте настройки по умолчанию → **"Deploy site"**

## 🔗 URL для TikTok-рекламы

После деплоя ваши ссылки будут:

| Филиал | URL |
|--------|-----|
| Астана, Кабанбай батыр | `https://ваш-сайт.netlify.app/astana-1` |
| Астана, Мангилик Ел | `https://ваш-сайт.netlify.app/astana-2` |
| Караганда | `https://ваш-сайт.netlify.app/karaganda` |

> **Совет**: На Netlify можно изменить имя сайта: **Site settings** → **Change site name**,
> например: `planpola.netlify.app`

## 🖼️ Добавление логотипа и фото

### Логотип
1. Поместите файл логотипа в папку `img/` (например `img/logo.png`)
2. В каждом HTML-файле найдите блок:
   ```html
   <div class="header__logo">
     <!-- Замените на: <img src="img/logo.png" alt="Plan Pola"> -->
     PP
   </div>
   ```
3. Замените на:
   ```html
   <div class="header__logo">
     <img src="img/logo.png" alt="Plan Pola">
   </div>
   ```

### Фото дверей
1. Поместите фото в папку `img/` (рекомендуемый размер: 800×1067px для вертикальных, 1200×675px для горизонтальных)
2. В каждом HTML-файле найдите блоки:
   ```html
   <div class="gallery__placeholder">
     <span class="gallery__placeholder-icon">🚪</span>
     <span>Фото двери</span>
   </div>
   ```
3. Замените на:
   ```html
   <img src="img/door-1.jpg" alt="Межкомнатная дверь">
   ```

## 📊 TikTok Pixel

1. Создайте Pixel в TikTok Ads Manager
2. Скопируйте Pixel ID
3. В каждом HTML-файле найдите блок `TikTok Pixel Code` в `<head>`
4. Раскомментируйте код (уберите `<!--` и `-->`)
5. Замените `ВАШ_PIXEL_ID_ЗДЕСЬ` на ваш реальный Pixel ID

## 📱 Предзаполненное сообщение WhatsApp

При клике на кнопку WhatsApp у клиента автоматически заполнится сообщение:
> «Здравствуйте! Увидел(а) рекламу в TikTok, интересуют двери»

Чтобы изменить текст, замените URL-encoded часть `?text=...` в ссылках `wa.me`.
