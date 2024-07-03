# temperature-logger
16 channel precision temperature logger with PT100/PT1000 sensors

This piece of equipment was created to make the measurement of PCBs in enclosures possible. The device consists of the base module witch can act in there mode:
- standalone mode using Ethernet communication and powered by PoE, 
- connect to FPGA using DIOT or EEM standard, communicate whit onboard MCU via LVDS line,
- connect to FPGA using DIOT or EEM standard, communicate whit sensors via LVDS line and bypassing the internal MCU controller.
In first two modes data can by log using SD card. Management and configuration are done by USB-C port via Rust consol.

Main module can by connect to the sensors in several ways:
-	directly using screw terminals:  with long VHDCI cable. Length does not matter since the connectivity is with 4 wires
-	with 8 FFC/FPC jumpers. Each jumper supports up to 2 sensors. Jumpers up to 61cm are available
    
The main idea behind using the FFC/FPC jumpers is that they can be easily inserted using enclosure slots and do not affect the airflow.

