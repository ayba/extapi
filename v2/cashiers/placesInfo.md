Описание запросов, тип токена _cashiers_
================================

_PlacesInfo_ - информация о занятых кассиром местах.
------------------------------------
`/api/v2/placesInfo/?token={token}`

### Описание
Информация о занятых кассиром местах.

Возвращает массив структур _[CashierPlace](../replies/cashierPlace)_.

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
      "performanceId": 1002,
      "placeId": 366,
      "price": 180,
      "discountId": 2,
      "discardNumber": "2440042116485",
      "discountValue": 100,
      "discardValue": 20,
      "bonusSale": false,
      "bonusDelta": 9
    },
    {
      "performanceId": 1002,
      "placeId": 367,
      "price": 270,
      "discountId": null,
      "discardNumber": "2440042116485",
      "discountValue": null,
      "discardValue": 30,
      "bonusSale": false,
      "bonusDelta": 14
    }
  ]
}
```

* [Содержание](../index)