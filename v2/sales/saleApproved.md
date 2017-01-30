Описание запросов, тип токена _sales_
=====================================

_SaleApproved_ - подтверждение продажи
-------------
```
/api/v2/saleApproved/?&token={token} 
/api/v2/saleApproved/?salePerson={name}&token={token} 
/api/v2/saleApproved/?saleExternalId={Id}&token={token} 
/api/v2/saleApproved/?salePerson={name}&saleExternalId={Id}&token={token}
``` 

### Описание
В случае успеха возвращает структуру _[Sale](../replies/sale)_. 
В дальнейшем удалить эту покупку можно только через запрос [_SaleRemove_](saleRemove).
Поля _saleExternalId_  и _salePerson_ можно заполнить только в этом запросе,
они используются для поиска заказа при печати билетов в кассе.
Эти поля не являются обязательными, так как для печати билетов системе достаточно уникального параметра _saleId_.

### Параметры
|    Параметр    |                               Описание                               | Обязателен |   Тип  | Значение по умолчанию |
|:--------------:|:--------------------------------------------------------------------:|:----------:|:------:|:---------------------:|
|      token     | токен, необходимо использовать тот же, что и при резервировании мест |     да     | string |      отсутствует      |
|   salePerson   |                     строковый признак покупателя                     |     нет    | string |      отсутствует      |
| saleExternalId |        идентификатор покупки, назначаемый генератором запроса        |     нет    | string |      отсутствует      |

### Пример запроса
`/api/v2/saleApproved/?token={token}`

### Пример ответа
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "saleId": "48582",
    "places": {
      "1": 230
    },
    "salePerson": "asd",
    "performanceId": "144162",
    "saleExternalId": "",
    "saleUniqueCode": "dd090d2a1151ba2e74703856b1eaafde",
    "isPaid": "1",
    "isPrinted": "0",
    "orderId": null,
    "tickets": [
      {
        "ticketId": "2795296",
        "placeId": "1",
        "price": "230",
        "uniqueCode": "7e726d52a0c1a0c0abad930e9eabac16",
        "useCounter": "0"
      }
    ]
  }
}
```

* Далее: [Описание запросов, тип токена `sales`. SaleInfo](saleInfo)
* Ранее: [Описание запросов, тип токена `sales`. SalePlaceReservation/remove](salePlaceReservationRemove)
* [Содержание](../index)