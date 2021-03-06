Структуры возвращаемые в запросах
=====================================

Order
-------------

Структура для описания бронирования. 

|    Параметр   |                                                               Описание                                                               |
|:-------------:|--------------------------------------------------------------------------------------------------------------------------------------|
|    orderId    | идентификатор в системе                                                                                                              |
|     places    | массив идентификаторов мест с ценами                                                                                                 |
| performanceId | идентификатор сеанса                                                                                                                 |
|     orderDatetime     	|                               Дата и время создания бронирования    |
|     created     	|                               Timestamp создания  |
|   orderType   | идентификатор типа брони                                                                                                             |
|  orderPerson  | на кого оформлена бронь                                                                                                              |
|    expired    | время, после которого изменение брони не возможно. Если отсутствует, значит изменения уже не возможны, только удаление (orderRemove) |
|     state     | состояние, возможные значения: active, finished, cancelled, unknown                                                                  |
|discardNumber  | номер скидочной карты, по которой оформлена бронь |
| owner  | информация о создателе брони **(OBJECT)** |
| owner['kinoplanId']  | ID пользователя из киноплана**(STRING)**, '' - нет знаяения |
| owner['appName']  | название приложения создавшего бронь**(STRING)**, '' - нет знаяения  |
| owner['appId']  | ID приложения создавшего бронь**(INT)**, 0 - создано не в приложении |




* Далее: [Структуры возвращаемые в запросах. OrderSettings](orderSettings)
* Ранее: [Структуры возвращаемые в запросах. SaleSettings](saleSettings)
* [Содержание](../index)