# tec-BANG

## Abstract
A Bit Bang Serial for the TEC-1 (without UART) and hex transfer program.

## Introduction
Bitbang serial without hardware based on http://www.ganssle.com/articles/auart.htm


## Observe and Question 
File transfer hex easier than manual entry on keypad. How to transfer code to TEC1?

## Theory
Need bit bang code with simple uploader, uploading via serial port, but no serial port on basic TEC-1. Therefore enter small amount of code via hex keypad to run bitbang serial and intel hex transfer.
 
## Predict


## Method

Use a free IO line and USB-TTL cable with embedded FT232R chip. Bit Bang Serial without UART, use a free port and USB to TTL serial converter cables. FT232R chip is in cable. 

Run TTY app on PC eg PUTTY through USB to TTL serial cable (PL2303TA USB to Serial Bridge Controller). This is a cheap ebay item. Has 4 wires; Red=+5V, Black=GND, White=RXD and Green=TXD. No need for a “level shifter to convert RS-232 to TTL with a MAX232 chip. We can add current limit resistors for protection if needed.  Others may have extra wires for RTS, CTS, DSR etc. Ignore these. Win-7/10 wil auto load driver for it. Device manager will show new com-port. Verify; Run and type  “cmd”, enter, type in c:/mode, enter. 

Enter hex into TEC1 keypad (add to ROM ?)
Or via bennvenn.myshopify.com/pages/eprom-emulator
Add RAM stack
Connect USB-TTL to PC 
Auto install win drivers
Install PUTTY on PC
Do loopback test TX to RX
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
2019 "Jim Robertson ... Interestingly, I found proof that the TEC-1 actually did support loading and parsing intel HEX files from the PC and actually had bi-directional bit-banged comms support at multiple baud rates. Therefore these things can be added to any revision without claims that it defeats the legacy scope of the TEC. ... Unfortunately, the source code is actually a barebones reconstruction from a disassembler and lacks comments. However, I tend to be able to read assembler as easy as plain English so it should be fun going through it all again. (Should I mention that I'm somewhat dyslexic?) :) I also found code that reminded me that I had plans to replace the EPROM with an EEPROM and so that new monitors could be "flashed" onboard the TEC. No UV eraser or, ahem, screwdriver required. There is code for a 8255 PPI based general purpose EPROM programmer included in the archive. Anyway, I've only glanced at the code so it all awaits a detailed review when I get home. Should be interesting!"

## References

https://github.com/SteveJustin1963/tec-PPI

http://www.ganssle.com/articles/auart.htm

https://en.wikipedia.org/wiki/Bit_banging

https://www.chiark.greenend.org.uk/~sgtatham/putty/

http://www.interfacebus.com/Design_Connector_RS232.html

https://cdn-shop.adafruit.com/datasheets/DS_PL2303TA_d20120504.pdf

http://pages.cs.wisc.edu/~bolo/shipyard/3ins4th.html

http://www.oshonsoft.com/z80.html 

http://www.asm.80.com

http://labs.domipheus.com/blog/teensy-z80-part-1-intro-memory-serial-io-and-display/

https://github.com/postfalk/z80/blob/master/z80asm/bootloader.asm

https://raspberrypi.stackexchange.com/questions/1987/can-raspberry-pi-reliably-bit-bang-a-9600-baud-serial-and-is-there-example-code

## Iterate, new hypotheses or predictions

### Firth of Forth
write code loader in forth

### RC2014
https://github.com/RC2014Z80/RC2014/tree/master/BASIC-Programs/hexload

Look at how RC2014 does hex load over serial 

### 3ins4th
http://pygmy.utoh.org/3ins4th.html

3 token control
These 3-instructions are a pre-Forth; a tokenized instructions set to allow any host to interact with the TEC1. 
The host sends a single byte code to the TEC1. 
The 3 instructions are; 
XC@  fetch a byte code 01
XC!  store a byte code 02
XCALL jump to a subroutine code 03
and any other code is ignored. 

When the host wants to read a byte it first sends the 01 code to indicate an XC@ instruction and then sends two more bytes to tell the TEC1 which address should be read. 
Upon receiving the 01 code the TEC1 executes the XC@ instruction, which collects the two byte address, reads the byte at that address, and sends the value to the host. 
The XC! instruction works similarly. The host sends the 02 code followed by two bytes for the address and one byte for the value to be stored. 
For the XCALL instruction the host sends the 03 code followed by two bytes for the address. Using the XC! instruction you can download short subroutines for testing, or long programs if the target has enough RAM., or program onboard EEPROM if present. Once the routine is downloaded, the host can send the XCALL instruction to cause the TEC1 to jump to the newly downloaded routine. If the routine ends with a return instruction (RTS) then control will automatically return to the 3-instruction monitor.”

 

 
