Структуры возвращаемые в запросах
=====================================

PlaceOnPerformance
-------------

Структура для описания места в зале на сеансе. 

| Параметр |                                                                           Описание                                                                           |
|:--------:|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    id    |                                                                    идентификатор в системе                                                                   |
|  hallId  |                                                                 идентификатор зала в системе                                                                 |
|     x    |                                              координата по горизонтали (начало отсчета от верхнего левого угла)                                              |
|     y    |                                               координата по вертикали (начало отсчета от верхнего левого угла)                                               |
|    row   |                                                                    номер или название ряда                                                                   |
|   place  |                                                                          номер места                                                                         |
|   type   |  тип места, используется для отрисовки диванов, возможные значения: 1. обычное кресло; 2. левая половина дивана;,3. правая половина дивана;,4. диван целиком |
|   color  |                                                                   цвет места для отрисовки                                                                   |
|   price  |                                                                        цена (в рублях)                                                                       |
|   priceZone  |  название ценового пояса, по умолчанию base                         |
|   state  |  состояние места (free, sold, inorder, occupied)                         |
| orderId | Идентификатор бронирования, если есть |
| order | Структура типа [Order](order), если доступно |
| saleId | Идентификатор продажи, если есть |
| sale | Структура типа [Sale](sale), если доступно |
| ticket | Объект с информацией о билете, если доступно |
| kinoplanId | идентификатор места в киноплане |
| kinoplanSectorId | идентификатор сектора в киноплане |
| isAllowSaleOnline | можно ли продавать онлайн билеты на это место |

### Описание объекта ticket

|     Параметр    |                                  Описание                                 |
|:---------:|-------------------------------------------------------------------------|
| id | Идентификатор билета |
| isPrinted | Статус печати билета |

* Далее: [Структуры возвращаемые в запросах. Place](place)
* Ранее: [Структуры возвращаемые в запросах. Performance](performance)
* [Содержание](../index)