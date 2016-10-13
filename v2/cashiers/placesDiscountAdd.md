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
`/api/v2/placesDiscountAdd/?performanceId=1077&placeId=400&discountId=2&token={token}`

### Пример ответа
```
 {
   "code": 0,
   "message": "OK",
   "data": {
     "performanceId": 1077,
     "placeId": 400,
     "price": 200,
     "discountId": 2
   }
 }
```

* [Содержание](../index)