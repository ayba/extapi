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
`/api/v2/placesDiscountRemove/?performanceId=1077&placeId=400&token={token}`

### Пример ответа
```
 {
   "code": 0,
   "message": "OK",
   "data": {
     "performanceId": 1077,
     "placeId": 400,
     "price": 300,
   }
 }
```

* [Содержание](../index)