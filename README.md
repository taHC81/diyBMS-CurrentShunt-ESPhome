# Standalone implementation of diyBMS-CurretnShut

Excellent battery monitor ![diyBMS-CurretnShut by Stuart Pittaway](https://github.com/stuartpittaway/diyBMS-CurrentShunt) shall be used as a standalone device and integrated to a Home assistand with an ESPhome node using RS485 connection. Provided YAML configuration file includes all sensors and input numbers in order to configure CurretnShunt.

## Notes
- modbus configuration should be modified according to your needs
- power is somehow strangely reported (invalid sign for low power readings), thus the template sensor (CurrentShunt Power reg) has been created
- daily mAh is resetting at midnight, and also during 100% SoC calibration which happens on reaching Fully Charged Voltage and current lower than Tail Current for few minutes. I'd suggest to create Utility meter on HA side to have consistent values.

## diyBMS-CurrentShunt
![HW](https://github.com/taHC81/diyBMS-CurrentShunt-ESPhome/blob/main/currentshunt.jpg?raw=true)

## ESPhome / Home assistant entities
![HW](https://github.com/taHC81/diyBMS-CurrentShunt-ESPhome/blob/main/cs-entities.png?raw=true)

## Youtube video
[![Video](https://img.youtube.com/vi/P4SeWt5aov0/0.jpg)](https://www.youtube.com/watch?v=P4SeWt5aov0)
