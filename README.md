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
- It's used a PID control Lib for STM32F446RE. 
- The thermal chamber has two NTC Temperature Sensors and a 33/10W ohms resistor inside.

## Technologies Used
- C 
- STM NUCLEO F446RE
- Zero detector

## Working principles
The system is composed of two parts. The first is the software, which calculates the PID output to activate a TRIAC that cuts the sinusoidal voltage of the power grid. The program can be modified to set a different temperature, but we must know the voltage value for the desired temperature. Once that information is clear, you can change the value in:

``

After that, you can adjust the PID coefficients if desired.
The power circuit was designed using a zero-crossing detector to synchronize with the power grid, and a TRIAC trigger circuit to activate the power grid sinusoid, allowing current to flow through the resistor and consequently heating the thermal chamber.

## Project Status
Finished

## Video
![System in action](https://img.youtube.com/vi/VGLLtkI0vu0/maxresdefault.jpg)
[Watch the system in action on YouTube](https://youtu.be/VGLLtkI0vu0)


## Contact
Created by [vituzm](https://github.com/vituzm) - feel free to contact!

