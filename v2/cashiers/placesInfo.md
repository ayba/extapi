Описание запросов, тип токена _cashiers_
================================

_PlacesInfo_ - информация о занятых кассиром местах.
------------------------------------
`/api/v2/placesInfo/?token={token}`

### Описание
Информация о занятых кассиром местах.

### Параметры
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|   token  	|         токен         	|     да     	| string 	|      отсутствует      	|

### Пример запроса
`/api/v2/placesInfo/?token={token}`

### Пример ответа
```
{
  "code": 0,
  "message": "OK",
  "data": [
    {
      "performanceId": 1077,
      "placeId": 400,
      "price": 300,
      "discountId": null,
      "discardId": null
    },
    {
      "performanceId": 1077,
      "placeId": 401,
      "price": 300,
      "discountId": null,
      "discardId": null
    },
    {
      "performanceId": 1078,
      "placeId": 400,
      "price": 200,
      "discountId": null,
      "discardId": null
    }
  ]
}
```

* [Содержание](../index)