Описание запросов, тип токена _cashiers_
================================

_PlacesCertAdd_ - применить сертификат к месту.
------------------------------------
`/api/v2/placesCertAdd/?performanceId={perf_id}&placeId={place_id}&cert={SER_NUM}&token={token}`

### Описание
Применение сертификата к месту.

### Параметры
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|   token  	|         токен         	|     да     	| string 	|      отсутствует      	|
|  performanceId 	| идентификатор сеанса |     да     	|   int  	|      отсутствует      	|
|  placeId 	| идентификатор места |     да     	|   int  	|      отсутствует      	|
|  cert 	| серия и номер сертификата |     да     	|   string  	|      отсутствует      	|

### Пример запроса
`/api/v2/placesCertAdd/?performanceId=945&placeId=1&cert=фф8028&token={token}`

### Пример ответа
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "performanceId": 945,
    "placeId": 1,
    "price": 0,
    "orderId": null,
    "discountId": null,
    "discardNumber": null,
    "discountValue": null,
    "discardValue": null,
    "bonusSale": false,
    "bonusDelta": null,
    "cert": "фф8028",
    "certValue": 200
  }
}
```

* [Содержание](../index)