Описание запросов, тип токена _cashiers_
================================

_PlacesDiscardRemove_ - убрать применение скидочной карты.
------------------------------------
`/api/v2/placesDiscardRemove/?token={token}`

### Описание
Убрать применение скидочной карты со всех мест в наборе.

### Параметры
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|   token  	|         токен         	|     да     	| string 	|      отсутствует      	|

### Пример запроса
`/api/v2/placesDiscardRemove/?token={token}`

### Пример ответа
```
{
  "code": 0,
  "message": "OK",
  "data": [
    {
      "performanceId": 1,
      "placeId": 202,
      "price": 100,
      "orderId": null,
      "discountId": 2,
      "discardNumber": null,
      "discountValue": 100,
      "discardValue": null,
      "bonusSale": false,
      "bonusDelta": null
    }
  ]
}
```

* [Содержание](../index)