https://weather-api-five-pink.vercel.app/

![weather](https://github.com/user-attachments/assets/f3d25aa0-3321-450e-8d0e-67bf4d63e6ab)


🌦️ Weather API

https://weather-api-five-pink.vercel.app/

https://github.com/chandaniptl/Weather_API

A simple web app that fetches real-time weather information using the OpenWeatherMap API. Built with HTML5, CSS3, and JavaScript.
📁 Project Structure

weather-api/
├── index.html
├── style.css
├── script.js
└── README.md

🔗 API Used

We use the OpenWeatherMap Current Weather API to get weather data based on city name.
📥 Example API Request

https://api.openweathermap.org/data/2.5/weather?q=London&units=metric&appid=YOUR_API_KEY

    q – City name (e.g., London)

    units – Use metric for Celsius

    appid – Your personal API key from OpenWeatherMap

✅ Sample JSON Response

{
  "weather": [
    {
      "main": "Clouds",
      "description": "broken clouds",
      "icon": "04d"
    }
  ],
  "main": {
    "temp": 21.7,
    "humidity": 64
  },
  "wind": {
    "speed": 4.12
  },
  "name": "London",
  "sys": {
    "country": "GB"
  }
}

💻 Usage
HTML

<input type="text" id="city" placeholder="Enter city name" />
<button id="btn">Search</button>
<div id="result"></div>

JavaScript

const API_KEY = 'YOUR_API_KEY';
const URL = 'https://api.openweathermap.org/data/2.5/weather?units=metric&q=';

async function getWeather(city) {
  const res = await fetch(`${URL}${city}&appid=${API_KEY}`);
  const data = await res.json();
  console.log(data);
}

🚀 Live Demo

weather-api-demo.vercel.app (Replace with your deployment link)
📌 Features

    Search weather by city name

    Displays:

        Temperature

        Weather conditions

        Humidity

        Wind speed

    Simple, responsive UI

🔐 Notes

    You must register on https://openweathermap.org/ to get your free API key.

    Requests are subject to API rate limits (60/minute on free tier).

