# Weather-App

This is a simple Python Weather App built using Tkinter for the GUI and the OpenWeatherMap API for fetching real-time weather data. Enter any city name, and the app will display the current weather, temperature, pressure, humidity, wind speed, and sunrise/sunset times.

Features:
- Weather data from OpenWeatherMap using API
- Displays
  - Current weather
  - Temperature (current, min, max)
  - Atmospheric Pressure
  - Humidity
  - Wind Speed
  - Sunrise/Sunset Times
Clean and user-friendly GUI using Tkinter

Preview:
![Weather App Screenshot](Image0073.jpeg)

Tech Stack:
  - Python 3
  - Tkinter for GUI
  - Requests for API calls
  - OpenWeatherMap API

Installations:
  - Install dependencies using:
    pip install requests
  - Tkinter must be installed as well, but it is included in most Python 3 installations

Setup:
  - Clone the repository:
    git clone https://github.com/cookies101-cookies/weather-app.git
    cd weather-app
    
  - API Key:
    - Replace the API key with your own from OpenWeatherMap:
    - api = "https://api.openweathermap.org/data/2.5/weather?q=" + city + "&appid=YOUR_API_KEY"

  - Run the app:
    - python weather_app.py

Example Output:
  - Clear
  - 75°F
  
  - Min Temp: 71°F
  - Max Temp: 78°F
  - Pressure: 1012
  - Humidity: 50
  - Wind Speed: 4.5
  - Sunrise: 06:13:45
  - Sunset: 08:19:20

Notes:
- Time zone for sunrise/sunset is adjusted manually (-21600 seconds = UTC-6). Adjust this for your own timezone if needed.
- API responses are in Kelvin, and the code converts them to Fahrenheit.
- Celsius conversion:
  - Replace this block (12-14)
    - temp = int(json_data['main']['temp'] * 1.8 - 459.67)
    - min_temp = int(json_data['main']['temp_min'] * 1.8 - 459.67)
    - max_temp = int(json_data['main']['temp_max'] * 1.8 - 459.67)
  - With this block:
    - temp = int(json_data['main']['temp'] - 273.15)
    - min_temp = int(json_data['main']['temp_min'] - 273.15)
    - max_temp = int(json_data['main']['temp_max'] - 273.15)

  - Update the units in this block (21-22)
    - final_info = condition + "\n" + str(temp) + "°F"
    - final_data = "\n" + "Min Temp: " + str(min_temp) + "°F" + ...
  - To this block:
    - final_info = condition + "\n" + str(temp) + "°C"
    - final_data = "\n" + "Min Temp: " + str(min_temp) + "°C" + ...

Contributions:
- Pull requests and suggestions are welcome! Feel free to fork and improve the project.






