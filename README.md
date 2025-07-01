# 🌍 Python API Challenge — WeatherPy & VacationPy

## 📦 Project Overview

This project demonstrates the power of **APIs**, **data visualization**, and **geospatial analysis** using Python. By harnessing real-time weather data and map-based APIs, we answer the question:  
> *"What is the weather like as we approach the equator?"*  
and take it one step further to find ideal vacation spots based on personalized weather criteria.

---

## 📁 Repository Structure
python-api-challenge/
├── WeatherPy/
│   ├── WeatherPy.ipynb             # Jupyter notebook for weather data analysis
│   └── city_data.csv               # Saved output of weather observations
├── VacationPy/
│   ├── VacationPy.ipynb            # Jupyter notebook for vacation mapping
│   └── weather_data.csv            # Filtered weather data for hotel search
├── .gitignore                      # Prevents api_keys.py from being committed
├── api_keys.py                     # API keys for OpenWeatherMap & Geoapify (ignored)
└── README.md                       # Project documentation---

## 🔑 Technologies Used

- Python 3.x  
- Jupyter Notebook  
- Pandas  
- Matplotlib  
- SciPy  
- Citipy  
- OpenWeatherMap API  
- Geoapify API  
- GeoViews (Map visualizations)  
- Requests / JSON parsing  

---

## 🧪 Part 1: WeatherPy — Weather Trends Across the Globe

### ✅ Key Steps
- Generate random lat/lon coordinates
- Use Citipy to map coordinates to the nearest city
- Query **OpenWeatherMap API** to collect:
  - Temperature, Humidity, Wind Speed, Cloudiness, etc.
- Visualize relationships via scatter plots:
  - Latitude vs Temperature
  - Latitude vs Humidity
  - Latitude vs Cloudiness
  - Latitude vs Wind Speed
- Perform **linear regression** on each metric, split by:
  - 🌎 Northern Hemisphere
  - 🌍 Southern Hemisphere
- Interpret R² values and regression trends

### 📊 Regression Analysis Examples
- Northern Hemisphere: Temperature ↓ as latitude ↑  
- Southern Hemisphere: Temperature ↑ as latitude ↓  
- Humidity, wind speed, and cloudiness showed **no strong correlation**

---

## 🏖️ Part 2: VacationPy — Finding Your Ideal Getaway

### ✅ Key Steps
- Filter cities with:
  - Temp between 21–27°C
  - Wind < 4.5 m/s
  - Clear skies (cloudiness = 0%)
- Use **Geoapify API** to find hotels near each selected city
- Display results on a map with:
  - 📍 City location (size = humidity)
  - 🏨 Hotel name and country in hover text

### 🌐 Output
- Interactive map highlighting vacation-ready destinations  
- Example:  
  - Location: Nice, France  
  - Weather: 24°C, 0% clouds, 3 m/s wind  
  - Hotel nearby: "Hôtel Rossetti"

---

## 🔐 API Keys & Security

Ensure sensitive data like API keys is **not committed**:
```bash
# .gitignore
api_keys.py

## 📌 Key Learnings
	•	How to generate and clean geographic data
	•	Efficient use of RESTful APIs and rate limits
	•	Plotting linear relationships with regression models
	•	Creating interactive map visualizations
	•	Filtering data based on multi-criteria weather conditions

## 🧠 Insights
	•	The closer a city is to the equator, the higher the temperature, but other metrics like wind speed and cloudiness show no clear trend.
	•	APIs provide rich real-time datasets that allow for flexible, dynamic queries and decision-making.
	•	Combining data science with mapping tools enables real-world applications like vacation planning or geographic targeting.

## 🚀 How to Run
	1.	Clone the repo: git clone https://github.com/yourusername/python-api-challenge.git
	2.	Add your OpenWeatherMap and Geoapify API keys to api_keys.py:
        weather_api_key = "your_key_here"
        geoapify_key = "your_key_here"
  3.	Launch the Jupyter notebook
	4.	Open and run cells in:
	•	WeatherPy.ipynb for weather analysis
	•	VacationPy.ipynb for vacation mapping

👤 Author

Aditi Nankar
Data Analyst | Weather Explorer | Python Dev

📜 License

This project is for educational use under the MIT License.
