Описание запросов, тип токена _cashiers_
================================

_OrderConvertToPlaces_ - создание набора мест, на основании бронирования.
------------------------------------
`/api/v2/orderConvertToPlaces/?orderId={id}&token={token}`

### Описание
Создание набора кассирских мест из бронирования. 
В дальнейшем можно добавить или удалить места из набора и обновить бронирование, или же создать продажу из набора мест.

Возвращает массив структур _[CashierPlace](../replies/cashierPlace)_.

### Параметры
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|   token  	|         токен         	|     да     	| string 	|      отсутствует      	|
|     orderId     |             идентификатор брони в системе             |     да     |   int  |      отсутствует      |

### Пример запроса
`/api/v2/orderConvertToPlaces/?orderId=78&token={token}`

### Пример ответа
```
{
  "code": 0,
  "message": "OK",
  "data": [
    {
      "performanceId": 1187,
      "placeId": 195,
      "price": 400,
      "discountId": null,
      "discardNumber": null,
      "discountValue": null,
      "discardValue": null,
      "bonusSale": false,
      "bonusDelta": null
    },
    {
      "performanceId": 1187,
      "placeId": 196,
      "price": 400,
      "discountId": null,
      "discardNumber": null,
      "discountValue": null,
      "discardValue": null,
      "bonusSale": false,
      "bonusDelta": null
    }
  ]
}
```

* [Содержание](../index)