# yamdb_final
# Ссылка на проект: http://158.160.36.48:5000/
![Build Status](https://github.com/Stanislav-Gutnikov/yamdb_final/workflows/tests/badge.svg)](https://github.com/Stanislav-Gutnikov/yamdb_final/actions/workflows/yamdb_workflow.yml)

# Описание:

Учебный проект. API для социальной сети YaTube. Что умеет:

Публиковать записи
Комментировать записи
Оставлять комментарии под записями
Подписываться и отписываться на определенного пользователя
Весь функционал проекта доступен только если пользователь зарегистрирован. Аутентификация реализована с помощью JWT-токена.

# Установка:

Клонируем репозиторий:

```
git clone git@github.com:Stanislav-Gutnikov/infra_sp2.git
```

Обновляем пакетный менеджер pip:

```
pip install --upgrade pip
```

Устанавливаем зависимости:

```
pip install -r requirements.txt
```

Собираем и запускаем проект:

```
docker-compose up -d --build
```

Устанавливаем миграций:

```
docker-compose exec web python manage.py migrate
```

Создаем суперпользователя (администратора):

```
docker-compose exec web python manage.py createsuperuser
```

Подключаем статику:

```
docker-compose exec web python collectstatic --no-input
```

Проект запустится, и посмотреть его можно здесь:
http://127.0.0.1:5000/

# Шаблон .env файла (создать и заполнить .env для работы с БД):
DB_ENGINE=your_engine (работае с postgresql)
DB_NAME=your_name (имя базы данных)
POSTGRES_USER=your_user (логин для подключения к базе данных)
POSTGRES_PASSWORD=your_password (пароль для подключения к БД)
DB_HOST=your_host (название контейнера)
DB_PORT=your_port (порт для подключения к БД)
