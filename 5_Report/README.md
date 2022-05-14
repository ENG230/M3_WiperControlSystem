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

## STM32F407G-DISC1 Board
![STM32F4](https://user-images.githubusercontent.com/83355817/168411330-da3d634c-1e25-4e63-a443-2ef314843b72.png)


STM32F407 series of microcontrollers are high-performance MCUs designed for medical, industrial and consumer applications. It is based on ARM Cortex-M4 and offers up to 168MHz. The STM32F407VGT6 is the onboard chip which comes in a 100-pin LQFP package.

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


