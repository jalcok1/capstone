# Week Six Meeting Notes 2/10/2015 10am

## Beginning Topics
* Vref - do we want to output a precision reference voltage
 * Input at 4.96 V every tic is a millivolt of 12 bit ADC. We can't do this, we need 2048
* We can cut the voltage rating closer for supercap
 * Target for vbat/supercap is seven days in standby with RTC
 * Check current rating on RTC 

## Crystal selection
* Don't pick the wrong one
* Don't care about start up time
* Crystal should not cost more than $0.15-0.20
* Frequency tolerance
 * 5ppm - Good
 * 10ppm - ok
 * 20ppm - Standard

## USB High Speed 
* Need 1.8 V to ULPI, used for internal HS logic
 * Give it a small LDO
* Research CLK_OUT on ULPI PHY
  * Should we tie it off?

## SWD connector
* Change SWD connector
 * Want the small connector not the big one
 * Need this to reduce board size
 
## Connectors 
* Tin or gold? Better to have gold
* Look into 20 pin connectors
* Analog pins need VDDA, VDD, and VRef
* Pin header library is in eagle

## Hardware Discussion
* Need pullups on network 
*  LED connections
* MBUS - choose I2C GPIO expander

## To do for next week
* Put together a board to ball park the form factor size
* Send Minutes to Gavin this week
* Capacitor SMD components 
 * 1 uF or greater - choose 0603
 * 10 uF or greater - choose 0805
 * 100 nF or below - 0402
* Be mindful of ESD, research and be ready for next week
* Choose reset switch and implement it
 * Want relatively small surface mount
 * Sparkfun has libraries for this - pull from there
 * K likes the one from the seeed studio cool runner board.
 
