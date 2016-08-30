Описание запросов, тип токена _Discards_
=====================================

_DiscardsInfo_ - получение информации о скидочной карте
-------------
`/api/v2/discardsInfo/?number={number}?token={token}`

### Описание
Возвращает информацию о скидочной карте и историю операций по карте в виде структуры 
_[DiscardsInfo](../replies/discardsInfo)_.

### Параметры
| Параметр |   Описание  | Обязателен |   Тип  | Значение по умолчанию |
|:--------:|:-----------:|:----------:|:------:|:---------------------:|
|   token  |    токен    |     да     | string |      отсутствует      |
|  number  | номер карты |     да     | string |      отсутствует      |

### Пример запроса
`/api/v2/discardsInfo/?number=101&token={token}`

### Пример ответа
```
{"code":0,"message":"OK","data":{"cardInfo":{"cardId":"101","cardNumber":"101",
"cardLine":"","cardholderName":"Ivan Ivanoff","cardholderBirthday":"2000-05-06","cardholderPhone":null,
"cardholderEmail":null,"cardBalance":"9200.00","cardDiscount":"0.00",
"cardScheme":"Bonuses","isActive":"1","cardIssuePlace":"Orel","cardHoster":"Cinema",
"ticketsCount":17,"ticketsSum":1600},"cardHistory":
{"1":{"balanceBeforeAfter":"0.00\/0.00","operationPlace":"Orel","discountBeforeAfter":"0.00\/0.00",
"operationDateTime":"2015-05-27 12:22:22","operationType":"activation","performance":"","ticketsCountSum":""},
"2":{"balanceBeforeAfter":"0.00\/0.00","operationPlace":"Orel","discountBeforeAfter":"0.00\/0.00",
"operationDateTime":"2015-05-27 12:23:31","operationType":"buying","performance":"Terminator (31.05.2015 11:00)",
"ticketsCountSum":"6\/0"}, 
...... 
}}}
```

* Далее: [Описание запросов, тип токена `door_keeper`. TicketCheck](../tickets/ticketCheck)
* Ранее: [Описание запросов, тип токена `discards`. DiscardsSettings](discardsSettings)
* [Содержание](../index)