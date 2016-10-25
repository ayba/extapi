Описание запросов, тип токена _cashiers_
========================================

_TicketListReturns_ - список возвращенных билетов
-----------------------------
`/api/v2/ticketListReturns/?token={token}`

### Описание
Возвращает массив возвращенных за смену билетов.

### Параметры
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|   token  	|         токен         	|     да     	| string 	|      отсутствует      	|

### Пример запроса
`/api/v2/ticketListReturns/?token={token}`

### Пример ответа
```
{
  "code": 0,
  "message": "OK",
  "data": [
    {
      "ticketId": 550,
      "performanceId": 1186,
      "placeId": 344,
      "printTime": "2016-10-20 17:59:08",
      "ticketSeries": "ФФ",
      "ticketNumber": 8001,
      "price": 300,
      "performanceTime": "2016-10-21 03:40:00",
      "hallName": "1",
      "hallId": 2,
      "showName": "Кубо. Легенда о самурае",
      "placeRowName": "8",
      "placeName": "10",
      "returnId": 1,
      "returnType": 1,
      "returnTime": "2016-10-20 18:06:48",
      "operator": "test kassa"
    }
  ]
}
```

* [Содержание](../index)