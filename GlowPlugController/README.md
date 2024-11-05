
 ____  __ _  __  ____  ____  __  __ _ 
/ ___)(  / )(  )(  _ \(  _ \(  )(  ( \
\___ \ )  (  )(  ) __/ ) __/ )( /    /
(____/(__\_)(__)(__)  (__)  (__)\_)__) _  _  _  _  ____  __ _  __  ____  ____ 
( \/ )/ )( \(    \(  / )(  )(  _ \(__  )
/ \/ \) \/ ( ) D ( )  (  )(  ) __/ / _/ 
\_)(_/\____/(____/(__\_)(__)(__)  (____)




 _____ _   _  _   _      _____               _          ___  ___          _     
|_   _| | | || | | |    |_   _|             | |         |  \/  |         | |    
  | | | |_| || |_| |______| |_ __ _   _  ___| | ________| .  . | ___   __| |___ 
  | | |  _  ||  _  |______| | '__| | | |/ __| |/ /______| |\/| |/ _ \ / _` / __|
  | | | | | || | | |      | | |  | |_| | (__|   <       | |  | | (_) | (_| \__ \
  \_/ \_| |_/\_| |_/      \_/_|   \__,_|\___|_|\_\      \_|  |_/\___/ \__,_|___/
                                                                                
                                                                                

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


# Glow Plug Controller (Arduino)

**Project Goal**  
Create an Arduino-based glow plug controller to improve starting reliability in Ford 6.9/7.3 IDI engines. This system customizes glow plug operation based on ambient temperature and engine conditions, with built-in monitoring to detect potential glow plug failures.

---

## 📋 Project Overview

The **Glow Plug Controller** project is designed to replace or enhance the stock controller in the 6.9 and 7.3 IDI diesel engines. By monitoring ambient and engine temperatures, as well as glow plug current draw, this controller optimizes glow plug activation to ensure efficient and reliable starting, especially in cold weather.

### Key Features
- **Configurable Glow Plug Timing**: Adjustable timing based on temperature data for optimal plug operation.
- **Real-Time Monitoring with Current Sensor**: Uses a current sensor to monitor glow plug current, detecting failures or anomalies in real time.
- **Temperature-Based Adjustments**: Automatically adjusts glow plug duration depending on ambient and engine temperatures.

---

## ⚙️ Components

- **Microcontroller**: Arduino (compatible with Elegoo or other affordable clones)
- **Temperature Sensor**: Digital sensor compatible with the Arduino (e.g., DS18B20)
- **Current Sensor**: ACS712 (or similar) current sensor module to measure the glow plug circuit current
- **Relays**: 12V relay to control the main glow plug relay
- **Wiring**: 14 AWG for glow plug harness, 18-22 AWG for Arduino connections

---

## 🖥️ Code Overview

The code for this project is written in **C++** and leverages basic Arduino libraries to handle relay control, temperature reading, and current monitoring. Key sections of the code:
1. **Temperature Monitoring**: Reads from the temperature sensor and determines glow plug activation time.
2. **Glow Plug Activation**: Controls the glow plug relay and manages timing.
3. **Current Monitoring**: Uses the current sensor to monitor glow plug current and detect potential plug failures.
4. **Fail-Safe Logic**: Alerts if current values indicate a failure, allowing timely replacement of failed glow plugs.

---

## 🔧 Wiring Diagram

_A detailed wiring diagram is available in the `/diagrams` folder._

### Basic Connections
- **Arduino Digital Pin X** → Glow plug relay (through a 12V relay module)
- **Temperature Sensor Pin** → Arduino analog input
- **Current Sensor Pin** → Arduino analog input
- **Ground** → Vehicle ground
- **Power** → Vehicle 12V (with fuse)

> **Note**: Ensure all connections are insulated and secure to avoid shorts or interference.

---

## 📑 Installation Instructions

1. **Download Code**: Clone or download the code from this repository.
2. **Upload to Arduino**: Open the Arduino IDE, load the code, and upload it to the board.
3. **Connect Components**: Wire the Arduino to the temperature sensor, current sensor, relays, and power as described in the wiring diagram.
4. **Mount the Arduino**: Install the controller in a safe, weather-protected location.

---

## ⚠️ Usage Notes

- **Pre-Test**: Run a preliminary test by connecting only to the temperature sensor, current sensor, and relays. Verify the glow plug timing and current readings, and make adjustments as needed.
- **Safety**: Ensure proper fusing on the power connections to avoid electrical damage.
- **Adjustment**: Modify glow plug timing and current monitoring thresholds in the code if different settings are needed.

---

## 📜 License

This project is open-source under the MIT License. See the main [LICENSE.md](../LICENSE.md) in the THH-Truck-Mods repository for details.

---

*For questions, updates, and to join the discussion, visit our project thread on Oilburners!*
https://www.oilburners.net/threads/arduino-glow-plug-controller-build-walk-through.93803/#post-1147962