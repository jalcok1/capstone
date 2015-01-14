#Week 2 Meeting Notes 1/13/2015 10am

##Block Diagram review and needed corrections

##Level 0<br>

###Input corrections

1. Change USB OTG to High Speed Upstream
2. Remove ADC, DAC, I2C, CAN, and UART from inputs
3. Change SWJ to SWD
4. Add USB Full Speed Debug to inputs

###Output corrections

1. Change USB OTG to USB Full Speed
2. Change Digital out to Digital I/O
3. Remove SWJ

##Level 1<br>

###Input corrections

1. Change SWJ to SWD
2. Change USB 2.0 to USB High Speed
3. Change Wall wart value to 5V
4. ***May:*** Add clock synchronization across Marionette boards (Clock plus sync, need to add this when creating PDS)

###Output corrections

1. Add USB Full Speed
2. Add ADC 
3. Remove Ethernet (Ethernet and USB connections are either or)

##Level 2 <br>

1. Change SPS/LDO connection from serial to parallel

##General Points of discussion

1. Add SDIO for micro SD card (This is both an input and an output)
 1. Only need 4 data pins for SDIO
 2. Need to be able to power-cycle SDIO
2. Reserve one of the I2C busses for use as a Marionette ID (paired with EEPROM. Also see note 7 below)
3. GPIO pins that are only 3.3 volt tolerant, will this be user configurable for analog inputs or will this be protected? We want to be able to reduce user error without alienating advanced users.
4. Compatibility with Waveshare boards, how far can we push this?
5. We want supercapacitor and vBat for a Real Time Clock (relevant http://electronics.stackexchange.com/questions/129405/supercap-charging-circuit-for-rtc-backup-on-stm32)
6. Add RGB LED for heartbeat/power indicators. How many LEDs do we need? 
 1. Claim one of the I2C busses for internal Marioneet bus (Port Expander) for system level control, configuration of input/output control, LED's, EEPROM, etc. 
 2. Beyond 8 LEDs we may as well have an LCD daughter board that runs off the management bus.
 
##Research and Homework for next week

1. Read the STM32 datasheet (Reference manual too).
2. Reread the STM32 datasheet
 1. Focus on periphreals first then move on to ADC and DAC
3. Prepare questions for K and Andrew
4. Prepare for PIN by PIN REVIEW





