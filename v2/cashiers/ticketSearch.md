Описание запросов, тип токена _cashiers_
========================================

_TicketSearch_ - поиск билета
-----------------------------
`/api/v2/ticketSearch/?string={string}&token={token}`

### Описание
Возвращает информацию о билете или сертификате.
Параметр string - id билета или СерияНомер, например АА20 или АА000020.

### Параметры
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|   token  	|         токен         	|     да     	| string 	|      отсутствует      	|
|   string 	| строка для поиска билета 	|     да     	| string 	|      отсутствует      	|

### Пример запроса 
`/api/v2/ticketSearch/?string=АА15&token={token}`

### Пример ответа - обычный билет
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "ticketId": "15",
    "performanceId": "16",
    "placeId": "469",
    "printTime": "2016-08-19 10:36:24",
    "soldOnline": "0",
    "sessionId": "1",
    "returned": "0",
    "stockId": "1",
    "ticketSeries": "АА",
    "ticketNumber": "15",
    "price": "250",
    "discountId": null,
    "discardId": null,
    "saleType": "cash",
    "performanceTime": "2016-08-19 15:30:00",
    "hallName": "1",
    "showName": "Батальонъ",
    "placeRowName": "5",
    "placeName": "7",
    "operator": "Кассир . ."
  }
}
```

### Пример запроса 
`/api/v2/ticketSearch/?string=ФФ8030&token={token}`

### Пример ответа - сертификат
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "ticketCertId": "12",
    "printTime": "2016-12-01 12:43:32",
    "sessionId": "151",
    "returned": "0",
    "used": "0",
    "stockId": "10",
    "ticketSeries": "ФФ",
    "ticketNumber": "8030",
    "price": "200",
    "saleType": "cash",
    "operator": "test kassa"
  }
}
```

* [Содержание](../index)