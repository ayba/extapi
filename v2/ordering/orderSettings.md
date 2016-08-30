Описание запросов, тип токена _Ordering_
=====================================

_OrderSettings_ - информация о настройках брони
-------------
`/api/v2/orderSettings/?token={token}`

### Описание
Возвращает структуру _[OrderSettings](../replies/orderSettings)_.

### Параметры
|    Параметр    |                        Описание                        | Обязателен |   Тип  | Значение по умолчанию |
|:--------------:|:------------------------------------------------------:|:----------:|:------:|:---------------------:|
|      token     |                          токен                         |     да     | string |      отсутствует      |

### Пример запроса
`/api/v2/orderSettings/?token={token}`

### Пример ответа
```
{“code”:0,"message":"OK","data":{"placeLimit":"3","percentLimit":"50","orderTypes":
[{"orderTypeId":"4","orderTypeName":"Сайт(30)","orderTypeTime":10},
{"orderTypeId":"5","orderTypeName":"VIP (20)","orderTypeTime":20}]}}
```

* Далее: [Описание запросов, тип токена `ordering`. OrderPlaceReservation/New](orderPlaceReservationNew)
* Ранее: [Описание запросов, тип токена `sales`. SaleDiscardAdd](../sales/saleDiscardAdd)
* [Содержание](../index)