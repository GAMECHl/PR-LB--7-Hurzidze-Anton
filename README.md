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
![5](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/5.png)
#### Рис. 5 - Файл index.ts

#### Для того, щоб сутності відображались з бази даних треба зробити наступні зміни в файлі Pages/Posts.tsx:
![6](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/6.png)
![7](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/7.png)
![8](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/8.png)
#### Рис. 6 - Файл Posts.tsx

#### А для того, щоб сутності збрегались в базі даних треба зробити зміни в файлі Pages/PostСreate.tsx:
![9](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/9.png)
#### Рис. 7 - Файл PostСreate.tsx

#### Також потрібно зробити зміни в файлі posts/index.ts для получення массивів сутностей с api:
![10](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/10.png)
![11](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/11.png)
![12](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/12.png)
![13](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/13.png)
#### Рис. 8 - Файл index.ts

#### Далі запускаємо сервер та сторінку командами npm run dev в відповідних проектах:
![14](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/14.png)
![15](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/15.png)
#### Рис. 9 - Запуск проектів

#### Перейдемо на сторінку http://192.168.3.3:5173/posts та подивимося на сторінку:
![16](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/16.png)
![17](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/17.png)
#### Рис. 10 - Сторінка с публікаціями та відповідні публікації в базі даних

#### Попробуємо додати нову публікацію і подивитися на відображення в базі даних:
![18](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/18.png)
![19](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/19.png)
#### Рис. 11 - Створення публікації та оновлена база даних

#### Далі попробуємо видалити публікацію і подивитися на відображення в базі даних:
![20](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/20.png)
![21](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/21.png)
#### Рис. 12 - Видалення публікації та оновлена база даних

#### Потім попробуємо оновити публікацію і подивитися на відображення в базі даних:
![22](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/22.png)
![23](https://github.com/GAMECHl/PR-LB--7-Hurzidze-Anton/blob/main/23.png)
#### Рис. 13 - Зміна публікації та оновлена база даних

## Висновок: У ході виконання лабораторно-практичної роботи я навчився підключати користувацький інтерфейс до реального серверного API та ознайомився з підходами до організації HTTP-запитів через Axios, зберігання токенів доступу, обробки помилок, роботи з .env-змінними. Було забезпечено повноцінну взаємодію клієнтської частини з бекендом.
