### WiFi Trolley Bot using ESP32

#### Introduction
This project demonstrates the creation of a WiFi-controlled Trolley Bot using the ESP32 microcontroller.

#### Features
- Remote control via WiFi
- Real-time data monitoring
- Obstacle detection and avoidance
- Speed and direction control

#### Hardware Requirements
- ESP32 microcontroller
- Motor driver (e.g., L298N)
- DC motors
- Wheels and chassis
- Power supply
- Ultrasonic sensors
- WiFi module

#### Software Requirements
- Arduino IDE
- ESP32 board support package
- Libraries: WiFi, Servo, Ultrasonic

#### Installation
1. **Clone the repository:**
   ```bash
   git clone https://github.com/AbiXnash/WiFi-Trolley-Bot-using-ESP32.git
   ```
2. **Open the project in Arduino IDE:**
   - Open `WiFi-Trolley-Bot-using-ESP32.ino` file.
   
3. **Install necessary libraries:**
   - Go to Sketch -> Include Library -> Manage Libraries.
   - Search for and install the required libraries (WiFi, Servo, Ultrasonic).

4. **Upload the code:**
   - Connect the ESP32 to your computer.
   - Select the appropriate board and port from Tools menu.
   - Click on Upload button.

#### Usage
1. **Power the Trolley Bot:**
   - Ensure the power supply is connected.

2. **Connect to ESP32's WiFi Network:**
   - On your device, connect to the WiFi network created by the ESP32.

3. **Control the Bot:**
   - Open a web browser and navigate to the ESP32's IP address.
   - Use the web interface to control the direction and speed of the trolley bot.

#### Contributing
Contributions are welcome. Please fork this repository, create a new branch, and submit a pull request.

#### License
This project is licensed under the MIT License.
