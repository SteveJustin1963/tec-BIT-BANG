## Bit Bang Serial for the TEC-1, that means no UART, only a latch for each direction.   

Bit-banging is a technique for serial communication that allows a device to transmit and receive data using only a single data line. It involves manually toggling the line between high and low states to transmit each bit of data. To transmit data using bit-banging, the sender device sends a start bit, followed by the data bits, and then a stop bit. The start bit signals the start of the transmission, and the stop bit signals the end. The data bits contain the actual data being transmitted.
To receive data using bit-banging, the receiver device listens for the start bit and then samples the data line at regular intervals to read the data bits. The receiver must be synchronized with the sender in order to correctly interpret the data. Bit-banging is a simple and low-cost method for serial communication, but it is generally slower and less reliable than using dedicated hardware for serial communication, such as a UART (Universal Asynchronous Receiver/Transmitter).

## hardware components:
We have the TEC-1 with digital input/output (I/O) lines that can be used to transmit and receive data. A transmission line, such as a wire (or a fiber optic cable or may other ways), to connect the sender and receiver devices. Optionally, a level shifter circuit to convert the logic levels of the sender and receiver if they are not compatible. We are using 5v on both sides so its not needed. To transmit data using bit-banging, the tec1 manipulates the state of its digital output line. The line is set to a high state to represent a logical 1 bit, and a low state to represent a logical 0 bit. The code toggles the line between high and low states at a specific baud rate to transmit each bit of data. 4800 would be used for a 4mhz clock. To receive data using bit-banging, the code monitors the state of the input line. We samples the line at regular intervals to read the data bits in, and then we can interprets the sequence of high and low states as the transmitted data and in this ascii or some other code if need be. we choose hardware components such as transistors, resistors or capacitors to interface with the transmission line and level shifter circuit. 


## DAT board- serial, D0 latch IN, D7 spkr OUT 

![](https://github.com/SteveJustin1963/tec-BIT-BANG/blob/master/pics/dat-ser-in2.png)

## 2021 Craig Jones bit bang  
a very simple way to get a serial port on your TEC-1D...

![](https://github.com/SteveJustin1963/tec-BIT-BANG/blob/master/pics/268641780_285024776923215_2514945051842294534_n.jpg)

![](https://github.com/SteveJustin1963/tec-BIT-BANG/blob/master/pics/bb-wir1.png)

## other 
- Southern Cross Computer (tec-1 clone), https://github.com/SteveJustin1963/tec-Southern-Cross-Computer
- tec_times 1990, serial uploader https://github.com/SteveJustin1963/tec-BOOKS/blob/master/TE/Mag/tec_times_1990_03.pdf
- bitbang from http://www.ganssle.com/articles/auart.htm
- RS2014
- and more


