Описание запросов, тип токена _cashiers_
================================

_PlacesTake_ - добавить место.
------------------------------------
`/api/v2/placesTake/?token={token}`

### Описание
Добавление места к кассирскому набору.
Параметры запроса передаются закодированными в JSON в BODY запроса

### Параметры
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|   token  	|         токен         	|     да     	| string 	|      отсутствует      	|

### Пример запроса
`/api/v2/placesTake/?token={token}`

***BODY***
```
{
  "performanceId": 3,
  "places": [
    360,
    361
  ]
}
```

### Пример ответа
```json
{
  "code": 0,
  "message": "OK",
  "data": [
    {
      "performanceId": 1602,
      "placeId": 360,
      "price": 250,
      "orderId": null,
      "discountId": null,
      "discardNumber": null,
      "discountValue": null,
      "discardValue": null,
      "bonusSale": false,
      "bonusDelta": null,
      "cert": null,
      "certValue": null
    },
    {
      "performanceId": 1602,
      "placeId": 361,
      "price": 250,
      "orderId": null,
      "discountId": null,
      "discardNumber": null,
      "discountValue": null,
      "discardValue": null,
      "bonusSale": false,
      "bonusDelta": null,
      "cert": null,
      "certValue": null
    }
  ]
}
```

* [Содержание](../index)