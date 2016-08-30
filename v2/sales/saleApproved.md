Описание запросов, тип токена _sales_
=====================================

_SaleApproved_ - подтверждение продажи
-------------
```
/api/v2/saleApproved/?&token={token} 
/api/v2/saleApproved/?salePerson={name}&token={token} 
/api/v2/saleApproved/?saleExternalId={Id}&token={token} 
/api/v2/saleApproved/?salePerson={name}&saleExternalId={Id}&token={token}
``` 

### Описание
В случае успеха возвращает структуру _[Sale](../replies/sale)_. 
В дальнейшем удалить эту покупку можно только через запрос [_SaleRemove_](saleRemove).
Поля _saleExternalId_  и _salePerson_ можно заполнить только в этом запросе,
они используются для поиска заказа при печати билетов в кассе.
Эти поля не являются обязательными, так как для печати билетов системе достаточно уникального параметра _saleId_.

### Параметры
|    Параметр    |                               Описание                               | Обязателен |   Тип  | Значение по умолчанию |
|:--------------:|:--------------------------------------------------------------------:|:----------:|:------:|:---------------------:|
|      token     | токен, необходимо использовать тот же, что и при резервировании мест |     да     | string |      отсутствует      |
|   salePerson   |                     строковый признак покупателя                     |     нет    | string |      отсутствует      |
| saleExternalId |        идентификатор покупки, назначаемый генератором запроса        |     нет    | string |      отсутствует      |

### Пример запроса
`/api/v2/saleApproved/?token={token}`

### Пример ответа
```
{"code":0,"message":"OK","data":{"saleId":"7","places":{"345":250,"346":
250},"salePerson":"Pokupatel","performanceId":"7025","saleExternalId":"11223344"}}
```

* Далее: [Описание запросов, тип токена `sales`. SaleInfo](saleInfo)
* Ранее: [Описание запросов, тип токена `sales`. SalePlaceReservation/remove](salePlaceReservationRemove)
* [Содержание](../index)