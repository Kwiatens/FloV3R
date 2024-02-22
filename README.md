# FloV3R - DiY 6DoF VR Headset
[This project is currently in developement, do not make it yet]
For more info join our Discord server: https://discord.gg/63jcr22wdD

FloV3R is an DiY, affordable, and a super fun to build project made for tinkeres.
It is built so that you can play any SteamVR game! It features 6DoF tracking on both the headset and controllers, which themself have a build in transcievers and LiPo batteries which make them wireless.

The whole build should be around $100 (with 2K display), but it might be more expensive depending on where you order the parts from. (It might be cheaper too :p)

## Printed Circuit Boards

I designed the schematics and PCB's using KiCad 7.0.9. They are designed by me, but I took inspiration from [HadesVR](https://github.com/HadesVR/HadesVR).
Circuit boards have some SMD components. I went this route because they are just more suitable for the purpose of something that you hold/wear.
If you are not feeling like soldering them by yourself, you can always buy pre-assembled PCB's.
Just keep in mind that this is also a good opportunity to learn how to solder them :)

PCB's for both the mainboard and controllers are designed for homemade fabrication, witch i highly recommend.
They are pretty challenging to make due to them being double sided. If you want to try making them on your own, use some high precision method such as the one with photo resist film.
I recommend applying soldermask to the board. For doing vias you can electroplate them or use a wire from RJ45 cable so that you insert them into the via and solder it from both sides.
I will be dropping a tutorial on how to fabricate them in a near future!

### FloV3R R1 Mainboard
> FloV3R R1 GEN 4 Headset Mainboard:
![obraz](https://github.com/Kwiatens/FloV3R/assets/110034652/cef007e3-b4e6-4579-aa67-ac4fdbf1d79b)

> FloV3R R1 GEN 4 Mainboard Schematic:
![obraz](https://github.com/Kwiatens/FloV3R/assets/110034652/1c676128-ab0e-4c9c-91a5-6d1375e7dee4)

 
The mainboard of the headset is a dual layer PCB.
To get the position in space it illuminates a ping-pong ball, to get the rotation it uses MPU6050 IMU.
The illumination is done by a single Neopixel LED.

The board is pretty simple to assemble, you can look up schematics for it here: [To Do]

List of parts for the FloV3R R1 Headset Mainboard:
| Part  | Quantity | Estimated Price per piece |
| ------------- | ------------- | ------------- |
| Arduino Pro Micro (Clone works) | 1 | $5 |
| NRF24l04 | 2 | $1.3 |
| MPU6050 IMU (5V VERSION!) | 1 | $2 |
| NeoPixel LED | 1 | $0.5 |
| Push button 6x6mm | 1 | $0.05 |
| SMD (1206) 10K Resistors | 2 | cheap |

> Neopixel with cables (this is how it should look like):
![IMG_20240205_185522214](https://github.com/Kwiatens/FloV3R/assets/110034652/f8a02026-e44f-48e7-b214-850d3dad86cc)

[To Do]

### FloV3R R1 Controller Mainboard
> FloV3R R1 Controller Mainboard:
![obraz](https://github.com/Kwiatens/FloV3R/assets/110034652/0f07a239-7f68-4b9c-bd52-e8954fd70ede)

FloV3R Controller works on Arduino Pro Micro (8MHz @3.3V), MPU6050 IMU and NRF24l01 radio module.
Tracking is done using illuminated ping-pong balls, [PSMoveServiceEx](https://github.com/Timocop/PSMoveServiceEx/releases) makes it possible.
It *does not use Bluetooth*, instead we use RF transceivers for it since it's simpler (still totally wireless).
On the PCB there are pads for connecting wires that go into LiPo charging and protection module (I'm looking into integrating it into the PCB).
For the assembly you would need some 3D Printed parts, if you don't have a 3D-Printer I would recommend purchasing them from JLCPCB or some other 3D printing company.

For iluminating the ping-pong ball on it we use NeoPixel LED's (same as headset mainboard).
Tracking is done via PSMoveServiceEx and at least two cameras (PS Eye Camera highly recommended!)

Part list for FloV3R VR Controller R1:
[To Do]

## Displays

This headset is compatible with pretty much any screen, although I recommend following this guide from [HadesVR - Choosing the display](https://github.com/HadesVR/HadesVR/blob/main/docs/Headset.md#displays).

I went with "LS055R1SX04 with Green board", due to pretty good resolution (2K @72Hz) and good price.
> LS055R1SX04 + Controll Board:
![obraz](https://github.com/Kwiatens/FloV3R/assets/110034652/ff7a0b52-771f-464c-926a-161258659656)









