Описание запросов, тип токена _Discards_
========================================

_DiscardsSearch_ - поиск скидочных карт
---------------------------------------
`/api/v2/discardsSearch/?string={searchString}&token={token}`

### Описание
Возвращает информацию о найденных скидочных картах.
Массив структур типа _[DiscardsInfo](../replies/discardsInfo)_.

Поиск производится по номеру брони и данным указанным при бронировании.

### Параметры
|    Параметр   |         Описание        | Обязателен |   Тип  | Значение по умолчанию |
|:-------------:|:-----------------------:|:----------:|:------:|:---------------------:|
|     token     |          токен          |     да     | string |      отсутствует      |
|     string    |   строка для поиска брони   |     да    |   string  |      отсутствует      |

### Пример запроса
`/api/v2/discardsSearch/?string=999&token={token}`

### Пример ответа
```
  {"code":0,"message":"OK","data":[{"cardInfo":{"cardNumber":"0000000011","cardLine":"","cardholderName":"\u0418\u0432\u0430\u043d\u043e\u0432 \u0418\u0432\u0430\u043d \u0418\u0432\u0430\u043d\u043e\u0432\u0438\u0447","cardholderBirthday":"1985-04-06","cardholderPhone":"+7-999-999-99-99","cardholderEmail":"ivanov@ivanov.su","cardBalance":"100.00","cardDiscount":"10.00","cardScheme":"\u0421\u0442\u0430\u043d\u0434\u0430\u0440\u0442","isActive":"0","ticketsCount":0,"ticketsSum":0}}]}   
```

* [Содержание](../index)