# Weather Application

A simple Weather Application built using **HTML**, **CSS**, and **JavaScript**. This app allows users to fetch and display the current weather information for any city using the [WeatherAPI](https://www.weatherapi.com/).

## Features

- Fetches real-time weather data for any city.
- Displays:
  - City name
  - Country name
  - Temperature in Celsius and Fahrenheit
  - Weather condition
- User-friendly interface with a responsive design.
- Clear button to remove displayed weather data.

## Technologies Used

- **HTML**: For structuring the application.
- **CSS**: For styling the application with a modern and clean design.
- **JavaScript**: For fetching weather data from the API and dynamically updating the DOM.

## How to Use

1. Clone the repository or download the files.
2. Open the `index.html` file in your browser.
3. Enter the name of a city in the input field.
4. Click the "Get Weather" button to fetch the weather data.
5. The weather details will be displayed below the input field.
6. Use the "Clear" button to remove the displayed weather data.

## API Used

This application uses the [WeatherAPI](https://www.weatherapi.com/) to fetch weather data. You need an API key to use this service. Replace the placeholder API key in the JavaScript code with your own API key.

## Code Snippet

Here is a snippet of the JavaScript code used to fetch and display weather data:

```javascript
const getWeather = async (city) => {
  const result = await fetch(`http://api.weatherapi.com/v1/current.json?key=YOUR_API_KEY&q=${city}`);
  if (result.status === 200) {
    const weatherData = await result.json();
    showWeather(weatherData);
  } else {
    alert('City not found or an error occurred.');
  }
};