Описание запросов, тип токена _Discards_
=====================================

_DiscardsSettings_ - получение настроек модуля скидочных карт
-------------
`/api/v2/discardsSettings/?token={token}`

### Описание
Возвращает информацию о настройках модуля скидочных карт в кинотеатре 
в виде структуры _[DiscardsSettings](../replies/discardsSettings)_.

### Параметры
|    Параметр   |         Описание        | Обязателен |   Тип  | Значение по умолчанию |
|:-------------:|:-----------------------:|:----------:|:------:|:---------------------:|
|     token     |          токен          |     да     | string |      отсутствует      |

### Пример запроса
`/api/v2/discardsSettings/?token={token}`

### Пример ответа
```
{
  "code": 0,
  "message": "OK",
  "data": {
    "isBonusSale": "1",
    "discountsMode": "1",
    "discountsModeMsg": "Summarize all",
    "bonusesPartialPayment": "0",
    "bonusesPartialPaymentAndDiscounts": "0",
    "cashiersAddDiscards": "1",
    "cashiersCardBalance": "1",
    "schemes": [
      {
        "schemeId": "1",
        "schemeName": "Бонусная"
      },
      {
        "schemeId": "2",
        "schemeName": "Киноман"
      },
      {
        "schemeId": "3",
        "schemeName": "Увидеть все"
      },
      {
        "schemeId": "4",
        "schemeName": "Бонусы"
      },
      {
        "schemeId": "5",
        "schemeName": "Новая"
      }
    ],
    "hosters": [
      {
        "hosterId": "1",
        "hosterName": "Кинотеатр"
      },
      {
        "hosterId": "2",
        "hosterName": "Магазин"
      }
    ]
  }
}
```
* Далее: [Описание запросов, тип токена `discards`. DiscardsInfo](discardsInfo)
* Ранее: [Описание запросов, тип токена `ordering`. OrderDiscardAdd](../ordering/orderDiscardAdd)
* [Содержание](../index)