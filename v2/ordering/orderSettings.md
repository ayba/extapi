Описание запросов, тип токена _Ordering_, _cashiers_
=====================================

_OrderSettings_ - информация о настройках брони
-------------
`/api/v2/orderSettings/?token={token}`

### Описание
Возвращает структуру _[OrderSettings](../replies/orderSettings)_.

Доступен как по токену бронирования, так и по кассирскому токену

### Параметры
|    Параметр    |                        Описание                        | Обязателен |   Тип  | Значение по умолчанию |
|:--------------:|:------------------------------------------------------:|:----------:|:------:|:---------------------:|
|      token     |                          токен                         |     да     | string |      отсутствует      |

### Пример запроса
`/api/v2/orderSettings/?token={token}`

### Пример ответа
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "placeLimit": "100",
    "percentLimit": "100",
    "orderTypes": [
      {
        "orderTypeId": "1",
        "orderTypeName": "Системная",
        "orderTypeTime": 0
      },
      {
        "orderTypeId": "3",
        "orderTypeName": "Бронь с сайта",
        "orderTypeTime": 30
      },
      {
        "orderTypeId": "4",
        "orderTypeName": "Обычная (30)",
        "orderTypeTime": 10
      },
      {
        "orderTypeId": "5",
        "orderTypeName": "По карте (20)",
        "orderTypeTime": 20
      },
      {
        "orderTypeId": "6",
        "orderTypeName": "Директор (0)",
        "orderTypeTime": -30
      },
      {
        "orderTypeId": "7",
        "orderTypeName": "Пригласительный билет",
        "orderTypeTime": 0
      },
      {
        "orderTypeId": "9",
        "orderTypeName": "Бронь 2",
        "orderTypeTime": 0
      }
    ],
    "globalSettings": {
      "morningTimeForOrders": "10:00:00 ",
      "morningTimeToRemoveOrders": "5"
    }
  }
}
```

* Далее: [Описание запросов, тип токена `ordering`. OrderPlaceReservation/New](orderPlaceReservationNew)
* Ранее: [Описание запросов, тип токена `sales`. SaleDiscardAdd](../sales/saleDiscardAdd)
* [Содержание](../index)