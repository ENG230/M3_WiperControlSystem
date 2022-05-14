# M3_WiperControlSystem
# BADGES
# Codiga
https://api.codiga.io/project/33449/score/svg

https://api.codiga.io/project/33449/status/svg

![windshield-wper](https://user-images.githubusercontent.com/83355817/168411897-7e5508de-896e-4f03-9737-94605f70382f.jpg)

Here we implemented Wiper Control System using STM32F407VG Board.

Rainwater, dust and exhaust gas chemicals from vehicles that stick to the surface of an automobile windshield are probably not an issue as long as the driver has an unobstructed view of the road. However, if the sticking substances are left unchecked, they will become a threat for travel safety.

## Features:

1.Ignition Key Position at ACC: The Red LED is ON, if the user button is pressed and held for 2 secs

2.Wiper ON: Wiper is OFF: On press of the user input, Blue, Green and Orange LEDs come ON one at a time with the set frequency, The frequency changes on every alternate key press, 3 frequency levels with 1, 4 and 8 Hz.

3.Wiper OFF: Wiper is ON: The LED glow pattern stops on the 4th press; the wiper action starts next press onwards as mentioned in step 2.

4.Ignition Key Position at Lock: The Red LED is OFF, if the user button is pressed and held for 2 secs.

5.Wipers returns back to their initial position even though they stuck in the middle position.
# Software Requiremets:
1.STM32 CUBE IDE

2.Xpack packages

  * Windows Build Tools
  * Open OCD
  * QEMU Software
# Components Used:
STM32F4O7VG MICROCONTROLLER BOARD

![STM32](https://user-images.githubusercontent.com/83355817/168412121-78299942-4dc6-4686-8bae-70905cf308be.jpg)

STM32F407 series of microcontrollers are high-performance MCUs designed for medical, industrial and consumer applications. It is based on ARM Cortex-M4 and offers up to 168MHz. The STM32F407VGT6 is the onboard chip which comes in a 100-pin LQFP package.

The STM32F407G-DISC1 is a Discovery Kit allows users to easily develop applications with the STM32F407 high performance microcontrollers with ARM cortex-M4 32-bit core. It includes everything required either for beginners or for experienced users to get quickly started. Based on the STM32F407VGT6, it includes an ST-LINK/V2 or ST-LINK/V2-A embedded debug tool, two ST MEMS digital accelerometers, a digital microphone, one audio DAC with integrated class D speaker driver, LEDs and push buttons and an USB OTG micro-AB connector.





## ADVANTAGES

*   Low cost automation project.
*   Free from wear adjustment.
*   Less power consumption.
*   Operating principle is very easy Installation is simple.
*   It is possible to operate manually/automatically by providing On/Off switch

## DISADVANTAGES

*   The rain sensor based system functions when water falls on the sensor directly.
*   The cost of overall system increases as additional components are needed along with rain sensor. 

## APPLICATIONS

*   used to remove rain, snow, ice, washer fluid, water, and/or debris from a vehicle's front window. Almost all motor vehicles, including cars, trucks, buses, train locomotives, and watercraft with a cabin—and some aircraft—are equipped with one or more such wipers, which are usually a legal requirement.

# BLOCK DIAGRAM
![BLOCK DIAGRAM (1)](https://user-images.githubusercontent.com/101693748/168218547-ca8edd38-6903-4d8d-b4fa-720618b8a066.png)
# FLOWCHART
![FLOWCHART 1](https://user-images.githubusercontent.com/101693748/168218561-281382d5-fa0a-484a-9d82-029d19521a35.png)



## High Level Requirements

|  ID  |   Description   |  Status  |
|------|-----------------|----------|
| HR_01| ACC Mode Operation| Implemented|
| HR_02|Wiper ON| Implemented|
| HR_03|Wiper Speed Change|Implemented|
|HR_04|Wiper OFF|Implemented|

## Low Level Reuirements

| ID	| Description	| Operation	|Status |
|-----|-------------|-----------|-------|
|LR_01|	Button pressed once for 2 secs|	Red LED ON	|Implemented|
|LR_02|	Button pressed second time|	1 Hz speed - Blue, Green Orange alternative|Implemented|
|LR_03|	Button pressed third time|4 Hz speed - Blue, Green Orange alternative	|Implemented|
|LR_04|	Button pressed fourth time|8 Hz speed - Blue, Green Orange alternative|Implemented|
|LR_05|Button pressed again for two seconds|Turn Off all LEDs|Implemented|
### OUTPUT IMAGES

<br  />

## Wiper ON STATE

<bs  />

![ON STATE](https://user-images.githubusercontent.com/89642370/168281628-68efeed6-2dff-4c95-a680-632d29b3d3fc.png)

<bs  />

## WIPER SPEED IS LOW

<bs  />

![WIPER SPEED IS LOW](https://user-images.githubusercontent.com/89642370/168281759-0454762c-8e53-41f2-a6f3-64b2855c3bd1.png)

<bs  />

## WIPER SPEED IS MODERATE

<bs  />

![WIPER SPEED IS MODERATE](https://user-images.githubusercontent.com/89642370/168281892-d91d6f6b-ed52-46a3-80a6-0477733c16db.png)

<bs  />

## WIPER SPEED IS HIGH

<bs  />

![WIPER SPEED IS HIGH](https://user-images.githubusercontent.com/89642370/168282083-504fec62-5364-4645-acb5-c2a3e619a2e8.png)

<bs  />

## Wiper OFF STATE

<bs  />

![OFF STATE](https://user-images.githubusercontent.com/89642370/168282238-96d3f26d-fe85-459f-b519-685b63c1084f.png)
