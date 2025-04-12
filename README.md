# ESP32 Temperature Monitoring System

A real-time temperature monitoring system using the ESP32 microcontroller, which sends data to a web dashboard via a Node.js backend and MongoDB database.

## Features

- ESP32 reads temperature using [sensor name, e.g., DHT11].
- Sends data to a Node.js backend over Wi-Fi.
- Stores readings in MongoDB.
- Displays live temperature data on a web dashboard.
- Automatically updates every minute.


## Tech Stack

- **Hardware**: ESP32, [Temperature Sensor; DHT11]
- **Firmware**: Arduino (C++)
- **Backend**: Node.js, Express.js, MongoDB Atlas
- **Frontend**: HTML, CSS, JavaScript

---

## How It Works

1. ESP32 connects to Wi-Fi and reads temperature.
2. It sends a POST request every 60 seconds to the backend.
3. The backend receives the data and stores it in MongoDB.
4. The frontend fetches and displays real-time data from the backend.

---


## Setup Instructions

### ESP32 Firmware

1. Open `esp32_temp.ino` in Arduino IDE.
2. Install necessary libraries (`DHT`, `WiFi`, `HTTPClient`).
3. Add your Wi-Fi credentials and backend URL.
4. Upload to ESP32.

### Backend

```bash
git clone https://github.com/yourusername/esp32-temp-monitor.git
cd esp32-temp-monitor/backend
npm install
