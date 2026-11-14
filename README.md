# Дмитрий — веб-разработчик

Личный сайт-портфолио: премиальные сайты, лендинги, сайты-визитки, Telegram-боты, редизайн и кастомные скрипты.

## Живой сайт

**https://sitecraft-studio.github.io/dmitry-portfolio/**

Сайт опубликован через GitHub Pages и открывается с любого устройства. Все кнопки «Обсудить проект», «Начать проект», «Связаться со мной», стрелки услуг и отзывов ведут в MAX. Карточки работ открывают модальное окно с описанием проекта и кнопкой «Хочу такой сайт».

## Локальный запуск

```powershell
cd C:\Users\777\Desktop\manicure_site
python -m pip install -r requirements.txt
python app.py
```

Сайт откроется на `http://127.0.0.1:5001`.

## Публикация

### GitHub Pages (основной хостинг)

Сайт статический, поэтому GitHub Pages отдаёт `index.html` напрямую:

1. Репозиторий: https://github.com/sitecraft-studio/dmitry-portfolio
2. Settings → Pages → Source: **Deploy from a branch**.
3. Branch: **main**, folder: **/ (root)**.
4. После пуша в `main` Pages пересобирается автоматически.

### Render (резервный вариант)

В репозитории есть `render.yaml`, `Procfile` и `requirements.txt` для запуска Flask на Render. Однако `render.com` может быть недоступен из некоторых сетей (в частности, соединение стабильно таймаутит из текущей сети), поэтому основной площадкой выбран GitHub Pages. При необходимости Render можно подключить через VPN или из другой сети: New → Blueprint → выбрать репозиторий.

## Структура

```text
index.html           сайт (HTML + CSS + JS), его отдаёт GitHub Pages
app.py               Flask-приложение для локального запуска и Render
static/img/          фото, иконки и работы
render.yaml          конфигурация Render
Procfile             команда запуска gunicorn
requirements.txt     зависимости Python
.nojekyll            отключает обработку Jekyll на GitHub Pages
```
