## Introduction 

The main purpose of the wiper Control system is to clean the windscreen sufficiently to provide suitable visibility at all times.
Rainwater, dust and exhaust gas chemicals from vehicles that stick to the surface of an automobile windshield are probably not an issue as long as the driver has an unobstructed view of the road. However, if the sticking substances are left unchecked, they will become a threat for travel safety.

A windshield wiper control system comprises a wiper drive and two wiper arms. The drive moves the two wiper arms at a certain angle across the windshield, providing a clear view for the driver and passenger. A specially-shaped rubber wiping lip ensures an optimal wiping result

Wipers are vital for driver visibility. The vehicle is considered unsafe if the wipers don't work. The front wiper motor and the wiper transmission mechanism (linkage) are installed below the windshield, under the cowl panel cover.

Here we implemented Wiper Control System using STM32F4Discovery Board.


## Features

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

(<img width="403" alt="Figure_1_STM32F4DISCOVERY" src="https://user-images.githubusercontent.com/83355817/168411412-d6b30ca1-5213-4a68-b245-77b6d96e7f54.png">)


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
**Figure 2. STM32F407VGT6 block diagram from 'STM32F4 Discovery User Manual'.**

![Figure_6_STM32F407VGT6_block_diagram](https://user-images.githubusercontent.com/83355817/168411665-fd3e4d17-1712-4739-8f19-8ef78d301c07.png)


The STM32F407 Discovery board uses STM32F407VGT6 Microcontroller which has **ARM Cortex-M4F** Processor, which is capable of running upto **168Mhz**. This MCU has many peripherals such as GPIO ports, TIMERS, ADCs, DACs, Flash Memory, SRAM, SPI, UART ect. The processor and peripherals talk via **BUS-Interface**.  There are three busses available :
1. I-BUS (Instruction Bus)   
2. D-BUS (Data Bus)
3. S-BUS (System Bus)

 The Cortex-M4 processor contains three external Advanced High-performance Bus (AHB)-Lite bus interface and one Advanced Peripheral Bus (APB) interface. The GPIOs are connected to AHB1 bus which has a maximum speed of 150Mhz and is divided into two buses as APB1 and APB2. APB1 runs at 42Mhz(max) and APB2 runs at 82Mhz(max). The different peripherals such as SPI, UART, TIMERs, ADCs, DACs, etc are connected to either APB1/APB2 buses. And the AHB2(168Mhz max) is connected to Camera and USB OTG interfaces, AHB3 is connected to External memory controller.
## Tools Used for Implementation

## Preprocessor
The C preprocessor is a macro processor that is used automatically by the C compiler to transform your program before actual compilation. It is called a macro processor because it allows you to define macros, which are brief abbreviations for longer constructs.

## The C preprocessor provides four separate facilities that you can use as you see fit

Inclusion of header files. These are files of declarations that can be substituted into your program. Macro expansion. You can define macros, which are abbreviations for arbitrary fragments of C code, and then the C preprocessor will replace the macros with their definitions throughout the program. Conditional compilation. Using special preprocessing directives, you can include or exclude parts of the program according to various conditions. Line control. If you use a program to combine or rearrange source files into an intermediate file which is then compiled, you can use line control to inform the compiler of where each source line originally came from.

## Pointers

The Pointer in C, is a variable that stores address of another variable. A pointer can also be used to refer to another pointer function. A pointer can be incremented/decremented, i.e., to point to the next/ previous memory location. The purpose of pointer is to save memory space and achieve faster execution time. Like variables, pointers in C programming have to be declared before they can be used in your program. Pointers can be named anything you want as long as they obey C’s naming rules. A pointer declaration has the following form.

syntax: data_type * pointer_variable_name;

Types of Pointers in C: 1.Null Pointer 2.Void Pointer 3.Wild pointer 4.Dangling pointer

## Funtion Pointer

In the C function pointer is used to resolve the run time-binding. A function pointer is a pointer that stores the address of the function and invokes the function whenever required. In C, we can use function pointers to avoid code redundancy.

Unlike normal pointers, a function pointer points to code, not data. Typically a function pointer stores the start of executable code.
Unlike normal pointers, we do not allocate de-allocate memory using function pointers.

## Struct

A structure is a key word that create user defined data type in C. A structure creates a data type that can be used to group items of possibly different types into a single type.

‘struct’ keyword is used to create a structure.

A structure variable can either be declared with structure declaration or as a separate declaration like basic types.Structure members cannot be initialized with declaration.

Structure members can be initialized using curly braces ‘{}’. For example, following is a valid initialization. Structure members are accessed using dot (.) operator.

## Type def

typedef, which you can use to give a type a new name. Following is an example to define a term BYTE for one-byte numbers.After this type definition, the identifier BYTE can be used as an abbreviation for the type unsigned char

By convention, uppercase letters are used for these definitions to remind the user that the type name is really a symbolic abbreviation, but you can use lowercase.

You can use typedef to give a name to your user defined data types as well. For example, you can use typedef with structure to define a new data type and then use that data type to define structure variables directly

Syntax: typedef data_type new_name

# 4W'S & 1H
## What
 Wiper control system is used to remove rain and debris from a windscreen.

## Why
 It is used To clean the windscreen sufficiently to provide suitable visibility at all times.
## When
The windshield wipers eliminate downpour and snow from the windshield, while the headlights further develop perceivability around evening time.

## Who
Anyone who wishes to be safe and have clear visibility in bad weather.
## How
You can adjust the speed of the car wiper system  by altering the frequency according to the rainfall.
# SWOT Analysis

## Strenghts

 ➨ Passive safety system in vehicles because it only works when needed.
 
 ➨ High sensitivity
 
 ➨Proides clear visibility for drivers.
## Weakness
 ➨No Focus on Private Sector
 
 ➨ Week Focus on Process Innovations.
## Opportunities
 ➨Technological Development
 
 ➨Demand for Saver Equipments.
## Threats
 ➨Highly regulated Industry
 
 ➨Low Bargaining Power Buyers.
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

# BLOCK DIAGRAM
![BLOCK DIAGRAM (1)](https://user-images.githubusercontent.com/101693748/168218547-ca8edd38-6903-4d8d-b4fa-720618b8a066.png)
# FLOWCHART
![FLOWCHART 1](https://user-images.githubusercontent.com/101693748/168218561-281382d5-fa0a-484a-9d82-029d19521a35.png)



                             
## OUTPUT IMAGES WHEN THE WIPER IS IN ON, LOW, MODERATE, HIGH, OFF STATES

<br  />

## ON STATE

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

## OFF STATE

<bs  />

![OFF STATE](https://user-images.githubusercontent.com/89642370/168282238-96d3f26d-fe85-459f-b519-685b63c1084f.png)
