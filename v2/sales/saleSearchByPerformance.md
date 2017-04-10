Описание запросов, тип токена _Sales_, _cashiers_
=====================================

_SaleSearchByPerformance_ - поиск продаж
---------------------------
`/api/v2/saleSearchByPerformance/?kinoplanId={kinoplanId}&token={token}`

### Описание
Возвращает информацию о всех найденных продажах для данного сеанса.
Массив структур типа _[Sale](../replies/sale)_.

Поиск производится по kinoplanId  сеанса.

Запрос доступен как по токену продаж, так и по кассирскому токену.

### Параметры
|    Параметр   |         Описание        | Обязателен |   Тип  | Значение по умолчанию |
|:-------------:|:-----------------------:|:----------:|:------:|:---------------------:|
|     token     |          токен          |     да     | string |      отсутствует      |
|     kinoplanId|   kinoplanId сеанса     |     да    |   string  |      отсутствует      |

### Пример запроса
`/api/v2/saleSearch/?kinoplanId=58d149b811f30d0ef3619d27&token={token}`

### Пример ответа
```json
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
        "appName": "Test Application",
        "appId": "652431340410299"
      }
    ]
  }   
```

* [Содержание](../index)