# Kittygram

## Описание
Данный проект является интернет-площадкой для владельцев котов, где они могут выставлять своих котиков на показ включая имя, цвет, дату рождения и даже фото, а так же отмечать достижения кота.

**Инструменты и стек:** #Python #Django #Docker-compose #API #Nginx #Pillow #Djoser #Gunicorn #Python-dotenv #JSON #YAML #Postman #VSCode

## Запуск
Для запуска приложения необходим сервер, рассмотрим на примере сервера под управлением ОС Linux.

1. Подготовим виртуальное окружение в директории проекта создадим файл .env:
```bash
nano .env
```

2. Добавляем следующие переменные:
```nano
POSTGRES_DB=kittygram
POSTGRES_USER=kittygram_user
POSTGRES_PASSWORD=kittygram_password
DB_HOST=db
DB_PORT=5432
SECRET_KEY=...
DEBUG=... # True/False
ALLOWED_HOSTS=127.0.0.1,localhost
```

3. Устанавливаем к Docker утилиту Docker Compose:
```bash
sudo apt update
sudo apt-get install docker-compose-plugin 
```

4. В директорию проекта копируем файл `docker-compose.production.yml` и запускаем Docker Compose:
```bash
sudo docker-compose up
```

## Примеры запросов

Добавить питомца: POST `/cats/add`

Редактировать питомца: PUTCH `/cats/edit`

Просмотр питомца: GET `/cats/{cat_id}`

Автор:
[Александр Севостьянов](https://github.com/SevostyanovAlex/)