# Wi-Fi Controlled Car using ESP8266 NodeMCU

This project demonstrates how to build a Wi-Fi controlled car using the ESP8266 NodeMCU microcontroller, L298N motor driver, two 3.6V DC motors, and a mobile application for control. The project involves setting up a webpage to control the movement of the car via a Wi-Fi network.

## Project Components

- **ESP8266 NodeMCU**: Acts as the microcontroller to receive commands from the mobile device via Wi-Fi.
- **L298N Motor Driver**: Controls the direction and speed of the DC motors.
- **DC Motors (2x 3.6V)**: Used to drive the car's movement.
- **Rear Wheels (2x)**: Provide stability and movement to the car.
- **360° Front Wheel**: Helps in controlling the direction of the car.
- **12V Battery**: Powers the L298N motor driver.
- **Mobile Application**: A simple webpage to send control signals to the NodeMCU.

## Features

- Control the car's movement (forward, backward, left, right) using a mobile app through Wi-Fi.
- Speed control of the motors.
- Simple user interface with intuitive controls.

## How It Works

1. **Hardware Setup**:
    - The ESP8266 NodeMCU is connected to the L298N motor driver and the DC motors.
    - The 12V battery powers the motor driver and the motors.
    - The front and rear wheels are attached to the motors for movement.

2. **Web Interface**:
    - A webpage is hosted by the ESP8266 NodeMCU, allowing users to control the car's movements via buttons.
    - The webpage sends HTTP requests to the NodeMCU, which interprets them to control the motors accordingly.

3. **Control Signals**:
    - Forward, backward, left, and right control signals are sent from the mobile browser to the ESP8266, which processes them to rotate the motors in the appropriate direction.

4. **Motor Driver**:
    - The L298N motor driver receives the control signals from the NodeMCU and drives the DC motors accordingly to move the car.

## Circuit Diagram

![Circuit Diagram]([link_to_your_circuit_diagram_image](https://drive.google.com/file/d/1RHg9bM0XIeCLwlDT8gruEhZnratW9lvD/view?usp=sharing))

## Setup and Installation

1. **Hardware Connections**:
    - Connect the ESP8266 NodeMCU to the L298N motor driver using jumper wires.
    - Connect the two 3.6V DC motors to the output pins of the L298N motor driver.
    - Power the L298N motor driver using the 12V battery.
    - Connect the 3.3V pin of the NodeMCU to the L298N logic input pin for motor control.

2. **Software Setup**:
    - Clone this repository to your local machine:
      ```bash
      git clone https://github.com/your_username/wifi-controlled-car.git
      ```
    - Open the code in Arduino IDE.
    - Upload the code to your ESP8266 NodeMCU.
    - Connect the ESP8266 to your Wi-Fi network by modifying the `ssid` and `password` variables in the code.
    - Once uploaded, open the Serial Monitor to get the IP address of the NodeMCU.

3. **Web Interface**:
    - Open a browser on your mobile device and enter the IP address displayed in the Serial Monitor.
    - You will be redirected to a simple control page to move the car in different directions.

## Code

The main code for controlling the car is written in Arduino IDE. It uses the ESP8266WiFi library to connect to a Wi-Fi network and the ESP8266WebServer library to host the webpage.
