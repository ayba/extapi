Токены
======

В любом запросе _(кроме запросов на получение токена)_ обязательным параметром является 
токен доступа.

Токены доступа бывают такие:

* `base` - базовый, многоразового использования           
* `discards` - на модуль скидочных карт, многоразового использования           
* `door_keeper` - для устройств пропуска в зал, многоразового использования
* `ordering` - на бронирование, одноразовый, аннулируется сразу по завершению операции, **некоторые операции состоят из нескольких запросов с одним и тем же
токеном**
* `sales` - на продажу, одноразовый, аннулируется сразу по завершению операции, **некоторые операции состоят из нескольких запросов с одним и тем же токеном**
* `cashiers` - на кассирские операции, многоразовый


Время действия каждого токена определяется настройками в системе. При осуществлении 
операций   бронирования/продажи   на   каждую   бронь/продажу   должен   быть   запрошен 
отдельный токен доступа. Проведение нескольких бронирований/продаж по одному токену 
**НЕВОЗМОЖНО!**


Например Вам надо сделать бронирование. Вы запрашиваете токен типа `ordering`.  
запрос `/api/v2/getToken/?type=ordering&ais={ais}`  

Получив токен осуществляется бронирование, например (все запросы с 
одним токеном):
 
* создание брони и добавление места  
```
/api/v2/orderPlaceReservation/new/?placeId={placeId}&performanceId={performanceId}&orderType={orderType}&orderPerson={person}&token={orderingToken}
```
* добавление мест  
```
/api/v2/orderPlaceReservation/add/?placeId={placeId}&token={orderingToken}
```
* подтверждение брони  
`/api/v2/orderApproved/?orderPerson=mrX&token={orderingToken}`

После этого токен в системе аннулируется.

* Далее: [Продажа](sales)
* Ранее: [Типы параметров](parameters_types)
* [Содержание](index)