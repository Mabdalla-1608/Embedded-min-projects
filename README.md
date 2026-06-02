# STM32L432KC Embedded Systems Exploration

A collection of embedded systems experiments, drivers, and projects built using the STM32L432KC Nucleo development board.

This repository serves as a hands-on learning environment for exploring low-level embedded programming concepts, STM32 peripherals, hardware interfaces, and real-time system design.

## Goals

This project is focused on developing practical experience with:

* Bare-metal embedded programming
* STM32 peripheral configuration
* GPIO, timers, interrupts, and DMA
* UART, SPI, I2C, and other communication protocols
* Power management and low-power modes
* Sensor integration
* RTOS concepts and task scheduling
* Debugging and performance analysis

## Hardware

### Development Board

* STM32L432KC Nucleo-32
* ARM Cortex-M4 core
* 80 MHz maximum clock frequency
* Low-power STM32L4 series MCU

### Tools

* STM32CubeIDE
* STM32CubeMX
<!--
* ST-LINK debugger/programmer 
-->
<!--
* Logic analyzer (optional)
-->
<!-- 
* Oscilloscope (optional)
-->


## Repository Structure

```text
Embedded-min-projects/
├── Project1_Blinky/
│   ├── Core/
│   │   ├── Inc/
│   │   ├── Src/
│   │   └── Startup/
│   ├── Project1_Blinky.ioc
│   └── STM32L432KCUX_FLASH.ld
│
├── Project2_UART_Hello_World/
│   ├── Core/
│   │   ├── Inc/
│   │   ├── Src/
│   │   └── Startup/
│   ├── Project2_UART_Hello_World.ioc
│   └── STM32L432KCUX_FLASH.ld
│
└── Project3_Motor_Control/
    ├── Core/
    │   ├── Inc/
    │   ├── Src/
    │   └── Startup/
    ├── Project3_Motor_Control.ioc
    └── STM32L432KCUX_FLASH.ld
```
<!--
│
├── Project4_Motor_Speed_Simple/
│   ├── Core/
│   ├── Project4_Motor_Speed_Simple.ioc
│   └── STM32L432KCUX_FLASH.ld
│
└── Project5_Motor_Speed_Joystick/
    ├── Core/
    ├── Project5_Motor_Speed_Joystick.ioc
    └── STM32L432KCUX_FLASH.ld
-->


### Key Files

* `Core/Inc` – Application header files
* `Core/Src` – Application source files
* `Core/Startup` – MCU startup code and interrupt vectors
* `.ioc` – STM32CubeMX project configuration
* `.ld` – Linker script for STM32L432KC flash memory layout

### Projects 

| Project                       | Description                                 | Status |
| ----------------------------- | ------------------------------------------- | ------ |
| Project1_Blinky               | GPIO configuration and LED blinking         |✅      |
| Project2_UART_Hello_World     | UART communication and serial output        |✅      |
| Project3_Motor_Control        | Basic motor control using STM32 peripherals |✅      |
| Project4_Motor_Speed_Simple   | PWM-based motor speed control               |🚧      |
| Project5_Motor_Speed_Joystick | ADC joystick input controlling motor speed  |🚧      |

```
```

## Getting Started

### Prerequisites

* STM32CubeIDE installed
* ST-LINK drivers installed
* STM32L432KC Nucleo board connected via USB

### Build

Open the desired project in STM32CubeIDE and build using:

```bash
Project → Build Project
```

### Flash

Connect the board and use:

```bash
Run → Debug
```

or

```bash
Run → Run
```

to program the device through ST-LINK.

## Learning Notes

This repository is intentionally structured as a learning project. Code quality, architecture, and implementations may evolve as new concepts are explored and better approaches are discovered.

Key takeaways, references, and design decisions are documented throughout the repository.

## References

* STM32L432KC Datasheet
* STM32L4 Reference Manual
* STM32Cube HAL Documentation
* ARM Cortex-M4 Technical Reference Manual

## Future Work

* [ ] Custom HAL-free peripheral drivers
* [ ] DMA-based communication
* [ ] FreeRTOS integration
* [ ] Sensor interfacing
* [ ] Bootloader experiments
* [ ] Power optimization measurements
* [ ] Unit testing embedded code

## License

This repository is provided for educational purposes and personal experimentation.
