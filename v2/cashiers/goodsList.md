Описание запросов, тип токена _cashiers_
================================

_GoodsList_ - список доступных товаров.
------------------------------------
`/api/v2/goodsList/?token={token}`

### Описание
Информация о доступных товарах.

### Параметры
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|   token  	|         токен         	|     да     	| string 	|      отсутствует      	|

### Пример запроса
`/api/v2/goodsList/?token={token}`

### Пример ответа
```
{
  "code": 0,
  "message": "OK",
  "data": [
    {
      "id": 1,
      "title": "3d очки простые",
      "price": "50"
    },
    {
      "id": 2,
      "title": "3d очки складные",
      "price": "100"
    },
    {
      "id": 3,
      "title": "Поп корн большой",
      "price": "200"
    },
    {
      "id": 4,
      "title": "Кола",
      "price": "100"
    }
  ]
}
```

* [Содержание](../index)