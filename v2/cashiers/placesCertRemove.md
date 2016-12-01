Описание запросов, тип токена _cashiers_
================================

_PlacesCertRemove_ - убрать сертификат.
------------------------------------
`/api/v2/placesCertRemove/?performanceId={perf_id}&placeId={place_id}&token={token}`

### Описание
Удалить скидку с места.

### Параметры
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|   token  	|         токен         	|     да     	| string 	|      отсутствует      	|
|  performanceId 	| идентификатор сеанса |     да     	|   int  	|      отсутствует      	|
|  placeId 	| идентификатор места |     да     	|   int  	|      отсутствует      	|

### Пример запроса
`/api/v2/placesCertRemove/?performanceId=945&placeId=1&token={token}`

### Пример ответа
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "performanceId": 945,
    "placeId": 1,
    "price": 200,
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
}
```

* [Содержание](../index)