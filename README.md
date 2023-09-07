## Установка

Создать и активировать виртуальное окружение Python.


Установить зависимости из файла **requirements.txt**:
```bash
pip install -r requirements.txt
```
# Создать и заполнить **_.env_** файл в директории **_python-final-diplom_**
```
DB_HOST=localhost
DB_PORT=5432
DB_NAME=
DB_USER=
DB_PASSWORD=
EMAIL_HOST=smtp.gmail.com
EMAIL_HOST_PORT=465
EMAIL_HOST_USER=
EMAIL_HOST_PASSWORD=
EMAIL_HOST_USER=
DEFAULT_FROM_EMAIL=email
```
# Выполнить следующие команды:
* Команда для создания миграций приложения для базы данных
```bash
python manage.py makemigrations
python manage.py migrate
```
* Команда для запуска celery:
```bash
celery -A celery worker -l INFO 
```
* Команда для запуска сервера:
```bash
python manage.py runserver
```
#### Приложение будет доступно по адресу: http://127.0.0.1:8000/