# stm32-baremetal-uart-timer
STM32 bare-metal project demonstrating asynchronous UART, EXTI, and hardware timers without HAL or RTOS.

This repository contains my educational project focused on deep hardware-level programming of STM32 microcontrollers. I deliberately abandoned the HAL (Hardware Abstraction Layer) library to program entirely on **bare-metal registers** in Embedded C.

The program features 3 main functions:
1. The onboard green LED blinks continuously every 500 ms (1 Hz) using a hardware timer (TIM2).
2. When the B1 user button is pressed, the system triggers an interrupt, toggles the LED, and instantly sends the character 'X' to the computer via UART.
3. When a user sends a letter via a serial terminal (e.g., 'A'), the microcontroller receives it and instantly returns the opposite case ('a'). It automatically converts uppercase to lowercase and vice versa.
<img width="194" height="346" alt="Adobe Express - IMG_5751" src="https://github.com/user-attachments/assets/f3c079dc-6265-4073-a75f-bea3a0348fda" />
Technologies & Hardware
* **Microcontroller:** STM32 Nucleo-64 (NUCLEO-L073RZ)
* **Language:** C (Bare-metal / Register level)
* **IDE:** STM32CubeIDE

Serial Terminal Configuration
To test the communication, use a terminal program like PuTTY or TeraTerm with the following settings:
* **Baud Rate:** 115200 
* **Data bits:** 8
* **Stop bits:** 1
* **Flow control:** None
