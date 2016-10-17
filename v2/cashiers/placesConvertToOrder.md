Описание запросов, тип токена _cashiers_
================================

_PlacesConvertToOrder_ - конвертировать набор мест в бронь.
------------------------------------
`/api/v2/placesConvertToOrder/?orderType={id}&orderPerson={person}&token={token}`

### Описание
Конвертация набора мест в бронь или несколько бронирований.

Возвращает массив структур [Order](../replies/order)

### Параметры
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|   token  	|         токен         	|     да     	| string 	|      отсутствует      	|
|  orderType 	| тип брони (идентификатор) |     да     	|   int  	|      отсутствует      	|
|  orderPerson  | на кого оформлена бронь |     нет    | string |      отсутствует      |

### Пример запроса
`/api/v2/placesConvertToOrder/?orderType=2&orderPerson=orderMan&token={token}`

### Пример ответа
```
 {
   "code": 0,
   "message": "OK",
   "data": [
     {
       "orderId": "77",
       "places": {
         "380": 300
       },
       "performanceId": "1002",
       "orderType": "2",
       "orderPerson": "orderMan",
       "state": "active"
     }
   ]
 }
```

* [Содержание](../index)