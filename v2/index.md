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
    * [DiscountSettings](common/discountSettings)                                                                                                                                       
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
    * [SaleSearch](sales/saleSearch)
    * [SaleSearchByPerformance](sales/saleSearchByPerformance)
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
    * [OrderSearch](ordering/orderSearch)
    * [OrderSearchByPerformance](ordering/orderSearchByPerformance)
* Описание запросов, тип токена `discards`
	* [DiscardsSettings](discards/discardsSettings)
	* [DiscardsInfo](discards/discardsInfo)
	* [DiscardsSearch](discards/discardsSearch)
* Описание запросов, тип токена `door_keeper`
    * [TicketCheck](tickets/ticketCheck)
    * [SaleCheck](sales/saleCheck)
* Описание запросов, тип токена `cashiers`
    * [SessionOpen](cashiers/sessionOpen)
    * [SessionClose](cashiers/sessionClose)
    * [SessionHasOpened](cashiers/sessionHasOpened)
    * [StockInfo](cashiers/stockInfo)
    * [StockEnable](cashiers/stockEnable)
    * [StockDisable](cashiers/stockDisable)
    * [StockTurn](cashiers/stockTurn)
    * [TicketSearch](cashiers/ticketSearch)
    * [TicketReturn](cashiers/ticketReturn)
    * [TicketsReturn](cashiers/ticketsReturn)
    * [TicketPrint](cashiers/ticketPrint)
    * [TicketListReturns](cashiers/ticketListReturns)
    * [TicketListOnline](cashiers/ticketListOnline)
    * [ReportsInfo](cashiers/reportsInfo)
    * [ReportsGenerate](cashiers/reportsGenerate)
    * [ReportsData](cashiers/reportsData)
    * [PlacesTake](cashiers/placesTake)
    * [PlacesFree](cashiers/placesFree)
    * [PlacesInfo](cashiers/placesInfo)
    * [PlacesClear](cashiers/placesClear)
    * [PlacesDiscountAdd](cashiers/placesDiscountAdd)
    * [PlacesDiscountRemove](cashiers/placesDiscountRemove)
    * [PlacesConvertToOrder](cashiers/placesConvertToOrder)
    * [PlacesConvertToSale](cashiers/placesConvertToSale)
    * [PlacesDiscardAdd](cashiers/placesDiscardAdd)
    * [PlacesDiscardRemove](cashiers/placesDiscardRemove)
    * [PlacesCertAdd](cashiers/placesCertAdd)
    * [PlacesCertRemove](cashiers/placesCertRemove)
    * [OrderConvertToPlaces](cashiers/orderConvertToPlaces)
    * [DiscardsBonusesAdd](cashiers/discardsBonusesAdd)
    * [DiscardsAdd](cashiers/discardsAdd)
    * [GoodsList](cashiers/goodsList)
    * [GoodsSale](cashiers/goodsSale)
    * [GoodsReturn](cashiers/goodsReturn)
    * [CertsList](cashiers/certsList)
    * [CertsSale](cashiers/certsSale)
    * [CompaniesList](cashiers/companiesList)
    * [CompaniesSearch](cashiers/companiesSearch)
    * [CustomersList](cashiers/customersList)
    * [CustomersSearch](cashiers/customersSearch)
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
    * [Stock](replies/stock)
    * [CashierPlace](replies/cashierPlace)
* [Отчеты](reports)
* [Коды ошибок](errors)