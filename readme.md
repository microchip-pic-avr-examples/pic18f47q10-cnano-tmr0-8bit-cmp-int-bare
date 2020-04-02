<div id="readme" class="Box-body readme blob js-code-block-container">
 <article class="markdown-body entry-content p-3 p-md-6" itemprop="text"><p><a href="https://www.microchip.com" rel="nofollow"><img src="images/MicrochipLogo.png" alt="MCHP" style="max-width:100%;"></a></p>

# PIC18F47Q10 Using TMR0 in 8-bit Mode with Periodic Interrupt:


## Objective:
This example describes how to configure Timer0 in 8-bit mode and to generate a compare interrupt every 100 ms
using LFINTOSC as clock source. A GPIO pin (the development board’s on-board LED) will be configured as output
and toggled each time the interrupt occurs. Additionally, the main clock will use a separate clock source (HFINTOSC)
and Timer0 will run asynchronously from the main clock.

## Resources:
- Technical Brief Link [(linkTBD)](http://www.microchip.com/)
- MPLAB® X IDE 5.30 or newer [(microchip.com/mplab/mplab-x-ide)](http://www.microchip.com/mplab/mplab-x-ide)
- MPLAB® XC8 2.10 or newer compiler [(microchip.com/mplab/compilers)](http://www.microchip.com/mplab/compilers)
- PIC18F47Q10 Curiosity Nano [(DM182029)](https://www.microchip.com/Developmenttools/ProductDetails/DM182029)
- [PIC18F47Q10 datasheet](http://ww1.microchip.com/downloads/en/DeviceDoc/40002043D.pdf) for more information or specifications.

## Hardware Configuration:

The PIC18F47Q10 Curiosity Nano Development Board [(DM182029)](https://www.microchip.com/Developmenttools/ProductDetails/DM182029) is used as the test platform.

The following configurations must be made for this project:
- Clock
	– Oscillator Select: HFINTOSC
	– HF Internal Clock: 1 MHz
	– Clock Divider: 1
- Port
	- RE0 (LED0) pin - Configured as digital output
- TMR0
	- TMR0 Enabled
	- Clock Prescaler: 1:16
	- Postscaler: 1:1
	- Timer mode: 8-bit
	- Clock Source: LFINTOSC
	- Synchronization: disabled
	- Timer period: 100 ms
	- Timer interrupt: enabled
- Watchdog Timer: disabled

## Demo:
Run the code, LED0 will toggle at a rate of 100ms. 

<img src="images/TMR0_8bit_cmp_int.gif" alt="Hardware Setup"/>