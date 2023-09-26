# Kittygram

Kittygram - это веб-приложение для обмена фотографиями и достижениями котиков. Позволяет пользователям создавать профили своих котиков, добавлять фотографии и отмечать достижения. Проект создан с использованием Django и Django REST framework для бэкэнда, а также React для фронтенда, и все это запускается в Docker контейнерах.

## Инструкция по запуску

### Запуск с использованием Docker

## 1. Установите [Docker](https://www.docker.com/get-started) на вашем компьютере, если у вас его еще нет.

## 2. Склонируйте репозиторий Kittygram:
   ```bash
   git clone https://github.com/PIEJIN/kittygram.git
   cd kittygram
   ```

## 3. Создайте файл `.env` в корневой папке проекта и укажите необходимые переменные окружения, такие как `SECRET_KEY`, `DEBUG`, и данные для базы данных PostgreSQL. Пример `.env` файла:

   ```
   SECRET_KEY=your_secret_key
   DEBUG=True
   POSTGRES_USER=django_user
   POSTGRES_PASSWORD=django_password
   POSTGRES_DB=django_db
   ```

## 4. Запустите Docker Compose для сборки и запуска всех контейнеров:
   ```bash
   docker-compose up -d
   ```

   Это запустит контейнеры для бэкэнда, фронтенда, базы данных PostgreSQL и веб-шлюза.

## 5. После успешного запуска, приложение будет доступно по адресу [http://localhost:9000/](http://localhost:9000/).

## 6. Чтобы остановить приложение, выполните следующую команду:
   ```bash
   docker-compose down
   ```

## Примеры запросов

Примеры API-запросов к бэкэнду:

- Получить список всех котиков:
  ```http
  GET http://localhost:9000/api/cats/
  ```

- Создать нового котика:
  ```http
  POST http://localhost:9000/api/cats/
  ```

- Загрузить фотографию котика:
  ```http
  POST http://localhost:9000/api/cats/<cat_id>/upload/
  ```

- Получить список достижений:
  ```http
  GET http://localhost:9000/api/achievements/
  ```

## Использованные технологии

- Django
- Django REST framework
- React
- Docker
- PostgreSQL

## Автор

Проект создан и поддерживается [PIEJIN (Радислав Королев)](https://github.com/PIEJIN).
```
