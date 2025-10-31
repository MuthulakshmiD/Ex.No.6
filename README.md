# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

# Date:31/10/2025
# Register no. 212223040122
# Aim: Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools

#AI Tools Required:

# Explanation:
Experiment the persona pattern as a programmer for any specific applications related with your interesting area. 
Generate the outoput using more than one AI tool and based on the code generation analyse and discussing that. 

## Process
#### Stage 1 – API Code Generation

Create a prompt that instructs the AI to generate Python code for interacting with two or more APIs.

Example task: “Write Python code to fetch weather data from both OpenWeatherMap and WeatherAPI.”

#### Stage 2 – Output Comparison

Frame a prompt that asks the AI to compare outputs from multiple APIs.

Example task: “Compare the JSON responses from both APIs and highlight key differences in temperature or humidity data.”

#### 💡 Stage 3 – Insight Generation

Design a prompt that requests AI-driven insights or next steps based on the comparison results.

Example task: “Based on the comparison, suggest which API provides more accurate or detailed weather information.”

## code 
```
import requests

def get_weather(city, api_key):
    """
    Fetch current weather data from WeatherAPI.
    """
    url = f"http://api.weatherapi.com/v1/current.json?key={api_key}&q={city}"
    response = requests.get(url)

    if response.status_code == 200:
        data = response.json()
        return data
    else:
        print("Error fetching data:", response.status_code)
        return None


def analyze_weather(data):
    """
    Analyze and interpret weather data.
    """
    if not data:
        return

    city = data["location"]["name"]
    temp_c = data["current"]["temp_c"]
    condition = data["current"]["condition"]["text"]
    humidity = data["current"]["humidity"]
    wind_speed = data["current"]["wind_kph"]

    print(f"\n🌤️ Weather Report for {city}")
    print(f"Temperature: {temp_c}°C")
    print(f"Condition: {condition}")
    print(f"Humidity: {humidity}%")
    print(f"Wind Speed: {wind_speed} km/h")

    # Generate simple insights
    if temp_c > 35:
        print("🔥 It's a hot day! Stay hydrated.")
    elif temp_c < 15:
        print("❄️ It's quite cold! Wear warm clothes.")
    else:
        print("😊 The weather feels moderate and pleasant.")


if __name__ == "__main__":
    api_key = "YOUR_API_KEY_HERE"  # 🔑 Replace with your WeatherAPI key
    city = input("Enter city name: ")
    weather_data = get_weather(city, api_key)
    analyze_weather(weather_data)
```

# Conclusion:
In this project, we successfully created a Python-based program that fetches real-time weather data using the WeatherAPI service. The system retrieves essential weather details such as temperature, humidity, wind speed, and general conditions for any given city.

Through this task, we learned how to use API requests, handle JSON data, and apply conditional logic to generate meaningful insights from real-world data.

This project demonstrates how data science and AI tools can be integrated into simple coding tasks to provide smart, interactive, and real-time applications. It also forms a strong foundation for expanding the project in the future—such as adding AI-generated summaries, data visualization, or voice-based weather assistance.

# Result: 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2703aff6-3ec4-4b8a-b46b-c104dfd7359a" />

The corresponding Prompt is executed successfully.
