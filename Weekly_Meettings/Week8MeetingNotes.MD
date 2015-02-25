# Week Eight Meeting Notes 2/24/2015

## Starting Topics and Questions
* NSRT - are we sure we want an external pullup? Yes, 10k selection will work fine.
* OTG VBus connection (FS)?
 * Currently connected to VDD, need to connect it to ground
* RX pin for USART in SPI mode, can we use this as a GPIO? Yes.
* Be mindful of board size constrainsts
* Do we want to add a 2nd external DAC footprint that the end user can populate>
 * No, we will either add a 2nd DAC or find a minimum four output DAC chip
 * Use TSSOP package for external DAC chip
* Find a smaller 32 KHz Crystal

## Board Layout topics 
* ULPI needs to be on the same side as power
* We don't care about the placement of the SD Card on the board
 * Caveat: We don't want it to stick out past the board
* Want debug and USB on the same side as JTAG
* Start placing mounting holes early
 * Use mount library with size #4 screws (0.125mm, 1/8" holes)
 * Leave enough space for stand offs
* Keep networking stuff (clock edges) away from analog
 * Layout should be in the order of ADC, DAC, GPIO, then networking 
* Kill I2C SMBA pins
* Consider readability when placing silk screen for pin description
* Adjust size of connections so pins are not touching
* Change connector layout
 * Stack high desity connectors behind right angle connectors
 * Use 0.1" headers with a 0.3" space between them
 * Fix power connections
* Switch direction of SD card, its backwards

## Schematic Layout
* Change direction of power pins, ie change from supply to power
 * Supply pins are only for s
 * Power pins are for ICs
*Label schematics sections with Text Labels, i.e. GPIO, I2C, etc.

## Things we need to start addressing
* Can bus needs traseiver/receiver
 * Find an IC that will work for this 
* ESD Protection 
 * Look into Transient Voltage Supressors
 * Need one TVS per leg ( check if this is a feature of STM32F4)
 * It would be best if each Pin had ESD protection, look for ESD pass through

## For the next week
* Need rapid turn around this week
* Ask questions as soon as you have them
* Go over schematic
* Audit existing BOM
 * Check availability 
 * Look for EOL products
 * Check for any Eratta on chosen components
* Email updates IMMEDIATELY 
 
