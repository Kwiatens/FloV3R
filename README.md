# FloV3R - DiY 6DoF VR Set
[This project is currently in developement, do not make it yet]

For more info join our Discord server by [clicking here!](https://discord.gg/63jcr22wdD)

### [Nettigo](https://nettigo.eu/) is a sponsor of this project, be sure to check them out <3
<p align="center">
  <img width="175" height="40.33" src="https://github.com/Kwiatens/FMS/assets/110034652/d75cc7bf-93fd-443e-ab1d-29554e22cad8">
</p>

## About the project
FloV3R is an DiY, affordable and super fun to build project made for tinkerers/hackers (not consumers :p).
It is built so that you can play any SteamVR game! It features 6DoF tracking on both the headset and controllers, which themself have a build in transcievers and LiPo batteries which make them wireless.

The whole build should be a bit over $140 (with 5.5" 2K @60Hz display), but it might be more expensive depending on where you order the parts from. (It might be cheaper too :p)

### Press [here](https://github.com/Kwiatens/FloV3R/blob/main/Instructions/About%20the%20project.md) to get started!

## Printed Circuit Boards

I designed the schematics and PCB's using KiCad 7.0.9 and 8.0. They are designed by me, but I took some inspiration from [HadesVR](https://github.com/HadesVR/HadesVR) due to the use of it's Steam driver (planning to make my own driver in the future, so more cool stuff can be added).
Circuit boards have some SMD components. If you are not feeling like soldering them by yourself, you can always buy pre-assembled PCB's.
Just keep in mind that this is also a good opportunity to learn how to solder them :)

PCB's for both the mainboard and controllers are designed for homemade fabrication, which i highly recommend.
They are pretty challenging to make due to them being double sided. If you want to try making them on your own, use some high precision method such as the one with photo resist film.
I recommend applying soldermask to the board. For doing vias you can use a wire from RJ45 cable so that you insert them into the via and solder it from both sides.

### FloV3R R1 Mainboard
> FloV3R R1 GEN 5 Headset Mainboard:
![obraz](https://github.com/Kwiatens/FloV3R/assets/110034652/1c912fa8-ed6f-4ef0-9f0a-33c0d00a81ab)

> FloV3R R1 GEN 5 Mainboard Schematic:
![obraz](https://github.com/Kwiatens/FloV3R/assets/110034652/3382e2a8-382d-47ce-9b34-629fe293ed5d)


This board will be inside your headset, it collects the rotation data from the IMU, recieves data packets from controllers, sends it to your computer via USB and controls face cooling fans.
In future it will send data to the controller so it knows when to turn on/off the vibration motor inside of it.
It uses some SMD components, but don't be scared of them, they are pretty big and after one youtube tutorial you will be able to do it. 
But if you still would have some trouble just DM me on Discord, I will help ;).

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
| 10 uF Electrolitic Capatitor (SMD 4x5.3mm) | 1 | $0.02 |
| 22 uF Electrolitic Capatitor (SMD 4x5.3mm) | 1 | $0.02 |
| 1K Resistor (SMD 1206) | 1 | < $0.01 |
| 10K Resistors (SMD 1206) | 2 | < $0.01 |
| 470R Resistor (SMD 1206) | 1 | < $0.01 |
| | | Total: ~$11 + PCB |

*DO NOT buy an Arduino Pro Micro with an micro USB connector, ONLY buy USB-C one! (The micro USB ones have a suuuper weak solder joint with the connector and it can just break off - learned that the hard way...)

**Neopixel with cables (this is how it should look like):
![IMG_20240205_185522214](https://github.com/Kwiatens/FloV3R/assets/110034652/f8a02026-e44f-48e7-b214-850d3dad86cc)


Begin soldering SMD resistors, capatitors and the voltage regulator, then electrolitic capatitors, LED and finally breakout boards such as Arduino, IMU etc.
Then plug it into you computer and flash the firmware to it. (todo)


### FloV3R R1 Controller Mainboard

> FloV3R Controller R1 board:
![obraz](https://github.com/Kwiatens/FloV3R/assets/110034652/ea015f0c-00d7-4f16-8023-958f9d73dde4)

> FloV3R Controller R1 Schematic:
![obraz](https://github.com/Kwiatens/FloV3R/assets/110034652/0a64ae67-9127-4a70-85ec-62631261c779)


FloV3R Controller works on Arduino Pro Mini, MPU6050 IMU and NRF24l01 transceiver module.
Tracking is done using illuminated ping-pong balls, [PSMoveServiceEx](https://github.com/Timocop/PSMoveServiceEx/releases) is used to track them.
On the PCB there are pads for connecting wires that go into LiPo charging and protection module (I'm looking into integrating it into the PCB).
For the assembly you would need some 3D Printed parts, if you don't have a 3D-Printer I would recommend purchasing them from JLCPCB or some other 3D printing company.
It uses an analog stick from an Xbox Series X controler (ALPS).
You could use hall-efect based ones for highier reliability, but they are more expensive so I won't include them in the final price.

For iluminating the ping-pong ball on it we use NeoPixel LED's (same as headset).
Tracking is done via PSMoveServiceEx and at least two cameras (PS Eye Camera highly recommended!)

Part list for FloV3R VR Controller R1 (for each controller):
| Part | Quantity | Estimated Price per piece |
| ------------- | ------------- | ------------- |
| Arduino Pro Mini | 1 | $2 |
| MPU6050 IMU (3.3V) | 1 | $2 |
| 1914 ALPS Analog stick (Xbox X/S) | 1 | $3 |
| NRF24l01 | 2 | $1.3 |
| LiPo 1-Cell 3.7V battery (minimum recommended capacity - 1200mAh/4.44Wh)| 1 | $4 | 
| TP4056 USB-C LiPo Charging Circuit | 1 | $1 |
| AZ1117H-3.3TRE1 Voltage regulator (SOT223) | 1 | $0.15 |
| Female Header Pins | 1 | $0.1 |
| Push button 6x6mm | 5 | $0.05 |
| 10 uF Electrolitic Capatitor (SMD 4x5.3mm) | 1 | $0.02 |
| 22 uF Electrolitic Capatitor (SMD 4x5.3mm) | 1 | $0.02 |
| 10K Resistors (SMD 1206) | 2 | < $0.01 |
| 3.3K Resistors (SMD 1206) | 1 | < $0.01 |
| 1K Resistor (SMD 1206) | 1 | < $0.01 |

To flash the frimware on it I recommend 'TTL PL2303' programmer.

You can download the driver for it by clicking [here](https://www.miklor.com/COM/UV_Drivers.php).

Vibration motors will be added to this controllers in the future.

## Display and Optics

FloV3R is designed for an 5.5" 2K @ ~60Hz* LS055R1SX04 display, but with some CAD model editing it could fit pretty much any screen.
However I still recommend sticking with LS055R1SX04 one just for simplicity.

Headset uses 40mm, 50mm focal length Fresnel lenses with 0.3mm steps.

*Some driver boards can be pushed to 72Hz.

Part list for FloV3R headset optics:
| Part | Quantity | Estimated Price per piece |
| ------------- | ------------- | ------------- |
| LS055R1SX04 Display | 1 | $24 |
| LS055R1SX04 Driver board | 1 | $45 |
| Fresnel lenses (40mm Diameter, 50mm Focal length) | 2 | $2 |

<ins> Make sure that you get the display version WITH backlight that supports 60Hz refresh rate (SAME for driver board)! </ins>


![obraz](https://github.com/Kwiatens/FloV3R/assets/110034652/0ea9ef27-ec02-470e-af8e-bcbfe34f00b5)

Here are the links from where I ordered:

- Buy Fresnel lenses here: [AliExpress](https://pl.aliexpress.com/item/1005004217107517.html?spm=a2g0o.cart.0.0.3029452cEMsRbM&mp=1&gatewayAdapt=glo2pol)

- Buy 5.5" LS055R1SX04 1440*2560 (2K @60Hz) display here: [AliExpress](https://pl.aliexpress.com/item/4000999801804.html?spm=a2g0o.order_list.order_list_main.5.23181c24EYUSo8&gatewayAdapt=glo2pol)

- Buy LS055R1SX04 driver board here (<ins>Get the C version</ins>): [AliExpress](https://pl.aliexpress.com/item/1005005216344799.html?spm=a2g0o.order_list.order_list_main.4.23181c24EYUSo8&gatewayAdapt=glo2pol)

Be super careful with handeling the display! It's very thin and can be damaged easily.

## 3D Models and printing them

The whole FloV3R set is almost entirely 3D Printed. It consists of many parts, which you can download from Printables.
Two controllers and the headset will take ~24 hours to print (aprox).
Everything is ment to be printed in PLA/ABS/ASA/PET-G filament.

### FloV3R Headset R1
FloV3R Headset is made out of 12 3D Printed parts, that should take around 12 hours to print.


### FloV3R Controller R1
![IMG_20240424_224109136](https://github.com/Kwiatens/FloV3R/assets/110034652/608481d2-30a1-4e10-907d-e836a4641e0b)
Our controller requires 8 - 3D printed parts, that should take around 6 hours to print (~70mm/s @3.5k accel) it might be more or less depending on your printer.
Make sure to add support material to the front and back shell.

You can download FloV3R Controller R1 3D files here: https://www.printables.com/model/954628-flov3r-vr-controller

# Future plans
todo




