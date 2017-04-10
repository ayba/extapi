Описание запросов, тип токена _Ordering_,_Cashiers_
=====================================

_OrderSearchByPerformance_ - поиск бронирований по kinoplanId  сеанса
----------------------------------
`/api/v2/orderSearchByPerformance/?kinoplanId={searchString}&token={token}`

### Описание
Возвращает информацию о найденных бронированиях для данныого сеанса.
Массив структур типа _[Order](../replies/order)_.

Поиск производится по kinoplanId сеанса.

Работает с токеном на бронирование или кассирским.

### Параметры
|    Параметр   |         Описание        | Обязателен |   Тип  | Значение по умолчанию |
|:-------------:|:-----------------------:|:----------:|:------:|:---------------------:|
|     token     |          токен          |     да     | string |      отсутствует      |
|     string    |   id сеанса в КП   |     да    |   string  |      отсутствует      |

### Пример запроса
`/api/v2/orderSearchByPerformance/?kinoplanId=589972e411f30dcdf14c86a8&token={token}`

### Пример ответа
```json
  {
  "code": 0,
  "message": "OK",
  "data": [
    {
      "orderId": "1",
      "places": null,
      "performanceId": "17",
      "orderType": "4",
      "orderPerson": "чел",
      "state": "active"
    }
  ]
}
```

* [Содержание](../index)