Описание запросов, тип токена _base_
====================================
DiscountInfo
------------

`/api/v2/discountInfo/?performanceId={performanceId}&token={token}`
 
### Описание
Возвращает массив структур _[Discount](../replies/discount)_ по идентификатору сеанса.

### Параметры
 
|    Параметр   |            Описание            | Обязателен |   Тип  | Значение по умолчанию |
|:-------------:|:------------------------------:|:----------:|:------:|:---------------------:|
|     token     |              токен             |     да     | string |      отсутствует      |
| performanceId | идентификатор сеанса в системе |     да     |   int  |      отсутствует      |
 
### Пример запроса
`/api/v2/discountInfo/?performanceId=8572&token={token}`

### Пример ответа

```
{
  "code": 0,
  "message": "OK",
  "data": [
    {
      "discountName": "Детскаяскидка 10%",
      "discountValue": "-10%",
      "discountId": "1"
    },
    {
      "discountName": "Детская скидка 20%",
      "discountValue": "-20%",
      "discountId": "2"
    },
    {
      "discountName": "Детская скидка 25%",
      "discountValue": "-25%",
      "discountId": "6"
    },
    {
      "discountName": "Полцены",
      "discountValue": "-50%",
      "discountId": "9"
    }
  ]
}
```

* Далее: [Описание запросов, тип токена `sales`. SaleSettings](../sales/saleSettings)
* Ранее: [Описание запросов, тип токена `base`. Places](places)
* [Содержание](../index)