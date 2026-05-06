# Self-Balancing-Robotic-Desk-Assistant-Scoot-Mk.-1-

A collection of files, code, and images involved in the development of Scoot Mk. 1.

# Overview
Scoot Mk.1 is a small self-balancing robotic desk assistant designed to be a companion for the user as they study or do work. Using buttons on the outside of its frame, the user can also use Scoot as a Pomodoro timer, helping with the user's productivity needs.

# Electronics Description
To develop the electronics for Scoot, I used the CAD tool KiCad to develop the schematic and footprint of the custom PCB. In this PCB, I used an STM32F411 microcontroller due to its high performance compared to the Arduino family of microcontrollers and its 512 KBytes of flash memory, giving me the plenty of space to write code and eliminating the need for external flash memory on the board. Peripherals are a USB-C 2.0 receptacle, ESD protection diode array, motor drivers, battery charger, LED display, accelerometer and gyroscope, an LDO, and 2 N20 motors with magnetic encoders. When making the footprint of the board, I used design techniques such as copper pours and via stitching to reduce the inductance and EMI of the board by reducing the current return loop area. I also made sure to minimize the distance of the USB D- and D+ differential pair and placed decoupling capacitors for every power pin of each IC as close as possible. I also used different trace widths for signal and power pins as thicker traces are needed for the amperage demands for power pins; I used 0.200 mm tracks for signal pins and 0.400 mm tracks for power pins.

# Frame and Software
I am currently in the process of creating the frame of Scoot and the code for Scoot. For the frame, I will use Autodesk Fusion360, and for the code, I plan to use a combination of STM32Cube IDE and Arduino IDE. STM32Cube IDE will allow me to interact directly with the microcontroller to assign pin functions. I will use the Arduino IDE to create the PID algorithm for self-balancing and the Pomodoro timer firmware.

# Future Iterations
- Replace Arduino IDE with C or C++ as programming knowledge expands
- Integrate obstacle-avoidance capabilities
