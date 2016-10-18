Описание запросов, тип токена _cashiers_
================================

_PlacesDiscardAdd_ - применить скидочную карту к набору мест.
------------------------------------
`/api/v2/placesDiscardAdd/?cardNumber={number}&useCardDiscount={0|1}&useCardBonuses={0|1}&token={token}`

### Описание
Добавление к набору мест скидочной карты и пересчет цен в наборе с учетом скидки или накоплений по карте. 
После конвертации в продажу, купленные билеты будут учтены в операциях по карте.

Возвращает массив структур _[CashierPlace](../replies/cashierPlace)_.

### Параметры
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|      token      |             токен            |     да     | string |      отсутствует      |
|    cardNumber   |     номер скидочной карты    |     да     | string |      отсутствует      |
| useCardDiscount | использовать скидку по карте |     нет    |   int  |           1           |
|  useCardBonuses |   использовать бонусы карты  |     нет    |   int  |           0           |

### Пример запроса
`api/v2/placesDiscardAdd/?cardNumber=2440042116485&useCardDiscount=0&useCardBonuses=1&token={token}`

### Пример ответа
```
{
  "code": 0,
  "message": "OK",
  "data": [
    {
      "performanceId": 1002,
      "placeId": 366,
      "price": 180,
      "discountId": 2,
      "discardNumber": "2440042116485",
      "discountValue": 100,
      "discardValue": 20,
      "bonusSale": false,
      "bonusDelta": 9
    },
    {
      "performanceId": 1002,
      "placeId": 367,
      "price": 270,
      "discountId": null,
      "discardNumber": "2440042116485",
      "discountValue": null,
      "discardValue": 30,
      "bonusSale": false,
      "bonusDelta": 14
    }
  ]
}
```

* [Содержание](../index)