# Home-Automation-Using-IR-sensor-and-Bluetooth

Serial Protocol:
Set HC05 and Microcontroller as 1 start Bit, 1 stop Bit, 8 data bit, No parity bit, 9600 Baud Rate
HC05 Connection Diagram:

![x](https://user-images.githubusercontent.com/35787202/127711219-8a3c122a-62ac-4987-b6c6-533f3ce892dd.jpg)

IR sensor Connection: 
IR Vcc is connected to MCU Vcc
IR Gnd is connected to MCU Gnd
IR Out is connected to PINB2
Load Connection:
Load 1/Light1 is connected to PINB0
Load2/Light2/Fan 1 is connected to PINB1

Component Needed:
1)Atmega328p Microcontroller:150Taka(https://bdspeedytech.com/index.php?route=product/product&product_id=445)

2)HC-05 Bluetooth Module:240   Taka(https://bdspeedytech.com/index.php?route=product/product&product_id=1384)

3)IR  Sensor:50Taka(https://bdspeedytech.com/index.php?route=product/product&product_id=238)

4)Relay Module: 220Taka(https://bdspeedytech.com/index.php?route=product/product&path=25&product_id=248)

5)Light Bulb/Fan etc as your wish

6) Android Phone

7)Three resistor of Identical Value

Program Algorithm:
•	If there is a data received by microcontroller UART then a receive interrupt is triggered. In interrupt routine it is checked what equipment to on or off. Here 
‘a’=light 1 on
‘b’= light 1 off
1= light 2 /fan 1 is on
2= light 2/fan 1 is off

•	Microcontroller always check if IR sensor sense an obstacle at the door. If there is a obstacle then all light and fan are turned on.


Relay Module:
There are three output connector for each relay. Middle should be used all the time. The other twos are normally open and normally closed with middle connector.

If Jumper of the relay is connected then it takes power from microcontroller board. If the jumper is disconnected then relay is isolated from microcontroller and separate 5v

supply need to given.

Relay is low triggered. That means when input is 0 relay is ON and when input is 5V relay is off.

