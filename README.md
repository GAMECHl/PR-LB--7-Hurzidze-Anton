# PR-LB--7-Hurzidze-Anton
## Хурцидзе Антон IПЗ 3.02 Практична-Лабораторна робота № 7

## Тема: Інтеграція клієнтської частини з RESTful API
## Мета: Підключити користувацький інтерфейс до реального серверного API. Ознайомитися з підходами до організації HTTP-запитів через Axios, зберігання токенів доступу, обробки помилок, роботи з .env-змінними. Забезпечити повноцінну взаємодію клієнтської частини з бекендом.

## 1. Налаштування Back-end перед початком інтеграції

#### Першим чином склонуюємо проект якій ми робили в практичній-лабораторній роботі №4 та відкриємо .env файл та змінюємо параметр JWT_EXPIRATION з 15m на 60m:
![1](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/1.png)
#### Рис. 1 - Файл .env бекенда

#### Пiсля цього запускаємо Postman і робимо запит auth\login із колекції RESTful API Boilerplate:
![2](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/2.png)
#### Рис. 2 - Запит auth\login

#### Далі копіюємо сгенерований токен і вставляємо його в .env у проект якій ми розробили в практичній-лабораторній роботі №6 наступним чином:
![3](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/3.png)
#### Рис. 3 - Файл .env фронтенда

#### Створюємо файл index.ts в каталозі src/api:
![4](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/4.png)
#### Рис. 4 - Каталог src/api

#### Додаємо залежність Axios командою ``npm add axios`` та пишемо наступний зміст файла index.ts:
![4](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/4.png)
#### Рис. 4 - Каталог src/api
