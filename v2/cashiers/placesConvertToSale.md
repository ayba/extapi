Описание запросов, тип токена _cashiers_
================================

_PlacesConvertToSale_ - конвертировать набор мест в продажу.
------------------------------------
`/api/v2/placesConvertToSale/?salePerson={person}&token={token}`

### Описание
Конвертация набора мест в продажу или несколько продаж.

Возвращает массив структур [Sale](../replies/sale)

### Параметры
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|   token  	|         токен         	|     да     	| string 	|      отсутствует      	|
|  salePerson  | на кого оформлена продажа |     нет    | string |      отсутствует      |

### Пример запроса
`/api/v2/placesConvertToSale/?salePerson=saleMan&token={token}`

### Пример ответа
```
{
  "code": 0,
  "message": "OK",
  "data": [
    {
      "saleId": "1185",
      "places": {
        "375": 300
      },
      "extInfo": null,
      "salePerson": "saleMan",
      "performanceId": "1002",
      "saleExternalId": "",
      "isPaid": "1",
      "isPrinted": "0",
      "orderId": null,
      "tickets": [
        {
          "ticketId": "493",
          "placeId": "375",
          "price": "300",
          "uniqueCode": "595afc8a51f34a918c76a14ad363145c",
          "useCounter": "0",
          "discountId": null,
          "discardId": null
        }
      ],
      "appName": "cashier : test kassa"
    }
  ]
}
```

* [Содержание](../index)