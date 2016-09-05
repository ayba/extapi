Описание запросов, тип токена _cashiers_
========================================

_TicketSearch_ - поиск билета
-----------------------------
`/api/v2/ticketSearch/?string={string}&token={token}`

### Описание
Возвращает информацию о билете.
Параметр string - id билета или СерияНомер, например АА20 или АА000020.

### Параметры
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|   token  	|         токен         	|     да     	| string 	|      отсутствует      	|
|   string 	| строка для поиска билета 	|     да     	| string 	|      отсутствует      	|

### Пример запроса
`/api/v2/ticketSearch/?string=15&token={token}`

### Пример ответа
```
{"code":0,"message":"OK","data":{"ticketId":"15","performanceId":"16","placeId":"469","printTime":"2016-08-19 10:36:24","soldOnline":"0","sessionId":"1","returned":"0","stockId":"1","ticketSeries":"\u0410\u0410","ticketNumber":"15","price":"250","discountId":null,"discardId":null,"saleType":"cash","performanceTime":"2016-08-19 15:30:00","hallName":"1","showName":"\u0411\u0430\u0442\u0430\u043b\u044c\u043e\u043d\u044a","placeRowName":"5","placeName":"7","operator":"\u041a\u0430\u0441\u0441\u0438\u0440 . ."}}
```

* [Содержание](../index)