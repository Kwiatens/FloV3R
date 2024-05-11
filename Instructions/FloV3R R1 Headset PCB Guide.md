### Building FloV3R - Part 3 - FloV3R Headset PCB
Alright, enough chit chat, let's move on into real work :)

This is what we are gonna build now:
> FloV3R R1 GEN 5 Headset Mainboard:
![obraz](https://github.com/Kwiatens/FloV3R/assets/110034652/1c912fa8-ed6f-4ef0-9f0a-33c0d00a81ab)

> FloV3R R1 GEN 5 Mainboard Schematic:
![obraz](https://github.com/Kwiatens/FloV3R/assets/110034652/3382e2a8-382d-47ce-9b34-629fe293ed5d)

This board will be inside your headset, it collects the rotation data from the IMU, recieves data packets from controllers, sends it to your computer via USB etc.

In future it will send data to the controller so it knows when to turn on/off the vibration motor inside of it.
It uses some SMD components, but don't be scared of them, they are pretty big and after one youtube tutorial you will be able to do it. 
If you would still have some trouble just DM me on Discord, I will help ;).

Here's a list of parts that we're gonna use:
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



