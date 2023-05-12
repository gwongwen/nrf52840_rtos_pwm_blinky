# Second Zephyr RTOS Project - PWM Blinky Application

## Overview

This application blinks the green LED using PWM API.

The LED starts blinking at a 1 Hz frequency. The frequency doubles every 4 seconds until it reaches 128 Hz. The frequency will then be halved every 4 seconds until it returns to 1 Hz, completing a single blinking cycle. This faster-then-slower blinking cycle then repeats forever.

Some PWM hardware cannot set the PWM period to 1 second to achieve the blinking frequency of 1 Hz. This sample calibrates itself to what the hardware supports at startup. The maximum PWM period is decreased appropriately until a value supported by the hardware is found.

**Board used** : Makediary nRF52840-MDK