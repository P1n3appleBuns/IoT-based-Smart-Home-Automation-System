# IoT-based Smart Home Automation System
This project is an IoT-based Smart Home System designed to remotely control a front door lock and bedroom lights using ESP32 boards and the Blynk IoT platform. It provides a convenient, wireless solution for home automation with both Wi-Fi and ESP-NOW communication.

# Features
* Remote Door Lock Control: Lock or unlock your door from anywhere using the Blynk IoT app.

* Room Light Automation: Turn your bedroom lights on or off wirelessly without leaving your bed.

* ESP-NOW Communication: Seamless device-to-device communication between ESP32 boards without additional network overhead.

* Blynk IoT Integration: Simple mobile interface for controlling devices with one-tap buttons.

* Servo Motor Actuation: Physical control of the door lock and light switch via continuous servo motors.

# Components Used
* 2 × ESP32 Development Boards

  * ESP32 (Door Lock): Connects to Wi-Fi and Blynk IoT app.

  * ESP32 (Room Light): Communicates locally via ESP-NOW with the first ESP32.

* Continuous Servo Motors (x2) – Mechanical actuation for locking/unlocking and toggling light switch.

* Blynk IoT App (Mobile) – Cloud platform for remote control.

* Wi-Fi Network – For remote operation of the door lock ESP32.

* Jumper wires, breadboard, and USB cables for connections.

# How It Works
1. Door Lock ESP32 connects to your Wi-Fi and the Blynk IoT platform.

2. Room Light ESP32 uses ESP-NOW to receive commands locally from the Door Lock ESP32.

3. Both ESP32 boards control continuous servo motors:

    * The first servo locks/unlocks the front door.

    * The second servo flips the bedroom light switch.

4. Control is handled entirely from the Blynk mobile app, making it simple and convenient.

# Why I Built This Project
I often forget if I’ve locked my front door after leaving the house. Additionally, I wanted a way to control my bedroom light while in bed without getting up. This project solved both problems with a practical and fun IoT solution!

# Quick Setup
1. Clone or download this repository.

2. Open the code in Arduino IDE or PlatformIO.

3. Update the following fields in the code:

    #define BLYNK_TEMPLATE_ID "Your_Template_ID"

    #define BLYNK_TEMPLATE_NAME "Your_Template_Name"

    #define BLYNK_AUTH_TOKEN "Your_Auth_Token"

    const char* ssid = "Your_WiFi_Name";

    const char* password = "Your_WiFi_Password";

4. Upload the code to both ESP32 boards.

5. Fine-tune the servo motor delay on lines 32 and 40 to adjust rotation timing for your setup.

6. Open the Blynk IoT app, connect your device, and start controlling your home!

#Future Improvements
* Add status feedback (door locked/unlocked state).

* Integrate voice assistant support (Google Home/Alexa).

* Include sensors for security alerts (e.g., door left open warning).

* Design a 3D-printed enclosure for a polished look.
