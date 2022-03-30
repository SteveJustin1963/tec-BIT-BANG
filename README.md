 
Investigate Bit Bang Serial for the TEC-1, that means no UART, only a latch  for each direction.   


## some examples  
- Southern Cross Computer (tec-1 clone), https://github.com/SteveJustin1963/tec-Southern-Cross-Computer
- tec_times 1990, serial uploader https://github.com/SteveJustin1963/tec-BOOKS/blob/master/TE/Mag/tec_times_1990_03.pdf
- bitbang from http://www.ganssle.com/articles/auart.htm
- RS2014
- and more
  

### serial on DAT board, D0 latch IN, D7 spkr OUT 

![](https://github.com/SteveJustin1963/tec-BIT-BANG/blob/master/pics/dat-ser-in2.png)

### untested idea
...use "shift" for serial in via Q  

![](https://github.com/SteveJustin1963/tec-BIT-BANG/blob/master/pics/another-hack1.png)

### untested idea
... lift and swap pins on 273 latch say pins 9 and 8 so data path reversed 

![](https://github.com/SteveJustin1963/tec-BIT-BANG/blob/master/pics/swap.png)

### the CJ port
15 dec 2021
Craig Jones

How do you get a serial port on your TEC-1D? This is how...

![](https://github.com/SteveJustin1963/tec-BIT-BANG/blob/master/pics/268641780_285024776923215_2514945051842294534_n.jpg)

![](https://github.com/SteveJustin1963/tec-BIT-BANG/blob/master/pics/bb-wir1.png)

 




