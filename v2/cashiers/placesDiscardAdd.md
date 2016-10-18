Описание запросов, тип токена _cashiers_
================================

_PlacesDiscardAdd_ - применить скидочную карту к набору мест.
------------------------------------
`/api/v2/placesDiscardAdd/?cardNumber={number}&useCardDiscount={0|1}&useCardBonuses={0|1}&token={token}`

### Описание
Добавление к набору мест скидочной карты и пересчет цен в наборе с учетом скидки или накоплений по карте. 
После конвертации в продажу, купленные билеты будут учтены в операциях по карте

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
  "data": {
    "8": {
      "performanceId": 1002,
      "placeId": 311,
      "price": 0,
      "discountId": null,
      "discardId": 26,
      "discountValue": null,
      "discardValue": 150,
      "bonusSale": true,
      "bonusDelta": -150
    },
    "9": {
      "performanceId": 1002,
      "placeId": 312,
      "price": 135,
      "discountId": null,
      "discardId": 26,
      "discountValue": null,
      "discardValue": 15,
      "bonusSale": false,
      "bonusDelta": 7
    }
  }
}
```

* [Содержание](../index)