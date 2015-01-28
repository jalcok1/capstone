<h1> Week 3 Meeting Notes 11/27/2015 10am </h1>

<h2> Pin Review </h2>
1. Choosing SWD over JTAG
2. There are reserved pins that we need to use
 * SMBus
 * OSC pins
3. Need to minimize collateral damage when selecting pins
4. Timers will be output as GPIO
5. Most everything will default to GPIO
6. ULPI and Ethernet will never be used at the same time
7. Possible scope expansion to two different boards
 * One with ULPI
 * One with Ethernet
8. Minimum bus requirements for board
 * 8 ADC
 * 1 SPI
 * 1 I2C
 * 1 CAN
 * 1 UART
9. Some pins come up in a non-traditional state
 * JTDI - PA15, comes up as a pull up
 * JTDO - PB3, comes up in a floating state
10. No need to worry about FSMC (Flexable static memory controller) pins
11. If internal SPI is needed we will use USART

<h2> Final Thoughts </h2>

<h3> Ideal configuration </h3>
1. 16 DAC
2. 16 ADC
3. 2 of every bus
4. SDIO <br>
Get as close as possible and give thought to future upgradability.
