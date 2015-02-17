# Week Seven Meeting Notes 2/17/2015

## Starting topics
* Separate ground connections from different circuits unless then NEED to be connected.  Connecting separate circuits imply that they need to be close and are related when they aren't

* Add pull up to NRST on the supply sheet not sheet 1


## SD card 
* Connect SD card detect to GPIO and gnd
* The SD car needs a power switch on the 3.3V (pfet switch)
	*	Add some 10uF and 100nF capacitors
	*	Add soft start on the pfet switch as well (capacitor)

## ULPI
*	ULPI check if it REALLY needs 1.8V supply - YEP IT NEEDS ONE
	*	a linear supply should be fine unless the current is 100mA use SPS
		*	28mA - see table 1
*	Double check about clock out, see if it really needs to be hooked up to STM32
*	Read about using the FS_DM/DM 
	

## micro usb connector
*	Add a 100nF cap from the shield of the micro connector to ground as per figure 8.1

## BOOT0/1
*	Connect BOOT0 to header to allow user to jumper it for desired boot mode
*	Connect BOOT1 to a header that we won't stuff

## Can the STM32 boot using the either USB FS or HS and is there a detect? 
*	DFU - device firmware update
*	Can we just use the secondary FS for this?

## ECOD
*	make 1 header right angle male pins 0.1" pitch for each network, include pwr and gnu
*	behind that use fine pitch 0.05" male headers 
*	one connector will be I2C 
*	another connector will be "mBUS" (I2C)


## LEDs
* if GPIO is under 20 research port expander
	*	Look for a I2C PORT Expander 
		*	the I2C is our mBus that will connect to 8 LEDs 
* Try to connect the RBG LED's to GPIO that have PWM (timer output)

## Research SPI driven DAC
*	it should exceed marionette's DAC 
	*	(SPI BUS) fast would be nice if 42MHz but most likely will be ~25MHz
*	Cap $5.00
*	8 DAC's would be awesome
*	12-bit resolution
*	0-3.3V output 
*	If we find a really really good one maybe ditch the STM's DAC
