# Week Four Meeting Notes 1/27/2015 10am

##  ULPI with SDIO is the best choice in this instance
* Start with ULPI then fork to Ethernet time permitting

## Do we want the board to power external periphreal devices?
* Switching power supply will add to the cost 
* At this time leave that worry to the users
## Component research
* LDO - for analog
* SPS - for 5 V in, 3.3 V out
* Want Vbat with either battery or supercap
* Need to research/ think about overvoltage, undervoltage, and overcurrent

## Discussions on Eagle
* Andrew will be getting us 4 layer licences, start schematics and libraries with free versions for now
* Create all libraries as individual libraries

## GPIO Breakout and connectors
* .1" or 2mm?
* Pin connector cluster
* Right angle 2mm?
* High density edge connector (for JIGs) ?

## To do before neeks week
* Initial Bill of Materials
* Add/Create Eagle libraries
* Research components and their dependencies
* Improve block diagrams
* Continue working on PDS and Schedule
* Look on web for STM32F407i eagle packages on internet
