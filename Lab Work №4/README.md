# Лабораторная работа №4

## Описание API 

Для описания API я использовал спецификацию SWAGGER, посмотреть ее можно по ссылке https://app.swaggerhub.com/apis-docs/k0perX-X/core-api/v1

## Написание API

API для этого задания описано в контроллерах ActiveBlanketsController и ClientsController.

## Тестирование API 

Генератор документации по SWAGGER имеет функции тестирования API, поэтому для собственного удобства часть тестирования будет показана, через него, часть через Postman.

### Clients GET

Получаем полный список всех клиентов.

![Clients GET](docs/Clients-GET.png)

### Client DELETE 

Удаляем пользователя по id.

![Client DELETE](docs/Clients-DELETE.png)

### Clients POST

Создаём под тем же id пользователя. API даёт значит запрос DELETE выполнился успешно

![Clients POST](docs/Clients-POST.png)

### Clients PUT

Изменим только что созданному пользователю email.

![Clients PUT](docs/Clients-PUT.png)

### Clients/id GET 

Проверим, что изменение применилось.

![Clients/id GET](docs/Clients.id-GET.png)