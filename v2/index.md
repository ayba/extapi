Содержание
==========

* [Краткое описание](description)                                                                                                
* [Типы параметров](parameters_types)                                                                                               
* [Токены](tokens)                                                                                                                   
* [Продажа](sales)                                                                                                                
* [Бронирование](ordering)                                                                                                      
* Описание запросов без токена                                                                         
    * [getToken](getToken)
* Описание запросов, тип токена `base`                                                        
    * [Cinemas](common/cinemas)                                                                                                                                              
    * [Halls](common/halls)                                                                                                                                                   
    * [Films](common/films)                                                                                                                                                  
    * [FilmsSoon](common/filmsSoon)                                                                                                                                                  
    * [Schedule](common/schedule)                                                                                                                                          
    * [Performance](common/performance)                                                                                                                                     
    * [Places](common/places) [Deprecated]                                                                                                                                              
    * [DiscountInfo](common/discountInfo)                                                                                                                                       
* Описание запросов, тип токена `sales`
    * [SaleSettings](sales/saleSettings)   
    * Подзапросы SalePlaceReservation, для работы с местами в продаже                                    
        * [_New_](sales/salePlaceReservationNew)                                                                                               
        * [_Add_](sales/salePlaceReservationAdd)                                                                                                  
        * [_Remove_](sales/salePlaceReservationRemove)
    * [SaleApproved](sales/saleApproved)
    * [SaleInfo](sales/saleInfo)
    * [SaleRemove](sales/saleRemove)
    * [SaleFromOrder](sales/saleFromOrder)
    * [SaleDiscardAdd](sales/saleDiscardAdd)
* Описание запросов, тип токена `ordering`                                                  
    * [OrderSettings](ordering/orderSettings)                                                                                                                         
    * Подзапросы OrderPlaceReservation, для работы с местами в брони                                       
        * [_New_](ordering/orderPlaceReservationNew)                                                                                                                                                                                 
        * [_Add_](ordering/orderPlaceReservationAdd)                                                                                                                                                                                   
        * [_Remove_](ordering/orderPlaceReservationRemove)                                                                                                                                                                           
    * [OrderApproved](ordering/orderApproved)                                                                                                                                
    * [OrderInfo](ordering/orderInfo)                                                                                                                                          
    * [OrderRemove](ordering/orderRemove)
    * [OrderDiscardAdd](ordering/orderDiscardAdd)
* Описание запросов, тип токена `discards`
	* [DiscardsSettings](discards/discardsSettings)
	* [DiscardsInfo](discards/discardsInfo)
* Описание запросов, тип токена `door_keeper`
    * [TicketCheck](tickets/ticketCheck)
* Структуры возвращаемые в запросах
    * [Error](replies/error) 
    * [Token](replies/token)                                                                                                                                               
    * [Cinema](replies/cinema)                                                                                                                                            
    * [Hall](replies/hall)                                                                                                                                                   
    * [Film](replies/film)                                                                                                                                                 
    * [Performance](replies/performance)                                                                                                                                    
    * [PlaceOnPerformance](replies/placeOnPerformance)
    * [Place](replies/place)
    * [Sale](replies/sale)
	* [SaleSettings](replies/saleSettings)  
	* [Order](replies/order)                                                                                                                          
    * [OrderSettings](replies/orderSettings)                                                                                                                                        
    * [OrderType](replies/orderType)                                                                                                                                        
    * [Discount](replies/discount)
    * [DiscardsSettings](replies/discardsSettings)
    * [DiscardsInfo](replies/discardsInfo)
    * [Ticket](replies/ticket)
    * [TicketCheck](replies/ticketCheck)
* [Коды ошибок](errors)