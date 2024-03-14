# FloV3R - DiY 6DoF VR Headset
[This project is currently in developement, do not make it yet]
For more info join our Discord server: https://discord.gg/63jcr22wdD

### [Nettigo](https://nettigo.eu/) is a sponsor of this project, be sure to check them out <3
<p align="center">
  <img width="175" height="40.33" src="https://github.com/Kwiatens/FMS/assets/110034652/d75cc7bf-93fd-443e-ab1d-29554e22cad8">
</p>

## About the project
FloV3R is an DiY, affordable, and a super fun to build project made for tinkeres.
It is built so that you can play any SteamVR game! It features 6DoF tracking on both the headset and controllers, which themself have a build in transcievers and LiPo batteries which make them wireless.

The whole build should be around $120 (with 5.5" 2K @72Hz display), but it might be more expensive depending on where you order the parts from. (It might be cheaper too :p)

## Printed Circuit Boards

I designed the schematics and PCB's using KiCad 7.0.9 and 8.0. They are designed by me, but I took some inspiration from [HadesVR](https://github.com/HadesVR/HadesVR).
Circuit boards have some SMD components. If you are not feeling like soldering them by yourself, you can always buy pre-assembled PCB's.
Just keep in mind that this is also a good opportunity to learn how to solder them :)

PCB's for both the mainboard and controllers are designed for homemade fabrication, which i highly recommend.
They are pretty challenging to make due to them being double sided. If you want to try making them on your own, use some high precision method such as the one with photo resist film.
I recommend applying soldermask to the board. For doing vias you can use a wire from RJ45 cable so that you insert them into the via and solder it from both sides.
I will be dropping a tutorial on how to fabricate it in a near future!

### FloV3R R1 Mainboard
> FloV3R R1 GEN 5 Headset Mainboard:
![obraz](https://github.com/Kwiatens/FloV3R/assets/110034652/1c912fa8-ed6f-4ef0-9f0a-33c0d00a81ab)

> FloV3R R1 GEN 5 Mainboard Schematic:
![obraz](https://github.com/Kwiatens/FloV3R/assets/110034652/3382e2a8-382d-47ce-9b34-629fe293ed5d)



This board will be inside your headset, it collects the rotation data from the IMU, recieves data packets from controllers, sends it to your computer via USB and controls face cooling fans.
In future it will send data to the controller so it knows when to turn on/off the vibration motor inside of it.
It uses some SMD components, but don't be scared of them, they are pretty big and after one youtube tutorial you will be able to do it. 
But stull if you would have some trouble just DM me on Discord, I will help ;).

List of parts for the FloV3R R1 GEN 5 Headset Mainboard:
| Part  | Quantity | Estimated Price per piece |
| ------------- | ------------- | ------------- |
| Arduino Pro Micro* | 1 | $5 |
| MPU6050 IMU (3.3V) | 1 | $2 |
| NRF24l01 | 2 | $1.3 |
| 5V Fan | 2 | $1.2 |
| BC547 NPN Transistor | 1 | $0.5 |
| NeoPixel LED** | 5 | $0.5 |
| Red LED 3mm | 1 | $0.15 |
| AZ1117H-3.3TRE1 Voltage regulator (SOT223) | 1 | $0.15 |
| Female Header Pins | 1 | $0.1 |
| Push button 6x6mm | 1 | $0.05 |
| 1N4007 Diode | 1 | $0.03 |
| 10 uF Ceramic Capatitor (SMD 0805) | 1 | $0.2 |
| 100 nF Ceramic Capatitor (SMD 1206) | 1 | $0.05 |
| 10 uF Electrolitic Capatitor (SMD) | 1 | $0.02 |
| 22 uF Electrolitic Capatitor (SMD) | 1 | $0.02 |
| 1K Resistor (SMD 1206) | 1 | < $0.01 |
| 10K Resistors (SMD 1206) | 2 | < $0.01 |
| 470R Resistor (SMD 1206) | 1 | < $0.01 |
| | | Total: ~$11 + PCB |

*DO NOT buy an Arduino Pro Micro with an micro USB connector, ONLY buy USB-C one! (The micro USB ones have a suuuper weak solder joint with the connector and it can just break off - learnd that the hard way...)

**Neopixel with cables (this is how it should look like):
![IMG_20240205_185522214](https://github.com/Kwiatens/FloV3R/assets/110034652/f8a02026-e44f-48e7-b214-850d3dad86cc)


Begin soldering SMD resistors, capatitors and the voltage regulator, then electrolitic capatitors, LED and finally breakout boars such as Arduino, IMU etc.
Then plug it into you computer and flash the firmware to it. (todo)


### FloV3R R1 Controller Mainboard

> FloV3R R1 GEN 1 Controller board:
![obraz](https://github.com/Kwiatens/FloV3R/assets/110034652/94f9d562-fd8c-48a8-ba62-21e59fa5b4ea)

FloV3R Controller works on Arduino Pro Mini, MPU6050 IMU and NRF24l01 transceiver module.
Tracking is done using illuminated ping-pong balls, [PSMoveServiceEx](https://github.com/Timocop/PSMoveServiceEx/releases) makes it possible.
On the PCB there are pads for connecting wires that go into LiPo charging and protection module (I'm looking into integrating it into the PCB).
For the assembly you would need some 3D Printed parts, if you don't have a 3D-Printer I would recommend purchasing them from JLCPCB or some other 3D printing company.
It uses an analog stick from an Xbox Series X controler (ALPS).
You could use hall-efect based ones for highier reliability, but they are much more expensive so I won't include them in the final price.

For iluminating the ping-pong ball on it we use NeoPixel LED's (same as headset).
Tracking is done via PSMoveServiceEx and at least two cameras (PS Eye Camera highly recommended!)

Part list for FloV3R VR Controller R1 (for each controller):
| Part | Quantity | Estimated Price per piece |
| ------------- | ------------- | ------------- |
| Arduino Pro Mini | 1 | $2 |
| MPU6050 IMU (3.3V VERSION!) | 1 | $2 |
| Joystick | 1 | $3 |
| NRF24l01 | 2 | $1.3 |
| LiPo 1S 3.7V battery (minimum recommended capacity - 1000mAh)| 1 | $4 | 
| TP4056 USB-C LiPo Charging Circuit | 1 | $1 |
| AZ1117H-3.3TRE1 Voltage regulator (SOT223) | 1 | $0.15 |
| Female Header Pins | 1 | $0.1 |
| Push button 6x6mm | 4 | $0.05 |
| 10 uF Electrolitic Capatitor (SMD) | 1 | $0.02 |
| 22 uF Electrolitic Capatitor (SMD) | 1 | $0.02 |
| S1M Rectifier diode* (SMD) | 1 | < $0.01 |
| 10K Resistors (SMD 1206) | 2 | < $0.01 |
| 3.3K Resistors (SMD 1206) | 1 | < $0.01 |
| 1K Resistor (SMD 1206) | 1 | < $0.01 |

*This diode isn't required, however I HIGHLY recommended it for safety! (If not using it just short the connections on it's footprint)

To flash the frimware on it I highly recommend 'TTL PL2303' programmer.

## Displays

This headset is compatible with pretty much any screen, although I recommend following this guide from [HadesVR - Choosing the display](https://github.com/HadesVR/HadesVR/blob/main/docs/Headset.md#displays).

I went with "LS055R1SX04 with Green board", due to pretty good resolution (2K @72Hz) and good price.
> LS055R1SX04 + LS055R1SX04 Controll Board:
![obraz](https://github.com/Kwiatens/FloV3R/assets/110034652/ff7a0b52-771f-464c-926a-161258659656)









