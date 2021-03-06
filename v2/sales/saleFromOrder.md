Описание запросов, тип токена _sales_
=====================================

_SaleFromOrder_ - создание продажи на основании бронирования
-------------
`/api/v2/saleFromOrder/?orderId={Id}&token={token}`

### Описание
Создает продажу из **подтвержденного** бронирования. Все места из брони, переносятся в продажу.

В случае успеха возвращает структуру _[Sale](../replies/sale)_.

### Параметры
|    Параметр    |                        Описание                        | Обязателен |   Тип  | Значение по умолчанию |
|:--------------:|:------------------------------------------------------:|:----------:|:------:|:---------------------:|
|      token     |                          токен                         |     да     | string |      отсутствует      |
|     orderId     |             идентификатор брони в системе             |     да     |   int  |      отсутствует      |

### Пример запроса
`/api/v2/saleFromOrder/?orderId=50&token={token}`

### Пример ответа
```
{"code":0,"message":"OK","data":{"saleId":"71","places":{"100":150},"performanceId":"24","orderId":"50","expired":"2015-07-09 12:07:59","discardNumber":""}}
```

* Далее: [Описание запросов, тип токена `sales`. SaleDiscardAdd](saleDiscardAdd)
* Ранее: [Описание запросов, тип токена `sales`. SaleRemove](saleRemove)
* [Содержание](../index)