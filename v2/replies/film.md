Структуры возвращаемые в запросах
=====================================

Film
-------------

Структура для описания фильма. 

|      Параметр      |                                   Описание                                  |
|:------------------:|-----------------------------------------------------------------------------|
|         id         |                           идентификатор в системе                           |
| externalId **[deprecated]** |   идентификатор фильма во внешнем источнике фильмов (параметр будет удален) |
| externalShowId |   идентификатор фильма во внешнем источнике фильмов |
| externalSource |   указание источника фильмов, варианты systemakino, kinohod, kinoplan |
|        name        |                               название фильма                               |
|      premiere      |                       дата премьеры, формат YYYY-MM-DD                      |
|      duration      |                         продолжительность в минутах                         |
|      ageLimit      |                            возрастное ограничение                           |
|        genre       |                                     жанр                                    |
|         3D         |                             фильм в 3D (yes/no)                             |
|     forChildren    |                              для детей (yes/no)                             |
|  rentCertificate   |                        номер прокатного удостоверения                       |
|     smallPoster    |  абсолютный URI для иконки или запрос к API, например /api/v2/images/?id=22 |
|      bigPoster     |  абсолютный URI для постера или запрос к API, например/api/v2/images/?id=23 |
|   fullSizePoster   |                  абсолютный URI для полноразмерного постера                 |
|       trailer      | абсолютный URI для трейлера или запрос к API, например /api/v2/files/?id=91 |
|       actors       |                                    актёры                                   |
|      ageRating     |                              возрастной рейтинг                             |
|   annotationFull   |                            полное описание фильма                           |
|   annotationShort  |                           короткое описание фильма                          |
|      attractor     |                                рекламодатель                                |
|       budget       |                                бюджет фильма                                |
|      companies     |                компании, участвовашие при создавшинии фильма                |
|      countries     |                 страны, участвовашие при создавшинии фильма                 |
|      directors     |                                  режиссеры                                  |
|   grossRevenueRus  |                                сборы в России                               |
|  grossRevenueWorld |                                 сборы в мире                                |
|       images       |                               кадры из фильма                               |
|       imdb_id      |                             идентификатор в IMDB                            |
|    language_ids    |                         идентификаторы речей фильма                         |
|    originalTitle   |                            оригинальное название                            |
| premiereDateRussia |                            дата премьеры в России                           |
|  premiereDateWorld |                             дата премьеры в мире                            |
|      producers     |                                  продюсеры                                  |
|   productionYear   |                               год производства                              |
|       rating       |                                   рейтинг                                   |

* Далее: [Структуры возвращаемые в запросах. Performance](performance)
* Ранее: [Структуры возвращаемые в запросах. Hall](hall)
* [Содержание](../index)