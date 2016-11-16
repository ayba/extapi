Описание запросов, тип токена _cashiers_
================================

_PlacesDiscountAdd_ - применить скидку к месту.
------------------------------------
`/api/v2/placesDiscountAdd/?performanceId={perf_id}&placeId={place_id}&discountId={discount_id}&token={token}`

### Описание
Применение скидки к месту.

### Параметры
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|   token  	|         токен         	|     да     	| string 	|      отсутствует      	|
|  performanceId 	| идентификатор сеанса |     да     	|   int  	|      отсутствует      	|
|  placeId 	| идентификатор места |     да     	|   int  	|      отсутствует      	|
|  discountId 	| идентификатор скидки |     да     	|   int  	|      отсутствует      	|

### Пример запроса
`/api/v2/placesDiscountAdd/?performanceId=310&placeId=101&discountId=2&token={token}`

### Пример ответа
```
{
  "code": 0,
  "message": "OK",
  "data": {
    "performanceId": 310,
    "placeId": 101,
    "price": 200,
    "orderId": null,
    "discountId": 2,
    "discardNumber": null,
    "discountValue": 100,
    "discardValue": null,
    "bonusSale": false,
    "bonusDelta": null
  }
}
```

* [Содержание](../index)