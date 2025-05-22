# Библиотека Игр

Веб-приложение для автоматизации деятельности библиотеки игр, разработанное на Django.

## Функциональность

### Для администраторов:
- Управление каталогом игр (CRUD операции)
- Просмотр статистики и отчетов
- Управление пользователями
- Отправка уведомлений пользователям

### Для пользователей:
- Просмотр каталога игр
- Оставление отзывов и комментариев
- Создание подборок игр
- Получение уведомлений

## Установка и запуск

1. Клонируйте репозиторий:
```bash
git clone <repository-url>
cd bibl_games
```

2. Создайте виртуальное окружение и активируйте его:
```bash
python -m venv venv
source venv/bin/activate  # для Linux/Mac
venv\Scripts\activate     # для Windows
```

3. Установите зависимости:
```bash
pip install -r requirements.txt
```

4. Создайте файл .env в корневой директории проекта и добавьте следующие переменные:
```
DEBUG=True
SECRET_KEY=your-secret-key
DATABASE_URL=postgresql://user:password@localhost:5432/bibl_games
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USE_TLS=True
EMAIL_HOST_USER=your-email@gmail.com
EMAIL_HOST_PASSWORD=your-email-password
```

5. Примените миграции:
```bash
python manage.py migrate
```

6. Создайте суперпользователя:
```bash
python manage.py createsuperuser
```

7. Запустите сервер разработки:
```bash
python manage.py runserver
```

## Технологии

- Python 3.8+
- Django 5.0
- PostgreSQL
- Bootstrap 5
- Django Crispy Forms
- Django Allauth
- XlsxWriter (для Excel отчетов)
- ReportLab (для PDF отчетов) 