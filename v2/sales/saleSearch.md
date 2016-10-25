Описание запросов, тип токена _Sales_
=====================================

_SaleSearch_ - поиск продаж
---------------------------
`/api/v2/saleSearch/?string={searchString}&token={token}`

### Описание
Возвращает информацию о найденных продажах.
Массив структур типа _[Sale](../replies/sale)_.

Поиск производится по номеру брони и данным указанным при бронировании.

### Параметры
|    Параметр   |         Описание        | Обязателен |   Тип  | Значение по умолчанию |
|:-------------:|:-----------------------:|:----------:|:------:|:---------------------:|
|     token     |          токен          |     да     | string |      отсутствует      |
|     string    |   строка для поиска брони   |     да    |   string  |      отсутствует      |

### Пример запроса
`/api/v2/saleSearch/?string=924&token={token}`

### Пример ответа
```
  {
    "code": 0,
    "message": "OK",
    "data": [
      {
        "saleId": "924",
        "created": "1476972100",
        "saleDatetime": "2016-10-20 17:01:40",
        "places": {
          "215": 300
        },
        "extInfo": null,
        "salePerson": "",
        "performanceId": "101",
        "saleExternalId": "",
        "isPaid": "1",
        "isPrinted": "0",
        "orderId": null,
        "tickets": [
          {
            "ticketId": "445",
            "performanceId": "101",
            "placeId": "215",
            "price": "300",
            "uniqueCode": "730ccc5fb8cd16b5bcd89f911e631ffd",
            "useCounter": "0",
            "discountId": null,
            "discardId": null
          }
        ],
        "appName": "cashier : Новый Кассир"
      }
    ]
  }   
```

* [Содержание](../index)