# Braugon
Braugon is a car-controlling gui for fun.

This repository containe an attempt to create a custom app that can control a Osoyoo V2.1 robot-car over WiFi. The application should send HTTP or UDP requests to the robot car to control it. A guide on how to implement both the microcontroller side and the browser-based application side could look like:

## 1. setting up the robot car
The Osoyoo V2.1 robot car is correctly assembled and configured. The instructions were followed to ensure that the Wi-Fi connection and control options are working. [Link](https://osoyoo.com/manual/V2.1robotcar.pdf)

## 2. selection of technologies
For a browser-based control, the following elements will be needed:
- HTML/CSS/JavaScript for the user interface
- WebSockets or HTTP for communication between the browser and the robot car
- Server (e.g. Node.js) to manage the communication

## 3. communication with the robot car
The robot car is controlled by a microcontroller board (Arduino Mega) that can be connected to a Wi-Fi network and can receive and process HTTP requests or accept a WebSocket connection.
Different methods can be used to let the Node.js server and the Arduino communicate with each other. One option is to use serial communication when the Arduino is connected directly to the computer. Alternatively, it can also communicate via the network.

## 4. development of the server
A simple Node.js server can be used to enable communication between the browser and the robot car. 

## 5. development of the user interface
A HTML page with controls (buttons, joystick, etc.) that allows the user to control the robot car.

## 6. robot car logic (Arduino sketch)
The in the documentation existing Arduino sketch is already set up to receive UDP messages and react accordingly. The implementation remains largely unchanged. It is just need to make sure that the communication between the Node.js server and the Arduino works correctly.


