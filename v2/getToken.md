Описание запросов без токена
============================
getToken
--------
 
`/api/v2/getToken/?type={tokenType}&ais={ais}`
 
### Описание

Возвращает токен для выполнения дальнейших запросов. [Структура token](replies/token)

### Параметры
| Параметр |        Возможные значения       |                         Описание        | Обязателен |   Тип  | Значение по умолчанию |
|:--------:|:-------------------------------:|:---------------------------------------:|:----------:|:------:|:---------------------:|
|   type   | base, ordering, sales, discards |                        тип токена       |     да     | string |          base         |
|    ais   |                                 | подпись приложения работающего с API    |     да     | string |                       |

Вычисление подписи приложения осуществляется ПО, с помощью полученных у администратора системы, с которой планируется работать, _applicationId_ и _секретному ключу_.
 
Пример вычисления AIS на языке `PHP5.3`

```
$ais = hash("sha256", hash("sha256", $appId) . hash("sha256", $appSecret))
```

**$appId** - идентификатор приложения  
**$appSecret** - секретный ключ приложения

### Пример запроса
```
/api/v2/getToken/?type=ordering&ais=d56ffdc0ab8a157f0ba66756e65888d17fe951d768202f844c608a15926cc506
```

### Пример ответа
```
{"code":
0,"message":"OK","data":"Mwkhd5Kcy0XnmMcfZmRA7ZklWpsSjYlSvXqnJ6NWa6GSgVz3xOpHm4pOezYgYmJ5vDIgGEWqQxzroRyTIuWqJlrgFWV76WUgqszCPLLNNe0TvboQy2ds9eKx5idXrg7I"}
```

* Далее: [Описание запросов, тип токена `base`. Cinemas](common/cinemas)
* Ранее: [Бронирование](ordering)
* [Содержание](index)
