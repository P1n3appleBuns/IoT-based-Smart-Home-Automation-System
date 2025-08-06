# IoT-based Smart Home Automation System
This repository contains the code used for my Smart Home System, which I designed to remotely control my front door lock and bedroom lights.

The system uses two ESP32 boards working together:

&nbsp;&nbsp;&nbsp;&nbsp;-ESP32 (Door Lock): Connects to Wi-Fi and communicates with the Blynk IoT app for remote control.

&nbsp;&nbsp;&nbsp;&nbsp;-ESP32 (Room Light): Linked to the first ESP32 via ESP-NOW for seamless local device-to-device communication.

Both ESP32 boards are connected to contiuous servo motors, which serve as the physical mechanisms to lock/unlock the door and switch the light on/off.

Through the Blynk IoT app, I can easily control both devices with simple button presses, providing a convenient, wireless smart home solution.

I decided to do this project because I tend to forget whether I locked my front door when I leave the house and also to control my bedroom light when I am in bed. :)

# Quick Setup

In the code, you will have to get your Blynk Template ID, Template Name, and Auth Token. Enter into the respective lines in the code. 

Then, you will need to allow the ESP32 to access the WIFI by entering your WIFI Name and Password into the respective lines.

When you have your ESP32 linked up and online you can then fine tune the delay of the servo motor in lines 32 and 40 to match your desired rotation.
