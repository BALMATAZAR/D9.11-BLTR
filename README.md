# Задание D9.11

Для того, чтобы запустить локальный сервер необходимо:
1) Распакуйте проект в папку и через терминал зайдите в директорию проекта
2) Создате виртуальное окружение:
   - python -m venv django
3) Активируйте виртуальное окружение:
   - django\Scripts\activate.bat
4) Установите все необходимые пакеты:
   - pip install -r requirements.txt
5) Выпонить следующую команду:
   - python manage.py runserver

Для того, чтобы сделать деплой на heroku необходимо (при Debug=False):
1) Перейти в каталог с проектом (например):
   - cd C:\my_site
2) Если используете статические файлы, то обязательно в проекте должны быть созданы две папки: static и staticfiles
3) Выполнить следующий команды:
   - git init
   - git add .
   - git commit -m "initial commit
   - heroku login
   - heroku create
   - heroku rename -a oldname newname (переименовываем приложение, если необходимо)
   - heroku addons:create heroku-postgresql --as DATABASE
   - heroku config:set SECRET_KEY=Ваш_секретный_код
   - git push heroku master
   - heroku run python manage.py makemigrations
   - heroku run python manage.py migrate
   - heroku run python manage.py loaddata data.xml
   - heroku run python manage.py createsuperuser
4) Запускаем приложение:
   - heroku open

   По умолчанию логин и пароль для пользователя-администратора в проекте:
   - Логин: pws_admin
   - Пароль: sf_password
