# LED Controller Code v1.0

This is a Python-based LED controller project designed to be used with Raspberry Pi Pico W, WS2812 LED strip, EC11 Encoder and Potentiometer.

## Hardware Requirements

- Raspberry Pi Pico W
- WS2812 LED strip
- EC11 Encoder
- Potentiometer

## Code Overview

The code consists of several parts:

1. **Importing necessary libraries** - Various libraries are imported that provide necessary functionalities such as controlling the GPIOs, manipulating time, handling mathematical operations etc.

2. **Definition of Constants and Global Variables** - The script defines several constants and global variables used throughout the code. Constants include the number of LEDs in the strip, maximum brightness, frames per second, and the input pins. The global variables keep track of the current state of the program such as current pattern, brightness level, encoder position, etc.

3. **Interrupts and Handlers** - An interrupt is set on the encoder button, and its corresponding handler `button_press()` handles the transitions between different menu modes.

4. **Menu Management Functions** - Functions such as `update_menu_values()`, `poll_encoder()`, and `enter_menu()` are used to update menu values, poll the encoder for its current value, and manage the menu system respectively.

5. **LED Animation Functions** - Functions such as `rainbow()`, `breathing()`, and `transition()` define different LED strip animations.

6. **Helper Functions** - Various helper functions are used to handle the color scales, color transitions and switching between patterns.

7. **Main Program Loop Control** - The `loop()` function is where the main program logic lies. It continually executes the currently selected LED pattern and updates the LEDs accordingly. 

## How to Run

Copy the code into a Python file (`.py`), and execute the script while connected to the appropriate hardware as described above.

Please ensure you have all the necessary libraries installed in your Python environment. The required libraries are `machine`, `time`, `neopixel`, `urandom` and `math`.

