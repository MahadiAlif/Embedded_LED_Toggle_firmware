# LED Blinking on STM32F427IIH6 Microcontroller

This project demonstrates how to blink LEDs using the STM32F427IIH6 microcontroller. The project is set up using STM32CubeMX for peripheral configuration and STM32CubeIDE for coding and building.

## Project Overview

The goal of this project is to configure the GPIOs of the STM32F427IIH6 microcontroller to toggle an LED. This serves as a foundational project to get familiar with the STM32F4 series and embedded systems development.

## Features

- **Microcontroller**: STM32F427IIH6
- **IDE**: STM32CubeIDE
- **Peripherals**: GPIO (General Purpose Input/Output)
- **Tool**: STM32CubeMX for peripheral initialization

## Hardware Requirements

- **Microcontroller**: STM32F427IIH6-based development board
- **One or more LEDs**
- Resistors (typically 220 ohms)
- Breadboard and jumper wires (if needed)

## Software Requirements

- [STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html)
- [STM32CubeMX](https://www.st.com/en/development-tools/stm32cubemx.html)

## Project Setup

1. **STM32CubeMX Configuration**:
   - Configure the GPIO pin connected to the LED as an output.
   - Enable the system clock and other necessary peripherals.
   - Generate the initialization code for STM32CubeIDE for the STM32F427IIH6.

2. **STM32CubeIDE**:
   - Open the project in STM32CubeIDE.
   - Write the code to toggle the LED in the `main.c` file using HAL (Hardware Abstraction Layer) functions.
   - Build and flash the code to the STM32F427IIH6 microcontroller.

## Code Explanation

The main code for toggling the LED is written in `Core/Src/main.c`:

```c
while (1)
{
    HAL_GPIO_TogglePin(GPIOx, GPIO_PIN_x);  // Replace GPIOx and GPIO_PIN_x with your specific configuration
    HAL_Delay(500);  // Delay in milliseconds
}
