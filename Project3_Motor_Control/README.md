# Project 3: Motor Control (GPIO + UART + L293D H-Bridge Experimentation)

This project demonstrates DC motor control using an STM32L432KC Nucleo board. It combines GPIO control, UART serial communication, and H-bridge motor driver logic to control motor direction, enable/disable behavior, and observe braking vs coasting behavior.

A key part of this project was experimenting with the **L293D motor driver** to understand how it behaves during motor shutdown conditions as described in its datasheet and **test the coasting vs braking behaviour**.

---

## 🧠 Overview

The firmware cycles through a sequence of motor states:

1. Motor rotates clockwise (CW)
2. Motor stops
3. Motor rotates counter-clockwise (CCW)
4. Motor disabled via enable pin
5. Repeat loop

Each state transition is logged over UART at 115200 baud.

This project also explores how the motor behaves under different L293D input conditions, particularly whether it coasts or brakes when stopping.

---

## ⚙️ Features

- GPIO control of L293D motor driver inputs
- Enable pin control for motor shutdown behavior testing
- Direction control (CW / CCW)
- UART debug output via USART2
- LED status indicator
- Timing-based state sequencing using HAL_Delay

---

## 🔌 Hardware Setup

This project uses an STM32L432KC Nucleo board connected to a DC motor through an **L293D H-bridge motor driver**.

The goal of this setup was not only to control motor direction, but also to observe and validate **motor stop behavior (braking vs coasting)** based on L293D datasheet characteristics.

According to the L293D documentation, motor shutdown behavior depends on input states:

- **Coast (free run)**: motor gradually slows down due to inertia
- **Brake (fast stop)**: motor terminals are effectively shorted internally, stopping rotation quickly

This project was used to experimentally observe these behaviors by toggling:
- Enable pin (EN)
- Input pins (IN1 / IN2)

---

## 📌 STM32 Pin Mapping

| STM32 Pin | Function | Connected To |
|------------|----------|--------------|
| LD3 (GPIOB) | Onboard LED | Status indicator |
| EN_3_4_Pin | Motor Enable | L293D EN pin |
| pin_3A_Pin | Motor Input A | L293D IN1 |
| pin_4A_Pin | Motor Input B | L293D IN2 |
| USART2 TX/RX | UART Debug | Serial monitor |

---

## 🔄 Motor Control Logic

| EN | IN1 (3A) | IN2 (4A) | Behavior |
|----|----------|----------|----------|
| 1  | 1        | 0        | Clockwise rotation |
| 1  | 0        | 1        | Counter-clockwise rotation |
| 1  | 0        | 0        | Brake or coast (depends on L293D behavior + load) |
| 0  | X        | X        | Motor disabled (high impedance / coast) |

> Note: Actual stopping behavior depends on motor load, supply conditions, and internal transistor states of the L293D.

---

## 📡 UART Output Example
Motor ON CW

Motor will now turn OFF

Motor OFF

Motor ON CCW

Motor will now turn OFF

Motor OFF by disabling EN

## 🖼️ Circuit Diagram


```markdown
![Project 3 Circuit](docs/images/Full_circuit.jpg)
```