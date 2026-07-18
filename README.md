
# ESP32-Powered Automated Smart Irrigation System 🌱💧
A standalone, battery-powered IoT prototype that automates plant watering based on real-time soil moisture telemetry and environmental factors.
## 🚀 Features
* **Smart Automated Watering:** Submersible pump automatically turns ON/OFF based on soil moisture thresholds.
* **Dual Telemetry:** Tracks both Soil Moisture (%) and Ambient Temperature (°C) using DHT11.
* **Local Visuals:** Outputs real-time status onto a 16x2 I2C LCD screen.
* **IoT Web Server:** Hosts a local HTML web dashboard to view live telemetry from any device on the same WiFi network.
* **Robust Power Management:** Integrated with a buck converter to run efficiently off a high-capacity LiPo battery.
## 🛠️ Hardware Architecture
* **Microcontroller:** ESP32 (with Expansion Board)
* **Sensors:** Soil Moisture Sensor Module, DHT11 Temperature Sensor
* **Actuators:** 4-Channel Relay Module, 5V Mini Submersible Water Pump
* **Power:** 11.1V 3S LiPo Battery (2200mAh), LM2596 Buck Converter (Stepped down to 5V)
* **Display:** 16x2 I2C LCD Display
## 🔌 Circuit Pin Mapping

| Component | Component Pin | ESP32 GPIO Pin |
| :--- | :--- | :--- |
| **Soil Moisture** | AO (Analog Out) | GPIO 34 |
| **DHT11 Sensor** | DATA | GPIO 23 |
| **I2C LCD** | SDA / SCL | GPIO 21 / GPIO 22 |
| **Relay Module** | IN1 | GPIO 19 |

## 💻 Software & Libraries Used
* **Framework:** Arduino IDE (ESP32 Board Core)
* **Libraries:**
  * `WiFi.h` & `WebServer.h` (Built-in)
  * `Wire.h` & `LiquidCrystal_I2C.h` (For LCD)
  * `DHT.h` by Adafruit (For Temp/Humidity)
## 🔧 How to Setup & Run
1. Clone this repository or download the `.ino` file.
2. Install the required libraries via Arduino Library Manager (`Ctrl + Shift + I`).
3. Open the code in Arduino IDE, and replace `YOUR_WIFI_NAME` and `YOUR_WIFI_PASSWORD` with your local credentials.
4. Select `ESP32 Dev Module` under `Tools -> Board`.
5. Calibrate the `threshold` variable based on your soil type and sensor readings.
6. Compile and upload!