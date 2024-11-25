# Temperature PID control using STM32F446
> This project consists on creatig [proportional–integral–derivative controller](https://en.wikipedia.org/wiki/Proportional–integral–derivative_controller) (PID controller or three-term controller) control using [STM32_F446](https://www.st.com/en/microcontrollers-microprocessors/stm32f446.html).

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Working principles](#working-principles)
* [Video](#video)
* [Project Status](#project-status)
* [Contact](#contact)
<!-- [Acknowledgements](#acknowledgements) -->

## General Information
- This project is based on a work for school.
- The names of the variables and comments were written in portuguese.
- It's used a PID control Lib for STM32F446RE PID calculations. 

## Technologies Used
- C 
- STM NUCLEO F446RE
- Zero-crossing detector 
- TRIAC trigger circuit 

## Working principles
The system is composed of two parts. The first is the software, which calculates the PID output to activate a TRIAC that cuts the sinusoidal voltage of the power grid. The program can be modified to set a different temperature, but we must know the voltage value for the desired temperature. Once that information is clear, you can change the value in Core/Src/main.:

<code double TempDesejada = VALUE OF VOLTAGE REQUIRED FOR THE TEMPERATURE.00 </code>


In the thermal chamber, there are two NTC temperature sensors and a 33/10W ohm resistor inside. One of the NTC sensors is used to display the temperature on the thermal chamber's display, while the other is used to acquire the current voltage (temperature) of the thermal chamber, which is connected to the PA0 pin.
The PA1 pin of the microcontroller generates a PWM signal, which increases in width if the current voltage (temperature) is lower than the desired value, and decreases when it is higher. This value is changed acocrdingly to the PID calculated value. 
After that, you can adjust the PID coefficients if desired.
The power circuit was designed using a zero-crossing detector to synchronize with the power grid, and a TRIAC trigger circuit to activate the power grid sinusoid, allowing current to flow through the resistor and consequently heating the thermal chamber.

## Video
![System in action](https://img.youtube.com/vi/VGLLtkI0vu0/maxresdefault.jpg)
[Watch the system in action on YouTube](https://youtu.be/VGLLtkI0vu0)

## Project Status
Finished

## Contact
Created by [vituzm](https://github.com/vituzm) - feel free to contact!

