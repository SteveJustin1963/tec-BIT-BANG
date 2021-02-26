 
Investigate Bit Bang Serial for the TEC-1, no UART, only latch etc.  
pc termnal > ascii > ttl > port >data bus > byte > buffer > code 


## code examples 
* Southern Cross Computer (tec-1 clone), https://github.com/SteveJustin1963/tec-Southern-Cross-Computer
* tec_times 1990, serial uploader
* bitbang from http://www.ganssle.com/articles/auart.htm
* rs2014
* 

## io latches for serial

* serial in dat board, serial out, D6
![](https://github.com/SteveJustin1963/tec-BIT-BANG/blob/master/pics/dat-ser-in.png)

* lift and swap pins on 273 latch say pins 9 and 8 so data path reversed 

* use "shift" for serial in via Q  
![](https://github.com/SteveJustin1963/tec-BIT-BANG/blob/master/pics/another-hack1.png)


* bad hack yuk
![](https://github.com/SteveJustin1963/tec-BIT-BANG/blob/master/pics/txrx-kb.png)
* serial in 74c923 hack





 




