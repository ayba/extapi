Описание запросов, тип токена _cashiers_
================================

_PlacesDiscountRemove_ - убрать скидку.
------------------------------------
`/api/v2/placesDiscountRemove/?performanceId={perf_id}&placeId={place_id}&token={token}`

### Описание
Удалить скидку с места.

### Параметры
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|   token  	|         токен         	|     да     	| string 	|      отсутствует      	|
|  performanceId 	| идентификатор сеанса |     да     	|   int  	|      отсутствует      	|
|  placeId 	| идентификатор места |     да     	|   int  	|      отсутствует      	|

### Пример запроса
`/api/v2/placesDiscountRemove/?performanceId=310&placeId=101&token={token}`

### Пример ответа
```
{
  "code": 0,
  "message": "OK",
  "data": {
    "performanceId": 310,
    "placeId": 101,
    "price": 300,
    "orderId": null,
    "discountId": null,
    "discardNumber": null,
    "discountValue": null,
    "discardValue": null,
    "bonusSale": false,
    "bonusDelta": null
  }
}
```

* [Содержание](../index)