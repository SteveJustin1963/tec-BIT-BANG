## Introduction
Investigate Bit Bang Serial for the TEC-1, no UART, only latch
 


## Observe and Question 
ascii and or file transfer useful addition to hex keypad entry. whats the easiest hack to transfer to TEC1? bitbang !
see


## Theory
https://en.wikipedia.org/wiki/Bit_banging

termnal > ascii > ttl > latch > bit/time/loop > byte > hex or ascii > code


bit bang code plus an uploader, via virtual serial port. 
Can add UART chip to TEC-1 later. 
Therefore enter small amount of code via hex keypad to run bitbang serial and intel hex transfer.
 
## Predict
* serial hex transfer to and from memory  
* serial for apps
* serial for forth

examples  
* Southern Cross Computer (tec-1 clone) bitbang code
* tec_times 1990, serial loader
* bitbang from http://www.ganssle.com/articles/auart.htm




## Method
1.HW
 * USB-TTL cable (has FT232R or PL2303TA) get from ebay
   * 4 wires, Red=+5V, Black=GND, White=RXD, Green=TXD (ignore RTS, CTS, DSR)
 * add current limit resistors if needed, can ignore
 * PnP loads drivers, verify; see device manager or >cmd >mode 
 * Loopback test, load putty or tty, link TX-RX (white green) cable, typing should echo to screen
 4. connect cable to 2 free ports on TEC-1 and GND,run TTY or PUTTY etc, link com port or USB-TTL-cable to free io line on TEC-1,  
 

* or true serial-serial, use MAX232 chip 
  
### Steps
1. Source code for Bit Bang Serial without UART (unfinsihed project)
2. Add RAM stack, https://github.com/SteveJustin1963/tec-RAM-STACK
3. Locate free IO line, and .equ in code to match port

5. Enter hex code into TEC-1 (furuture ROM ?) 
 * or via https://github.com/SteveJustin1963/tec-EMU-BG
6
Connect TTL end to TEC1
Upload HEX via serial

download them with tokens; 
fetch a byte, 
store byte 
run [those] subroutine 


## Test

## Report, figures, tables

## Results

## Discuss objectively, scientific significance 

## Conclusion 

## Acknowledgements
Jim Robertson


## Inspiration:
2019 "Jim Robertson ... Interestingly, I found proof that the TEC-1 actually did support loading and parsing intel HEX files from the PC and actually had bi-directional bit-banged comms support at multiple baud rates. Therefore these things can be added to any revision without claims that it defeats the legacy scope of the TEC. ... Unfortunately, the source code is actually a barebones reconstruction from a disassembler and lacks comments. However, I tend to be able to read assembler as easy as plain English so it should be fun going through it all again. (Should I mention that I'm somewhat dyslexic?) :) I also found code that reminded me that I had plans to replace the EPROM with an EEPROM and so that new monitors could be "flashed" onboard the TEC. No UV eraser or, ahem, screwdriver required. There is code for a 8255 PPI based general purpose EPROM programmer included in the archive. Anyway, I've only glanced at the code so it all awaits a detailed review when I get home. Should be interesting!" (https://www.facebook.com/groups/AusVintage/search/?query=Interestingly%2C%20I%20found%20proof%20that%20the%20TEC-1&epa=SEARCH_BOX)


## References


http://www.edaboard.com/attachment.php?attachmentid=82290&d=1351849308

https://github.com/SteveJustin1963/tec-BOOKS/blob/master/TE/Mag/tec_times_1990_03.pdf

https://en.wikipedia.org/wiki/Bit_banging

http://www.ganssle.com/articles/auart.htm

RC2014 https://github.com/RC2014Z80/RC2014/tree/master/BASIC-Programs/hexload

https://github.com/SteveJustin1963/tec-PPI

https://www.chiark.greenend.org.uk/~sgtatham/putty/

https://sourceforge.net/projects/realterm/files/Realterm/2.0.0.70/

http://www.interfacebus.com/Design_Connector_RS232.html

https://cdn-shop.adafruit.com/datasheets/DS_PL2303TA_d20120504.pdf

http://pages.cs.wisc.edu/~bolo/shipyard/3ins4th.html

http://labs.domipheus.com/blog/teensy-z80-part-1-intro-memory-serial-io-and-display/

https://github.com/postfalk/z80/blob/master/z80asm/bootloader.asm

https://raspberrypi.stackexchange.com/questions/1987/can-raspberry-pi-reliably-bit-bang-a-9600-baud-serial-and-is-there-example-code

## Iterate, new hypotheses or predictions
1. rewrite in Forth
2. alternative https://github.com/SteveJustin1963/tec-BOOT-JM

 



