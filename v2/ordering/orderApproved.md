Описание запросов, тип токена _Ordering_
=====================================

_OrderApproved_ - подтверждение бронирования
-------------
`/api/v2/orderApproved/?orderPerson={orderPerson}&token={token}`

### Описание
Подтверждение бронирования. В случае успеха возвращает структуру типа _[Order](../replies/order)_.

### Параметры
|    Параметр   |         Описание        | Обязателен |   Тип  | Значение по умолчанию |
|:-------------:|:-----------------------:|:----------:|:------:|:---------------------:|
|     token     |          токен          |     да     | string |      отсутствует      |
|  orderPerson  | на кого оформлена бронь |     нет    | string |      отсутствует      |

### Пример запроса
`/api/v2/orderApproved/?orderPerson=SomeBody&token={token}`

### Пример ответа
```
{“code”:0,"message":"OK","data":{"orderId":"4401","places":
[75],"performanceId":"14230","orderType":"3","orderPerson":"SomeBody","state":"active"}}
```

* Далее: [Описание запросов, тип токена `ordering`. OrderInfo](orderInfo)
* Ранее: [Описание запросов, тип токена `ordering`. OrderPlaceReservationRemove](orderPlaceReservationRemove)
* [Содержание](../index)