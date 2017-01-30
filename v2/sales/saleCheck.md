Описание запросов, тип токена _door_keeper_
=====================================

_SaleCheck_ - получение информации о продаже по ее уникальному коду
-------------
`/api/v2/saleCheck/?code={code}&hallId={hall_id1,hall_id2,...}&token={token}`

### Описание
Возвращает информацию о продаже и количество сканирований в виде структуры
_[Sale](../replies/sale)_.

### Параметры
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|   token  	|         токен         	|     да     	| string 	|      отсутствует      	|
|   code   	| уникальный код продажи 	|     да     	| string 	|      отсутствует      	|
|  hall_id 	|идентификаторы залов, разделенные запятой  	|     да     	|   string  	|      отсутствует      	|

### Пример запроса
`/api/v2/saleCheck/?code=3d30c9d900278018dd1ab6c127735755&hallId=3,2&token={token}`

### Пример ответа
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "saleId": "7926",
    "created": "1485774901",
    "saleDatetime": "2017-01-30 14:15:01",
    "places": {
      "260": 190,
      "261": 190,
      "262": 190
    },
    "extInfo": null,
    "salePerson": "",
    "performanceId": "13699",
    "saleExternalId": "",
    "saleUniqueCode": "3d30c9d900278018dd1ab6c127735755",
    "saleUseCounter": "0",
    "isPaid": "1",
    "isPrinted": "0",
    "orderId": null,
    "tickets": [
      {
        "ticketId": "19307",
        "performanceId": "13699",
        "placeId": "260",
        "price": "190",
        "uniqueCode": "cbf73a984e0cea84c2c29e1ad60e6766",
        "useCounter": "0",
        "discountId": null,
        "discardId": null,
        "certId": null
      },
      {
        "ticketId": "19308",
        "performanceId": "13699",
        "placeId": "261",
        "price": "190",
        "uniqueCode": "63bf779c83720aa5848cb55cb9197f9a",
        "useCounter": "0",
        "discountId": null,
        "discardId": null,
        "certId": null
      },
      {
        "ticketId": "19309",
        "performanceId": "13699",
        "placeId": "262",
        "price": "190",
        "uniqueCode": "12822ee48fb21fc67f1318190176148a",
        "useCounter": "0",
        "discountId": null,
        "discardId": null,
        "certId": null
      }
    ],
    "appName": "cashier : кассир точка кипения",
    "appId": "697522904211"
  }
}
```

* [Содержание](../index)