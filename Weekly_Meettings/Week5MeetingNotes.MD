# Week Five Meeting Notes 2/03/2015 10am

##  Last Weeks Questions Addressed
* Drop out voltage limit on LDO
 * Not a concern
* SPS voltage isolation is a must
* ULPI PHY number of driver/receivers
 * Not a concern
 
## Beginning Topics
* Add no. 1 pin indicator to STM32
* Add BOM to capstone
* Choose an SMT crystal to replace the through hole one
 * Check for ST data sheet for recommended crystals
* LDO from 3.3-3.0 V - We might want this

## Eagle Discussion
* No silk screen on tplace layer, put on tdocu layer
* Fix current libraries so that pin is a short line in the schematics instead of circles
 * Continue with this for for all future libraries
* Add descriptions to all libraries
* Need preliminary schematic by next week at the latest
 * Andrew will upload previously built libraries
 * Andrew will provide eagle licenses by Thursday at the latest
  * Contact him if we don't have them by Thursday morning
* Need to use extensive silk screen labeling (this will increase board size)


## Hardware Discussion
* Use 16 MHz crystal for clock selection
 * Check what waveshare board uses and use that or similar
 * Use SMT
 * Analog band of concern is in the 100s of kHz range
* Schottkey Diodes
 * Minimize voltage drop without affecting maximum reverse voltage
 * Make sure diode is rated for at least 2x the current we will ever need
 * Reverse voltage must be at least 2x the voltage we need
* Need to choose connectors (edge connectors of death)
* Design should have 0.1" headers (initial breakout)
* Will need to design breakout board
 * This will decrease the footprint of the Marionette board
 * Use 2 layer board for breakout, this will decrease the overall cost of the board
 
## Questions we need to address in the coming weeks
 * ESD protection?
  * This needs to be done
* Anti aliasing?
 * Needs to be done
 * Active or passive?
  * Passive would be easiest and least expensive
* better front ends?
* More DACS?
 * Can provide this on the daughter board
* EEPROM?
* Crystals and SDCard?
 * Keep these as close as possible to the MCU
* Choice of analog reference voltage?
 * Read up on ADC periphreals on STM32 manual

## Research for next week
* What is the reference voltage and how do we change it if/as needed
* How many bits can we get out of our ADCs
* Sampling
 * How do we get the fastest speed that we can without sacrificing performance

