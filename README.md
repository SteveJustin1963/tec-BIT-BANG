 
Investigate Bit Bang Serial for the TEC-1, no UART, only latch. for proper serial use UART chip. 
 
pc termnal > ascii > ttl > tec1-latch > bit/time/loop > byte > buffer code
buffer > reverse from above

code examples from
* Southern Cross Computer (tec-1 clone), https://github.com/SteveJustin1963/tec-Southern-Cross-Computer
* tec_times 1990, serial loader
* bitbang from http://www.ganssle.com/articles/auart.htm
* rs2014

io latches for serial
* serial in dat board
* serial in 74c923 hack
* serial out, pin 6


serial apps
* intel hex file uploader, rs2014, 
* 3 token forth, https://github.com/SteveJustin1963/tec-3RS
* stream data from app into serial
* serial video, https://github.com/SteveJustin1963/tec-EYE
* data logging, https://github.com/SteveJustin1963/tec-DATA-LOG
* ppp protocol, https://github.com/SteveJustin1963/tec-TCPIP
* DCE serial device w/r/control
* digital radio tx, https://github.com/SteveJustin1963/tec-RTTY
  
  







 




