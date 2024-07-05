## ToDo API

Простой RESTful API для управления задачами (ToDo) с использованием Express.js и Sequelize с базой данных SQLite.

## Установка

1. Убедитесь, что у вас установлен Node.js (рекомендуем LTS версию).

2. Склонируйте репозиторий:

   ```bash
   git clone <url-вашего-репозитория>
   cd <название-папки-проекта>
3. Установите зависимости:
   ```bash
   npm install

## Настройка базы данных
Приложение использует базу данных SQLite, которая будет создана автоматически в файле sqliteData/todo.db, если её нет.

# Запуск
Запустите приложение:
1. Запустите приложение:
   ```bash
   npm start

3. API будет доступно по адресу http://localhost:3000.

# Использование API
## Получение всех задач (ToDo)
    GET /api/todos
## Получение задачи (ToDo) по id
    GET /api/todos/:id
## Создание новой задачи (ToDo)
    POST /api/todos
    Content-Type: application/json

    {
      "title": "Название задачи",
      "description": "Описание задачи",
      "isDone": false
    }
## Редактирование задачи (ToDo) по id
    PATCH /api/todos/:id
    Content-Type: application/json

    {
      "title": "Новое название задачи",
      "description": "Новое описание задачи",
      "isDone": true
    }
## Удаление задачи (ToDo) по id
    DELETE /api/todos/:id
## Удаление всех задач (ToDo)
    DELETE /api/todos
    
## Обработка ошибок
При возникновении ошибок API возвращает соответствующий HTTP статус и сообщение об ошибке в формате JSON.
