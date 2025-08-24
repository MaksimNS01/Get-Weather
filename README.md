# Weather Utility

## Overview
This Python script retrieves weather information for a specified location using the `wttr.in` API. It can display current weather conditions in the terminal and optionally save a weather forecast image as a PNG file. The script supports command-line arguments for customization.

## Features
- Fetches current weather data for a specified location (default: Tomsk).
- Displays weather details including temperature, description, wind speed, humidity, pressure, and visibility.
- Saves weather data in JSON format to `data.txt`.
- Optionally downloads a weather forecast image as a PNG file.
- Supports command-line arguments for specifying the location and image-saving options.

## Requirements
- Python 3.6+
- Required libraries:
  - `requests`
  - `argparse`
  - `json`
  - `typing`

Install the required library:
```bash
pip install requests
```

## Usage
Run the script from the command line with optional arguments.

### Basic Usage
To get weather information for the default location (Tomsk):
```bash
python main.py
```

### Specify a City
To get weather information for a specific city:
```bash
python main.py -c "New York"
```

### Save a Weather Image
To save a PNG image of the weather forecast:
```bash
python main.py -c "New York" --image
```

### Custom Filename for the Image
To specify a custom filename for the PNG image:
```bash
python main.py -c "New York" --image --filename "ny_weather.png"
```

### Command-Line Arguments
- `-c, --city`: Specify the city for the weather forecast (default: Tomsk).
- `--image`: Enable saving a PNG image of the weather forecast.
- `--filename`: Specify a custom filename for the saved PNG image (default: `<city>.png`).

## Output
- **Terminal Output**: Displays formatted weather information including temperature, description, wind speed, humidity, pressure, and visibility.
- **JSON File**: Saves raw weather data to `data.txt`.
- **PNG File**: If the `--image` flag is used, saves a weather forecast image to the specified or default filename.

## Example Output
```plaintext
====== Weather New York ======
  Temperature: 20 °C
  Description: Partly cloudy
  Wind: 15 km/h
  Humidity: 65 %
  Pressure: 1012 mbar
  Visibility: 10 km
==========================
[+] Image saved as "New York.png"
```

## Error Handling
- Handles network errors during API requests.
- Handles invalid data formats from the API response.

## Notes
- The script uses the `wttr.in` API, which requires an active internet connection.
- The default language for weather descriptions is Russian (`lang=ru`).
- Ensure the specified city name is valid and recognized by the `wttr.in` API.
