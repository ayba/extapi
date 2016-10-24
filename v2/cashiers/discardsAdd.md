Описание запросов, тип токена _cashiers_
================================

_DiscardsAdd_ - генерировать отчёт.
---------------------------------------
`/api/v2/discardsAdd/?token={token}`

### Описание
Добавление скидочной карты.
Параметры для добавления передаются закодированными в JSON в BODY запроса.

Возвращает информацию о скидочной карте в виде структуры 
_[DiscardsInfo](../replies/discardsInfo)_.

### Параметры
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|   token  	|         токен         	|     да     	| string 	|      отсутствует      	|

### Параметры в BODY
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|   cardNumber  	| Номер карточки |     да     	| string 	|      отсутствует      	|
|   schemeId  	| Идентификатор скидочной схемы |     да     	| int 	|      отсутствует      	|
|   cardLine  	| Информация для сканера штрих-кодов |     нет     	| string 	|      отсутствует      	|
|   cardholderName  	| ФИО держателя карты |     нет     	| string 	|      отсутствует      	|
|   cardholderBirthday  	| ДР держателя карты, в формате YYYY-MM-DD |     нет     	| string 	|      отсутствует      	|
|   cardholderPhone  	| номер телефона держателя карты |     нет     	| string 	|      отсутствует      	|
|   cardholderEmail  	| адрес электропочты |     нет     	| string 	|      отсутствует      	|
|   cardDescription  	| описание карты |     нет     	| string 	|      отсутствует      	|
|   hosterId  	| идентификатор организации выдавшей карту |     нет     	| int 	|      отсутствует      	|

### Пример запроса
`/api/v2/discardsAdd/?token={token}`

***BODY***
```
{
  "cardNumber": "777111444123",
  "schemeId": "1",
  "cardLine": "123456789",
  "cardholderName": "Иванов Пётр Сидорович",
  "cardholderBirthday": "1900-01-05",
  "cardholderPhone": "+7911123456789",
  "cardholderEmail": "ivanov@ura.ru",
  "cardDescription": "карточка Иванова"
}
```

### Пример ответа
```
{
  "code": 0,
  "message": "OK",
  "data": {
    "cardInfo": {
      "cardNumber": "777111444123",
      "cardLine": "123456789",
      "cardholderName": "Иванов Пётр Сидорович",
      "cardholderBirthday": "1900-01-05",
      "cardholderPhone": "+7911123456789",
      "cardholderEmail": "ivanov@ura.ru",
      "cardBalance": "0.00",
      "cardDiscount": "10.00",
      "cardScheme": "Бонусная",
      "isActive": "1",
      "ticketsCount": 0,
      "ticketsSum": 0
    }
  }
}
```

* [Содержание](../index)