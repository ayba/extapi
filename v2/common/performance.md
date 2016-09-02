Описание запросов, тип токена _base_
====================================
Performance
-----------

`/api/v2/schedule/performance/?id={ID}&withPlaces={withPlaces}&token={token}` 

### Описание

Возвращает структуру _[Performance](../replies/performance)_ по ее идентификатору.
 
### Параметры

|  Параметр  |            Описание            | Обязателен |   Тип  | Значение по умолчанию |
|:----------:|:------------------------------:|:----------:|:------:|:---------------------:|
|    token   |              токен             |     да     | string |      отсутствует      |
|     id     | идентификатор сеанса в системе |     да     |   int  |      отсутствует      |
| withPlaces |    выводить свободные места    |     нет    |  bool  |           0           |
| filterPlaces |    фильтр мест (free, all)   | нет     | string    | free      |

### Пример запроса
`/api/v2/schedule/performance/?id=2861&withPlaces=0&token={token}`

### Пример ответа

```
{"code":0,"message":"OK","data":{"id":2861,"datetime":"2014-01-13 09:05:00","ﬁlmId":
194,"ﬁlm":"Тестовое кино”,"smallPoster":"/api/images/?id=582","3D":"no","ageLimit":
5,"hallId":1,"hall":"Первый","cinemaId":1,"cinema":"Кристалл","freePlaces":
214,"minPrice":100,"maxPrice":100}}
```

* Далее: [Описание запросов, тип токена `base`. Places](places)
* Ранее: [Описание запросов, тип токена `base`. Schedule](schedule)
* [Содержание](../index)