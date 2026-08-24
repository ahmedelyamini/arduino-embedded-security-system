# Arduino Embedded Security System

Embedded security and alarm prototype developed with **Arduino Uno**, combining motion detection, password-based control, user interaction and real-time alarm management.

## Project Overview

This project demonstrates the design and implementation of a small embedded security system using sensors, actuators and a microcontroller.

The system can be armed by the user, monitor movement through a **PIR sensor**, trigger an audible alarm when motion is detected and require a password to deactivate the alarm.

A **4x4 keypad** provides user input while a **16x2 LCD** displays system status and instructions.

> This project is an educational embedded-systems prototype and is not intended to replace a certified commercial security system.

## Main Features

- Alarm activation from the keypad
- Motion detection using a PIR sensor
- Audible alert using a buzzer
- Password-protected alarm deactivation
- Password modification through the keypad
- LCD-based user interface
- Visual activation countdown
- Embedded real-time control using Arduino

## Hardware

| Component | Purpose |
|---|---|
| Arduino Uno | Main embedded controller |
| PIR sensor | Motion detection |
| 16x2 LCD | User interface and system messages |
| 4x4 keypad | Password and command input |
| Buzzer | Audible alarm |
| Breadboard | Electronic prototyping |
| Jumper wires | Electrical connections |

## System Architecture

```text
              +----------------+
              |   PIR Sensor   |
              +-------+--------+
                      |
                      v
+----------+    +-------------+    +-----------+
| Keypad   | -> | Arduino Uno | -> |  Buzzer   |
|  4x4     |    |             |    |   Alarm   |
+----------+    +------+------+    +-----------+
                      |
                      v
                +-----------+
                | LCD 16x2  |
                +-----------+
```

The Arduino acts as the central controller and coordinates sensor acquisition, alarm logic, password management and the user interface.

## Operating Logic

### 1. Idle State

The LCD provides access to the main actions:

- Activate the alarm
- Change the password

### 2. Alarm Activation

When activation is requested, the system displays a countdown before entering monitoring mode.

### 3. Motion Monitoring

Once armed, the Arduino continuously reads the PIR sensor.

If movement is detected:

- The buzzer is activated
- The LCD displays an alarm message
- The system requests the password

### 4. Authentication

The user enters the password using the keypad.

If the password is correct, the alarm is disabled and the system returns to its normal state.

### 5. Password Management

The software also provides a password-change mode.

The current password must first be validated before a new password can be entered.

## Pin Configuration

### PIR Sensor

| PIR | Arduino |
|---|---|
| VCC | 5V |
| GND | GND |
| OUT | Pin 10 |

### Buzzer

| Buzzer | Arduino |
|---|---|
| + | Pin 11 |
| - | GND |

### LCD 16x2

| LCD | Arduino |
|---|---|
| RS | A0 |
| E | A1 |
| D4 | A2 |
| D5 | A3 |
| D6 | A4 |
| D7 | A5 |

### Keypad 4x4

| Interface | Arduino Pins |
|---|---|
| Rows | 9, 8, 7, 6 |
| Columns | 5, 4, 3, 2 |

## Software

The embedded application is implemented in **Arduino C/C++**.

Main libraries:

```text
LiquidCrystal
Keypad
```

The program handles:

- Digital sensor acquisition
- Alarm state management
- Keypad input
- Password verification
- Password modification
- LCD interface management
- Buzzer control

## Repository Structure

```text
arduino-embedded-security-system/
├── pfe.ino
├── README.md
├── License
└── mimoire de fin d'etudes - Réalisation d'un système de sécurité et d'alarme.pdf
```

## Running the Project

1. Install the Arduino IDE.
2. Connect the Arduino Uno to the computer.
3. Install or verify the required `Keypad` and `LiquidCrystal` libraries.
4. Open `pfe.ino`.
5. Connect the components according to the pin configuration.
6. Compile and upload the program to the Arduino Uno.

## Engineering Skills Demonstrated

This project demonstrates practical experience with:

- Embedded systems
- Arduino programming
- C/C++
- Sensor integration
- Actuator control
- Human-machine interfaces
- State-based control logic
- Digital electronics
- Hardware/software integration

## Possible Improvements

Potential extensions include:

- ESP32-based Wi-Fi connectivity
- MQTT communication
- Mobile or web monitoring
- GSM/SMS notifications
- Event logging
- Camera integration
- Multiple sensor zones
- Persistent configuration storage
- Improved authentication mechanisms

## Author

**Ahmed EL YAMINI**  
Aeronautical Engineering & Space Technologies