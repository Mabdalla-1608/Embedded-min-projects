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
* ST-LINK debugger/programmer
* Logic analyzer (optional)
* Oscilloscope (optional)

## Repository Structure

```text
.
├── projects/
│   ├── gpio_blink/
│   ├── uart_echo/
│   ├── timer_interrupts/
│   ├── spi_driver/
│   └── ...
│
├── drivers/
│   ├── gpio/
│   ├── uart/
│   ├── spi/
│   └── ...
│
├── docs/
│   ├── notes/
│   ├── diagrams/
│   └── references/
│
└── README.md
```

## Experiments and Projects

| Project          | Description                   | Status |
| ---------------- | ----------------------------- | ------ |
| GPIO Blink       | Basic LED control             | ✅      |
| UART Echo        | Serial communication testing  | ✅      |
| Timer Interrupts | Periodic task execution       | 🚧     |
| SPI Driver       | Custom SPI interface          | 🚧     |
| Low Power Modes  | Sleep and wake-up experiments | 📋     |

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
