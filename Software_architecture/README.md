### Розробка й документація проекту

Роль архітектора не можливо отримати зі старту карьери. Потребує перш за все технічного беку.

![Screenshot_112](https://user-images.githubusercontent.com/106797604/201801137-f8e751fa-b78c-4d62-b962-bad39587debb.png)

З якими рішеями працює архітектор щодня?
- Визначення архітектурно знаяующих влстивостей програмної системи.
Типові речі з точки фукціональності:залогіненні автори, логін, пароль, почта

- Праця з нефукціональними вимогами
Питання стосовно збереження даних користувача.І відповідності.

- Постійна співпраця та комунікація з замовниками.
Фокус на рішеннях проблемах, бути проактивним.

- Документація, як визначені властивості системи та нефункційні вимоги мають бути реалізовані.
Усі речі, які зясовуються при процессах переговорів. Документуємо. Діаграми від ситуації.

-Контроль клманд розробки під час реалізації.


### Діаграмма системи

![Screenshot_113](https://user-images.githubusercontent.com/106797604/201806917-e851a7e6-7319-4862-b020-85c5852e4ff3.png)




### Комунікація з розробниками

![Screenshot_114](https://user-images.githubusercontent.com/106797604/201806926-e0c9dcae-1075-4fbe-8a2d-fc2fd9af4ce0.png)



Концепція проекту.
Набір API-сервісів. Є Вебсайт, який по API звертається до цих сервісів та отримати відповідь.
- Сам вебсайт є окремий додаток, як клієнт.Розгортаемо веб-додаток як статичний вебсайт. AWS S3 - сервіс для зберіганя файлів й для статичних вебсайтів.
Далі по API бекенд сервіс виступає AWS Lambdа. Для регістрації й управління користувачами, - AWS Cognito
Окремий AWS S3 Bucket для юзер аватарів.
База данних, Dynamo DB - для зберіганя данних користувачів.

- Слідуюча секція, - статистиці Statistic API hander

- Секція Game Engine
Декілька сервісів, які будуть реалізувати функціонал безпосередньо гри.
.WebSocketAPI + connect/disconnect/default/messege rout  + Reds Cash 
Reds Cash -для швидче доступу клыента до данних, щоб не звертатися до бази Dynamo DB

![Screenshot_113](https://user-images.githubusercontent.com/106797604/201806917-e851a7e6-7319-4862-b020-85c5852e4ff3.png)

