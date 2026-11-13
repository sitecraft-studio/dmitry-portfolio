# Дмитрий — веб-разработчик

Личный сайт-портфолио: премиальные сайты, лендинги, сайты-визитки, Telegram-боты, редизайн и кастомные скрипты.

## Локальный запуск

```powershell
cd C:\Users\777\Desktop\manicure_site
python -m pip install -r requirements.txt
python app.py
```

Сайт откроется на `http://127.0.0.1:5001`.

## Публикация на Render

Проект уже подготовлен для Render:

- `render.yaml` — конфигурация веб-сервиса;
- `Procfile` — команда запуска `gunicorn app:app`;
- `requirements.txt` — зависимости Python.

Порядок:

1. Залей репозиторий на GitHub.
2. Открой [render.com](https://render.com), войди через GitHub.
3. Нажми **New → Blueprint**, выбери репозиторий.
4. Render сам прочитает `render.yaml` и запустит сайт.
5. Получи публичную ссылку вида `https://dmitry-portfolio.onrender.com`.

На бесплатном тарифе Render сервис засыпает после простоя. Первый запрос после сна может занять 30–60 секунд.

## Структура

```text
app.py               Flask-приложение
templates/index.html сайт (HTML + CSS + JS)
static/img/          фото, иконки и работы
render.yaml          конфигурация Render
requirements.txt     зависимости
```
