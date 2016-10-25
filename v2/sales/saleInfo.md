Описание запросов, тип токена _sales_
=====================================
SaleInfo
--------

`/api/v2/saleInfo/?saleId={saleId}token={token}` 

### Описание
Получение информации о продаже. Возвращает структуру _[Sale](../replies/sale)_.
 
Если указан параметр _saleId_, то ищется продажа по идентификатору. 
**Доступны для поиска только продажи созданные в этом же приложении.**

Если saleId не указан, то выдается информация по текущей продаже по токену. 
Также в этом случае обновляется параметр токена _expired_.

### Параметры

| Параметр |             Описание            | Обязателен |   Тип  | Значение по умолчанию |
|:--------:|:-------------------------------:|:----------:|:------:|:---------------------:|
|   token  |              токен              |     да     | string |      отсутствует      |
|  saleId  | идентификатор продажи в системе |     нет    |   int  |      отсутствует      |

### Пример запроса
`/api/v2/saleInfo/?saleId=924token={token}`

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

* Далее: [Описание запросов, тип токена `sales`. SaleRemove](saleRemove)
* Ранее: [Описание запросов, тип токена `sales`. SaleApproved](saleApproved)
* [Содержание](../index)