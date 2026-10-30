# 🌦️ Weather Data Analysis & Visualization

A Python-based weather data analysis project that fetches the last 7 days of weather data using the **Open-Meteo API**, processes it with Pandas, calculates average temperatures, and generates visualizations using Matplotlib.

The project also exports the weather data into a CSV file and saves the temperature chart as a PNG image.

## ✨ Features

- Fetches the last 7 days of weather data using Open-Meteo API.
- Allows users to customize location using latitude and longitude.
- Processes weather data using Pandas.
- Calculates average daily temperature.
- Visualizes maximum, minimum, and average temperatures.
- Exports processed data into a CSV file.
- Saves temperature visualization as a PNG image.

## 🛠️ Tech Stack

- Python
- Requests
- Pandas
- Matplotlib
- Open-Meteo API

## 📁 Project Structure

```text
Weather-Data-Analysis/
│
├── main.py
├── requirements.txt
├── README.md
│
├── data/
│   ├── weather_chart.png
│   └── paris_weather.csv
│
└── .venv/
```

*Note: The `data/` folder and its files are automatically generated when you run the project. The `.venv/` folder is created during environment setup.*

## 🚀 Getting Started

Follow these steps to run the project on your local machine.

### 1. Clone the Repository

```bash
git clone https://github.com/Jainvaishali2107/weather-application
```

Navigate into the project directory:

```bash
cd Weather-Data-Analysis
```

### 2. Create a Virtual Environment

Create an isolated Python environment for this project:

```bash
python -m venv .venv
```

### 3. Activate the Virtual Environment

**For Windows PowerShell:**

```powershell
.\.venv\Scripts\Activate.ps1
```

**For Git Bash:**

```bash
source .venv/Scripts/activate
```

Once activated, you should see `(.venv)` in your terminal.

### 4. Install Dependencies

Install all the required Python libraries with their specified versions:

```bash
pip install -r requirements.txt
```

### 5. Customize Your Location 📍

Open `main.py` and find the API URL.

```python
url = f"https://api.open-meteo.com/v1/forecast?latitude=48.85&longitude=2.35&start_date={start_date}&end_date={end_date}&daily=temperature_2m_max,temperature_2m_min"
```

Replace the latitude and longitude with your preferred location's coordinates.

For example:

| Location | Latitude | Longitude |
|---|---:|---:|
| Delhi, India | 28.6139 | 77.2090 |
| Mumbai, India | 19.0760 | 72.8777 |
| Bengaluru, India | 12.9716 | 77.5946 |
| Paris, France | 48.8566 | 2.3522 |

You can find your coordinates using Google Maps.

**Important:** Keep the rest of the API URL unchanged.

### 6. Run the Project

Execute the Python script:

```bash
python main.py
```

The program will:
1. Fetch weather data from the API.
2. Convert the response into a Pandas DataFrame.
3. Calculate average temperatures.
4. Generate a temperature visualization.
5. Save the chart and CSV file inside the `data/` folder.
6. Display the average temperature in the terminal.

## 📊 Generated Outputs

After successful execution, the project generates:

**1. Weather Chart (`weather_chart.png`)**

A line chart displaying:
- Maximum temperature (Red)
- Minimum temperature (Blue)
- Average temperature (Green)

**2. Weather Dataset (`paris_weather.csv`)**

A CSV file containing:

| Column | Description |
|---|---|
| date | Date of weather observation |
| max_temp | Maximum temperature |
| min_temp | Minimum temperature |
| avg_temp | Average temperature |

*The CSV filename is currently `paris_weather.csv` in the code. You can rename it if you use another location.*

## 📦 Dependencies

The project uses the following Python libraries:

- requests
- pandas
- matplotlib

Other imported modules such as `datetime` and `os` are part of Python's standard library.

All dependency versions are specified in `requirements.txt`.

## 🌐 API Reference

Weather data is retrieved from:

[Open-Meteo Weather API](https://open-meteo.com/)

Open-Meteo provides free weather API access for non-commercial use without requiring an API key.

## 👩‍💻 Author

Created as a Python learning project to practice:

- Working with external APIs
- Python libraries and modules
- Data manipulation using Pandas
- Data visualization using Matplotlib
- File handling and CSV exports
- Virtual environments and dependency management

---

**If you find this project useful, consider giving the repository a ⭐!**