## Introduction:

The main purpose of the wiper Control system is to clean the windscreen sufficiently to provide suitable visibility at all times.
Rainwater, dust and exhaust gas chemicals from vehicles that stick to the surface of an automobile windshield are probably not an issue as long as the driver has an unobstructed view of the road. However, if the sticking substances are left unchecked, they will become a threat for travel safety.

A windshield wiper control system comprises a wiper drive and two wiper arms. The drive moves the two wiper arms at a certain angle across the windshield, providing a clear view for the driver and passenger. A specially-shaped rubber wiping lip ensures an optimal wiping result

Wipers are vital for driver visibility. The vehicle is considered unsafe if the wipers don't work. The front wiper motor and the wiper transmission mechanism (linkage) are installed below the windshield, under the cowl panel cover.

Here we implemented Wiper Control System using STM32F4Discovery Board.


## Features:

1.Ignition Key Position at ACC: The Red LED is ON, if the user button is pressed and held for 2 secs

2.Wiper ON: Wiper is OFF: On press of the user input, Blue, Green and Orange LEDs come ON one at a time with the set frequency, The frequency changes on every alternate key press, 3 frequency levels with 1, 4 and 8 Hz.

3.Wiper OFF: Wiper is ON: The LED glow pattern stops on the 4th press; the wiper action starts next press onwards as mentioned in step 2.

4.Ignition Key Position at Lock: The Red LED is OFF, if the user button is pressed and held for 2 secs.

5.Wipers returns back to their initial position even though they stuck in the middle position.
## REQUIREMENTS FOR THE PROJECT
## STM32Cube IDE

*   STM32Cube software ecosystem. STM32CubeIDE is an advanced C/C++ development platform with peripheral configuration, code generation, code compilation, and debug features for STM32 microcontrollers and microprocessors. It is based on the Eclipse®/CDT™ framework and GCC toolchain for the development, and GDB for the debugging. It allows the integration of the hundreds of existing plugins that complete the features of the Eclipse® IDE

## Xpack Packages

## * Windows Build Tools

 The xPack Windows Build Tools is a standalone Windows binary distribution of GNU make and a few of other tools required by the Eclipse Embedded CDT (formerly GNU MCU/ARM Eclipse) project, but the binaries can also be used in generic build environments.

## * OpenOCD

 Open On-Chip Debugger (OpenOCD) is a free, open-source project that aims to provide debugging, in-system programming, and boundary scan using a debug adapter. The adapter is a hardware module that provides the right signals for the target to understand.

## * QEMU

The xPack QEMU Arm is a standalone cross-platform binary distribution of QEMU, with several extensions for Arm Cortex-M devices.

## COMPONENTS USED IN PROJECT
# Exploring STM32F407 Discovery Board

STM32F407 series of microcontrollers are high-performance MCUs designed for medical, industrial and consumer applications. It is based on ARM Cortex-M4 and offers up to 168MHz. The STM32F407VGT6 is the onboard chip which comes in a 100-pin LQFP package.

 Figure 1 : STM32F407 Discovery Board

![STM32]<img width="403" alt="Figure_1_STM32F4DISCOVERY" src="https://user-images.githubusercontent.com/83355817/168411412-d6b30ca1-5213-4a68-b245-77b6d96e7f54.png">


The STM32F407G-DISC1 is a Discovery Kit allows users to easily develop applications with the STM32F407 high performance microcontrollers with ARM cortex-M4 32-bit core. It includes everything required either for beginners or for experienced users to get quickly started. Based on the STM32F407VGT6, it includes an ST-LINK/V2 or ST-LINK/V2-A embedded debug tool, two ST MEMS digital accelerometers, a digital microphone, one audio DAC with integrated class D speaker driver, LEDs and push buttons and an USB OTG micro-AB connector.

## Features Of STM32F407G

*   Flash memory of up to 1 megabyte.
*   OTP memory of 512 bytes.
*   Compact Flash, SRAM, PSRAM, NOR, and NAND memories are supported by this flexible static memory controller.
*   Sleep, Stop, and Standby modes are low-power modes.
*   16-stream DMA controller with FIFOs and burst support for general-purpose DMA.
*   Up to 54 Mbytes/s 8- to 14-bit parallel camera interface.
*   Generator of true random numbers.
*   Hardware calendar, CRC calculating unit, 96-bit unique ID RTC, subsecond accuracy.  
 ## Overview of STM32F407VGT6 Microcontroller
**Figure 2. STM32F407VGT6 block diagram from 'STM32F4 Discovery User Manual' (Page 12).**

<img src = "Images/Figure_6_STM32F407VGT6_block_diagram.png" width="750" height="950" hspace="30">

The STM32F407 Discovery board uses STM32F407VGT6 Microcontroller which has **ARM Cortex-M4F** Processor, which is capable of running upto **168Mhz**. This MCU has many peripherals such as GPIO ports, TIMERS, ADCs, DACs, Flash Memory, SRAM, SPI, UART ect. The processor and peripherals talk via **BUS-Interface**.  There are three busses available :-
1. **I-BUS** (Instruction Bus)   
2. **D-BUS** (Data Bus)
3. **S-BUS** (System Bus)

**I-BUS**
This bus connects the Instruction bus of the Cortex®-M4 with FPU(Floating point unit) core to the BusMatrix. This bus is used by the core to fetch instructions. The target of this bus is a memory containing code (internal Flash memory/SRAM or external memories through the FSMC/FMC).

**D-BUS**
This bus connects the databus of the Cortex®-M4 with FPU to the 64-Kbyte CCM data RAM to the BusMatrix. This bus is used by the core for literal load and debug access. The target of this bus is a memory containing code or data (internal Flash memory or external memories through the FSMC/FMC).

**S-BUS**
This bus connects the system bus of the Cortex®-M4 with FPU core to a BusMatrix. This bus is used to access data located in a peripheral or in SRAM. Instructions may also be fetched on this bus (less efficient than ICode). The targets of this bus are the internal SRAM1, SRAM2 and SRAM3, the AHB1 peripherals including the APB peripherals, the AHB2 peripherals and the external memories through the FSMC/FMC.

So instructions and data use I-bus and D-bus respectively, All the other peripheral uses System bus. The Cortex-M4 processor contains three external Advanced High-performance Bus (AHB)-Lite bus interface and one Advanced Peripheral Bus (APB) interface. The GPIOs are connected to AHB1 bus which has a maximum speed of 150Mhz and is divided into two buses as APB1 and APB2. APB1 runs at 42Mhz(max) and APB2 runs at 82Mhz(max). The different peripherals such as SPI, UART, TIMERs, ADCs, DACs, etc are connected to either APB1/APB2 buses. And the AHB2(168Mhz max) is connected to Camera and USB OTG interfaces, AHB3 is connected to External memory controller.
## REQUIREMENTS

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


                             

