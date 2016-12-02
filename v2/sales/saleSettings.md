Описание запросов, тип токена _sales_, _cashiers_
=====================================

_SaleSettings_ - информация о настройках продажи
-------------
`/api/v2/saleSettings/?token={token}`

### Описание
Возвращает структуру _[SaleSettings](../replies/saleSettings)_.

Запрос доступен как по токену продаж, так и по кассирскому токену.

### Параметры
|    Параметр    |                        Описание                        | Обязателен |   Тип  | Значение по умолчанию |
|:--------------:|:------------------------------------------------------:|:----------:|:------:|:---------------------:|
|      token     |                          токен                         |     да     | string |      отсутствует      |

### Пример запроса
`/api/v2/saleSettings/?token={token}`

### Пример ответа
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "applyDiscount": 0,
    "placesLimit": 0,
    "globalSettings": {
      "ticketReturnTime": "15"
    }
  }
}
```

* Далее: [Описание запросов, тип токена `ordering`. SalePlaceReservation/new](../sales/salePlaceReservationNew)
* Ранее: [Описание запросов, тип токена `base`. DiscountInfo](discountInfo)
* [Содержание](../index)