Продажа
=======

Продажа осуществляется с обязательным токеном типа `sales`. Вся операция продажи, 
состоящая из запросов резервации мест, удаления мест, подтверждение оплаты, 
производится с использованием одного токена. Время жизни токена установлено в 
системе и по умолчанию равняется 5-ти минутам, но при любом из выше указанных 
запросов _expired time_ токена обновляется (сдвигается на время жизни).

### Пример продажи билетов ###

получили токен $token
```
#!text
/api/v2/getToken/?type=sales&ais={ais}
```
создали продажу(место сразу добавляется)
```
#!text
/api/v2/salePlaceReservation/new/?placeId={placeId}&performanceId={performanceId}&token=$token
```
добавили еще одно место
```
#!text
/api/v2/salePlaceReservation/add/?placeId={placeId}&token=$token
```
провели оплату,а после прислали нам подтверждение
```
#!text
/api/v2/saleApproved/?&token=$token 
```



* Далее: [Бронирование](ordering)
* Ранее: [Токены](tokens)
* [Содержание](index)