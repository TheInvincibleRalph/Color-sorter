# Color Sorter Project

This repository contains the code for a **color sorting machine** built using C++ for an embedded system. The project aims to detect colors using a sensor, control a motor system, and sort objects based on their color.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Hardware Requirements](#hardware-requirements)
4. [Software Requirements](#software-requirements)
5. [Installation and Setup](#installation-and-setup)
6. [Usage](#usage)
7. [Contributing](#contributing)


## Project Overview:

The **Color Sorter Project** is designed to identify and sort objects based on their color. This system utilizes a color sensor, motors, and an embedded controller (e.g., Arduino, STM32, or similar microcontroller) to automate the sorting process.

Objects are placed in a conveyor belt mechanism, and the color sensor identifies the object's color. Based on the detected color, the object is sorted into predefined bins.

## Features

- **Color Detection**: Uses a color sensor to accurately detect the color of objects.
- **Motor Control**: Controls servos/motors to sort objects based on their detected color.
- **Embedded System Implementation**: Written in C++ for efficiency and real-time performance.
- **Extensible**: Easy to add new colors and sorting rules.

## Hardware Requirements

To build the full system, you'll need the following hardware components:

- **Microcontroller** (e.g., Arduino, STM32, or similar)
- **Color Sensor** (e.g., TCS3200/TCS34725)
- **Servo Motors** for sorting mechanism
- **Conveyor Belt** (optional, but recommended for automated sorting)
- **Power Supply**
- Jumper wires, resistors, and other common electronic components

## Software Requirements

- C++ Compiler (e.g., GCC, or Arduino IDE if using Arduino)
- [Visual Studio Code](https://code.visualstudio.com/) with the C/C++ extension (if developing in VS Code)
- Arduino IDE (optional, for Arduino-based development)
- Additional libraries for specific components (e.g., color sensor libraries)

## Installation and Setup

### 1. Clone the Repository

To get started, clone this repository to your local machine:

```bash
git clone https://github.com/TheInvincibleRalph/Color-sorter.git
```

### 2. Install Dependencies

Make sure you have the necessary libraries for your microcontroller platform installed. For example, if you're using Arduino:

1. Open the Arduino IDE.
2. Go to **Sketch** -> **Include Library** -> **Manage Libraries...**
3. Search for and install any required libraries, such as:
   - TCS3200/TCS34725 Color Sensor libraries
   - Servo Motor libraries (if needed)

### 3. Configure Include Paths

If you are using VS Code and encountering issues with include paths, ensure that your `c_cpp_properties.json` is configured correctly. Refer to the following snippet for guidance:

```json
{
  "configurations": [
    {
      "name": "Win32",
      "includePath": [
        "${workspaceFolder}/**",
        "C:/path_to_your_libraries/include"
      ],
      "defines": [],
      "compilerPath": "C:/path_to_your_compiler/gcc.exe",
      "cStandard": "c11",
      "cppStandard": "c++17",
      "intelliSenseMode": "gcc-x64"
    }
  ],
  "version": 4
}
```

### 4. Build and Upload the Code

If using the Arduino IDE:
1. Open the `.ino` or `.cpp` file.
2. Connect your microcontroller to the computer.
3. Select the correct board and port under **Tools**.
4. Compile and upload the code to the microcontroller.

For non-Arduino platforms, follow the relevant build and upload procedure for your board.

## Usage

Once the code is uploaded, the system will automatically begin detecting and sorting objects based on color.

1. Place an object in front of the color sensor.
2. The color sensor will detect the color of the object.
3. The system will move the object to the corresponding bin using the motor/servo system.

### Example

In the current setup, the system can detect the following colors:

- Red
- Green
- Blue
- White

You can modify the color detection thresholds and motor control logic by editing the respective sections in the code.


## Contributing

Contributions are welcome! If you have any suggestions, bug reports, or feature requests, please open an issue or submit a pull request.

### Steps to Contribute

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

