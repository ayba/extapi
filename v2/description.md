Краткое описание
================

API работает по протоколу HTTP(S).
 
Для начала работы необходимо получить у администраторов системы AppID и SecretKey. С 
помощью которых в дальнейшем получаются токены для осуществления запросов.
Общение строится при помощи посылки GET-запросов и получения на них ответов в формате 
JSON.   Необходимые   параметры   передаются   в   строке   запроса;   в   качестве   разделителя 
используется амперсанд:

`http://{host}/api/v2/{request}/{subrequest}/?{param}={value}&{param}={value}`

**Пример запроса:**

```
http://SERVER_URL/api/v2/ﬁlms/?date=2014-01-13&token=Me7z9M4vgetY0rGgNKnr9DCumXRXKwcJvMoJeqlR0ZjXo3XMQJgXPpFAR2r6MedPhoFEQKV7XnlHt823yd2GYR6zlV3EQaJwerl3FwAftrq2N8OQnqaGOjGjsxUmxriv
```

**Пример ответа:**

```
{"code":0,"message":"OK","data":[{"id":193,"name":"Kino-1","genre":"анимационный","duration":
120,"premiere":"2014-01-13","description":"описание фильма в красках","smallPoster":"/api/
images/?id=579","bigPoster":"/api/images/?
id=578","trailer":"","3D":"yes","forChildren":"no","ageLimit":14},{"id":194,"name":"Тестовое 
кино","genre":"антиутопия","duration":110,"premiere":"2014-01-06","description":"Еще один 
дескриптион cо всякими подробностями”,”smallPoster”:"/api/images/?id=582","bigPoster":"/api/
images/?id=581","trailer":"","3D":"no","forChildren":"yes","ageLimit":5}]}
```

**Пример ответа с ошибкой:**

`{"code":403,"message":"Unknown hall ID or empty data in DB"}`

* Далее: [Типы параметров](parameters_types)
* [Содержание](index)