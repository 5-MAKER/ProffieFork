# ProffieFork
Hardware fork for Proffieboard V2.2 

https://fredrik.hubbe.net/lightsaber/v5/board22.html

https://github.com/profezzorn/ProffieOS

Project purpose:
- larger components, optimised for hand soldering
- larger board size 
- on-board connectors
- NO-killkey, momentary switch on/off power
- include IP5310 soc: bat charger + 3A 5V booster (provide power for neopixel or led driver)
- SDIO 
- various led driver sub-board (optional)

Main board - similar to Proffieboard V2.2, but without 6ch PWM mosfet.
Board size 50x19x1mm (draft).

Sub driver board variants:
* No board needed - for neopixel blade
* PWM 6ch N-mosfet output
* Linear driver 6ch AMC7135 based (350-750-1000mA output options)
* RGBW 4ch 1A dc-dc driver, may based on LED2000, TPS92200D1, LM3405A/LM3414, PAM2804, MP2480
* One 3A driver LED2001


#### Main board I/O 

Side power connector - MPX 8 pin socket (6,85mm height, 19,2mm with).

https://www.nexusmodels.co.uk/mpx-connector-moulded-8-pin-socket-black-male.html

Pins:
* VBAT - battery
* SP+/- speaker output
* Vusb - input from charge port
* V5 - booster output, provide power for neopixel

Side signal connector - JST PHD 10 pin 
(2mm pitch, side entry, 2x5pin, 5mm height, 12mm with).

https://cdn-reichelt.de/documents/datenblatt/C100/JST_PHD_DB_EN.pdf

Pins:
* GND 
* BTN1, 2 
* PWM4,5 - from 20ma driver
* Blade_ID
* NEO_data1, 2
* USB DP, DM

Other output pins:
I2C, UART, V33, BTN3

Pad pins (need special pogo-like connector):
BOOT, GND, SW_D, SW_C, RES 

Board 2 board connector - solder header 2mm pitch:
GND, VBAT, V5, 6ch PWM

