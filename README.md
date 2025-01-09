

# ESP32 Camera Car

This project demonstrates how to build a Wi-Fi-controlled car with a camera using the ESP32. The car can be controlled via a web interface, allowing users to view the camera feed in real time and control the car's movement and other functionalities.

---

## Features
1. **Real-time Camera Feed**: Streams live video feed from the ESP32 camera module.
2. **Car Movement Control**: Move the car forward, backward, left, or right using on-screen arrow buttons.
3. **Speed Control**: Adjust the car's motor speed with a slider.
4. **Light Control**: Control the car's headlights or onboard light using a slider.
5. **Wi-Fi Access Point**: The ESP32 acts as an access point, making it easy to connect and control the car.

---

## Hardware Requirements
1. **ESP32-CAM**: For the camera and Wi-Fi capabilities.
2. **L298N Motor Driver**: To control the motors.
3. **Motors**: DC motors for car movement.
4. **LED/Light**: For headlight control.
5. **Power Supply**: Suitable for the ESP32 and motors.
6. **Chassis**: A car chassis to mount the components.

---

## Software Requirements
1. **Arduino IDE**: To program the ESP32.
2. **ESP32 Board Support**: Install via Arduino IDE Board Manager.
3. **Libraries**: Install the following Arduino libraries:
   - `ESPAsyncWebServer`
   - `AsyncTCP`
   - `esp_camera`

---

## Pin Connections

### ESP32-CAM Pin Configuration
| **Function** | **ESP32 Pin** |
|--------------|---------------|
| Camera D0    | GPIO 5        |
| Camera D1    | GPIO 18       |
| Camera D2    | GPIO 19       |
| Camera D3    | GPIO 21       |
| Camera D4    | GPIO 36       |
| Camera D5    | GPIO 39       |
| Camera D6    | GPIO 34       |
| Camera D7    | GPIO 35       |
| XCLK         | GPIO 0        |
| PCLK         | GPIO 22       |
| VSYNC        | GPIO 25       |
| HREF         | GPIO 23       |
| SDA          | GPIO 26       |
| SCL          | GPIO 27       |

### Motor Driver Connections
| **Motor**        | **Pins** |
|------------------|----------|
| Right Motor PWM  | GPIO 12  |
| Right Motor IN1  | GPIO 13  |
| Right Motor IN2  | GPIO 15  |
| Left Motor PWM   | GPIO 12  |
| Left Motor IN3   | GPIO 14  |
| Left Motor IN4   | GPIO 2   |

### Additional Pin Configuration
| **Component**  | **Pin**  |
|----------------|----------|
| Light (LED)    | GPIO 4   |

---

## Setup Instructions
1. **Hardware Setup**:
   - Connect the motors to the L298N motor driver.
   - Connect the ESP32-CAM to the motor driver and the light module as per the pin configuration.
   - Mount all components on the car chassis.

2. **Software Setup**:
   - Open the Arduino IDE.
   - Install the required libraries.
   - Copy the provided code into the Arduino IDE.
   - Update the `ssid` and `password` variables for your Wi-Fi credentials.
   - Compile and upload the code to the ESP32-CAM.

3. **Power the Car**:
   - Provide power to the ESP32-CAM and motor driver.

4. **Access the Web Interface**:
   - Connect to the ESP32's Wi-Fi (SSID: `MyWiFiCar`, Password: `12345678`).
   - Open a browser and navigate to `192.168.4.1`.

---

## Usage Instructions
1. **View the Camera Feed**:
   - The live video feed will be displayed on the web interface.

2. **Control the Car**:
   - Use the arrow buttons on the interface to control the car's movement (forward, backward, left, right, stop).
   - Adjust the speed using the speed slider.
   - Control the light intensity using the light slider.

---

## Troubleshooting
1. **No Camera Feed**:
   - Check the camera connections.
   - Ensure the ESP32-CAM has sufficient power.
   - Verify that the `esp_camera` library is installed.

2. **No Motor Movement**:
   - Verify motor driver connections.
   - Check motor power supply.
   - Ensure the PWM signal is being sent correctly.

3. **Cannot Connect to Wi-Fi**:
   - Check the SSID and password in the code.
   - Ensure the ESP32-CAM is powered and in range.

---

## License
This project is open-source. Feel free to modify and distribute it as per your needs.

---

## Author
Your Name (Optional)

For any queries or contributions, feel free to contact me.

---

Let me know if you'd like me to refine or add additional details!
