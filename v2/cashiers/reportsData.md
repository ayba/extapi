Описание запросов, тип токена _cashiers_
================================

_ReportsData_ - получить данные отчёта.
---------------------------------------
`/api/v2/reportsData/token={token}`

### Описание
Возвращает массив с данными для построения отчёта.

reportId и входящие параметры для отчета передаются закодированными в JSON в BODY запроса.

### Параметры
| Параметр 	|        Описание       	| Обязателен 	|   Тип  	| Значение по умолчанию 	|
|:--------:	|:---------------------:	|:----------:	|:------:	|:---------------------:	|
|   token  	|         токен         	|     да     	| string 	|      отсутствует      	|
|   reportId    |   идентификатор отчета (в BODY)	|     да     	| int 	|      отсутствует      	|

### Доступные для кассиров отчеты
см. в [ReportsGenerate](reportsGenerate) 

### Пример запроса
`/api/v2/reportsData/?token={token}`

***BODY***
```
{"reportId": 3}
```

### Пример ответа
```json
{
  "code": 0,
  "message": "OK",
  "data": {
    "header": {
      "sessionId": "151",
      "endTime": null,
      "userId": "48",
      "cashier": "test k.",
      "session": "с 09.11.2016 10:34 по 22.12.2016 12:31",
      "cinemaName": "Die Burg",
      "cinemaId": "1"
    },
    "stocks": {
      "10_101": {
        "having": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "firstNumber": "8019",
          "lastNumber": "9000"
        },
        "sales": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "firstNumber": "8500",
          "lastNumber": 8999,
          "summ": 0
        },
        "stayed": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "firstNumber": "8502",
          "lastNumber": "9000"
        },
        "brokes": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "ticketNumber": "9000",
          "ticketLNumber": "9000",
          "ticketId": "640"
        }
      },
      "10_102": {
        "having": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "firstNumber": "8019",
          "lastNumber": "9000"
        },
        "sales": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "firstNumber": 9001,
          "lastNumber": 8999,
          "summ": 0
        },
        "stayed": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "firstNumber": "8502",
          "lastNumber": "9000"
        },
        "brokes": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "ticketNumber": "9000",
          "ticketLNumber": "9000",
          "ticketId": "641"
        }
      },
      "10_103": {
        "having": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "firstNumber": "8019",
          "lastNumber": "9000"
        },
        "sales": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "firstNumber": 9001,
          "lastNumber": 8999,
          "summ": 0
        },
        "stayed": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "firstNumber": "8502",
          "lastNumber": "9000"
        },
        "brokes": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "ticketNumber": "9000",
          "ticketLNumber": "9000",
          "ticketId": "642"
        }
      },
      "10_104": {
        "having": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "firstNumber": "8019",
          "lastNumber": "9000"
        },
        "sales": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "firstNumber": 9001,
          "lastNumber": 8999,
          "summ": 0
        },
        "stayed": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "firstNumber": "8502",
          "lastNumber": "9000"
        },
        "brokes": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "ticketNumber": "9000",
          "ticketLNumber": "9000",
          "ticketId": "643"
        }
      },
      "10_105": {
        "having": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "firstNumber": "8019",
          "lastNumber": "9000"
        },
        "sales": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "firstNumber": 9001,
          "lastNumber": 8999,
          "summ": 0
        },
        "stayed": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "firstNumber": "8502",
          "lastNumber": "9000"
        },
        "brokes": {
          "stockId": "10",
          "stockSeria": "ФФ",
          "ticketNumber": "9000",
          "ticketLNumber": "9000",
          "ticketId": "639"
        }
      }
    },
    "returns": []
  }
}
```

* [Содержание](../index)