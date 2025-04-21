# ESPHome Weather Station

This project is an ESPHome-based weather station using an ESP8266 microcontroller (D1 Mini). It integrates multiple sensors, displays, and APIs to provide real-time weather data and environmental monitoring.

## Features

- **DHT11 Sensor**: Measures temperature and humidity.
- **BMP180 Sensor**: Measures temperature and atmospheric pressure.
- **OpenWeatherMap Integration**: Fetches real-time weather data for Bauchi State, Nigeria, and Budapest, Hungary.
- **OLED Display**: Displays sensor readings, weather data, and time.
- **Buzzer**: Plays melodies using the RTTTL protocol.
- **Button Shield**: Detects button presses and triggers actions.
- **Web Server**: Provides a web interface for monitoring.
- **Wi-Fi Connectivity**: Connects to your local Wi-Fi network.
- **I2C Bus Scanning**: Detects connected I2C devices.
- **Time Synchronization**: Uses SNTP for accurate timekeeping.

## Project Structure

. ├── esp-weather.step-01.yaml # Main ESPHome configuration file ├── esp-weather.step-01.yaml_bkp # Backup of the configuration file ├── fonts/ # Fonts used for the OLED display │ ├── regupix_.ttf │ ├── regupixb.ttf ├── img/ # Images used for the OLED display │ ├── bitcoin-logo.png │ ├── logo_slh_dshop.png ├── tests/ # Test files for the project │ ├── test_config_validation.py ├── .gitignore # Git ignore file


## Prerequisites

- [ESPHome](https://esphome.io/) installed on your system.
- An ESP8266-based microcontroller (e.g., D1 Mini).
- Sensors: DHT11 and BMP180.
- OLED display (SSD1306 64x48).
- Active OpenWeatherMap API key.

## Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd esphome-workshop

2. Install ESPHome: Follow the [ESPHome installation guide](https://esphome.io/guides/installing_esphome.html). 

3. Configure Wi-Fi and Secrets: Create a secrets.yaml file in the root directory with your Wi-Fi credentials:
   ``
   wifi_ssid: "YourWiFiSSID"
   ``
   ``
   wifi_password: "YourWiFiPassword"
   ``
4. Deploy the Configuration: Run the following command to validate and upload the configuration:

   ``
   esphome run esp-weather.step-01.yaml  ``

## Usage
- Access the web server by navigating to the device's IP address in your browser.
- View real-time weather data and sensor readings on the OLED display.
- Use the button shield to trigger actions or play melodies.
## Images and Fonts
- Images: Located in the img/ directory, used for the OLED display.
- Fonts: Located in the fonts/ directory, used for text rendering on the OLED display.
## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments
- [ESPHome](https://esphome.io/) for simplifying IoT development.
- [OpenWeatherMap](https://openweathermap.org/) for providing weather data.