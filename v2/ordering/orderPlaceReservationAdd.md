Описание запросов, тип токена _ordering_
=====================================

Подзапросы OrderPlaceReservation, для работы с местами в брони
------------------------------------

_Add_ - добавление места к брони
------------------------------------
 
```
/api/v2/orderPlaceReservation/add/?placeId={placeId}&token={token}
``` 

### Описание

Запрос на добавление места в текущую бронь. Возвращает структуру типа _[Order](../replies/order)_

### Параметры

|    Параметр   |         Описание        | Обязателен |   Тип  | Значение по умолчанию |
|:-------------:|:-----------------------:|:----------:|:------:|:---------------------:|
|     token     |          токен          |     да     | string |      отсутствует      |
|    placeId    |   идентификатор места   |     да     |   int  |      отсутствует      |

### Пример запроса
```
/api/v2/orderPlaceReservation/add/?placeId=11&token={token}
```

### Пример ответа
```
{"code":0,"message":"OK","data":{"orderId":"6","places":
[10,11],"performanceId":"4044","orderType":"4","orderPerson":"\u041d\u0438\u043a
\u0438\u0442\u0430 \u0417\u043e\u043d\u043e\u0432","expired":"2014-05-11 
20:41:04”}}
```

* Далее: [Описание запросов, тип токена `ordering`. OrderPlaceReservation/remove](orderPlaceReservationRemove)
* Ранее: [Описание запросов, тип токена `ordering`. OrderPlaceReservation/new](orderPlaceReservationNew)
* [Содержание](../index)