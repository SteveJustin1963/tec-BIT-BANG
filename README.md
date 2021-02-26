 
Investigate Bit Bang Serial for the TEC-1, no UART, only latch etc.  
pc termnal > ascii > ttl > port >data bus > byte > buffer > code 


## code examples 
* Southern Cross Computer (tec-1 clone), https://github.com/SteveJustin1963/tec-Southern-Cross-Computer
* tec_times 1990, serial uploader
* bitbang from http://www.ganssle.com/articles/auart.htm
* rs2014
* 

## io latches for serial


![](https://github.com/SteveJustin1963/tec-BIT-BANG/blob/master/pics/dat-ser-in2.png)
* serial on DAT board, D0 latch IN, D7 spkr OUT 

![](https://github.com/SteveJustin1963/tec-BIT-BANG/blob/master/pics/another-hack1.png)
* use "shift" for serial in via Q  

![](https://github.com/SteveJustin1963/tec-BIT-BANG/blob/master/pics/swap.png)
* lift and swap pins on 273 latch say pins 9 and 8 so data path reversed 




 




