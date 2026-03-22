# QR'S WEATHER DASHBOARD

A feature-rich weather app with hourly charts, air quality data, astronomy information and a 3-day forecast — built with vanilla JavaScript and Alpine.js.

---

## What is it?

A weather dashboard that pulls real-time data from the WeatherAPI and presents it in a clean, detailed interface. Goes far beyond a basic weather app — includes hourly temperature graphs, dewpoint, feels like, precipitation, snow, air quality metrics, moon phases and more.

---

## Features

- **Current conditions** — temperature, feels like, humidity, wind speed/direction/gust, cloud cover, precipitation, UV index, visibility
- **Air quality** — CO, NO₂, O₃, PM10 readings
- **3 day forecast** — with full daily breakdown per day
- **Hourly charts** — temperature, dewpoint, feels like, rain and snow plotted per hour using Chart.js
- **Astronomy data** — sunrise, sunset, moonrise, moonset, moon phase, moon illumination
- **Rain and snow alerts** — conditional display when precipitation expected
- **Two views** — current conditions view and forecast dashboard

---

## Screenshots

*Coming soon*

---

## How it works

```
User enters city name
        │
        ▼
WeatherAPI called with city + 3 day forecast + air quality
        │
        ▼
Current conditions parsed and displayed
        │
        ▼
3 day forecast stored
        │
        ▼
For each day:
  - Hourly temperature chart rendered (Chart.js)
  - Hourly rain/snow chart rendered (Chart.js)
  - Daily summary displayed
  - Astronomy data displayed
```

---

## Data Displayed

### Current Conditions
| Field | Description |
|-------|-------------|
| Temperature | °C with feels like |
| Humidity | % |
| Wind | Speed, direction, degree, gust |
| Precipitation | mm |
| Cloud cover | % |
| UV Index | 0-11+ |
| Visibility | km |
| Condition | Text and icon |

### Air Quality
| Field | Description |
|-------|-------------|
| CO | Carbon monoxide |
| NO₂ | Nitrogen dioxide |
| O₃ | Ozone |
| PM10 | Particulate matter |

### Forecast (per day)
| Field | Description |
|-------|-------------|
| Avg / Max / Min temp | °C |
| Humidity | % |
| Max wind | kph |
| Rain chance | % + mm |
| Snow chance | % + cm |
| Condition | Text |

### Astronomy (per day)
| Field | Description |
|-------|-------------|
| Sunrise / Sunset | Time |
| Moonrise / Moonset | Time |
| Moon phase | e.g. Waxing Crescent |
| Moon illumination | % |

---

## Charts

Each forecast day renders two Chart.js line charts:

**Temperature chart** — plots hourly:
- Temperature (°C)
- Dewpoint (°C)
- Feels like (°C)

**Rain and Snow chart** — plots hourly:
- Precipitation (mm)
- Snowfall (mm)

---

## Tech Stack

- **Language:** JavaScript
- **Framework:** Alpine.js
- **Styling:** Tailwind CSS
- **Charts:** Chart.js
- **API:** [WeatherAPI](https://www.weatherapi.com/)

---

## Setup

1. Get a free API key from [WeatherAPI](https://www.weatherapi.com/)
2. Open `index.html`
3. Replace the API key in the fetch URL
4. Open in browser
5. Enter any city name and click **Weather**

---

## Project Structure

```
index.html      Everything — UI, charts, API logic
```

Single file application. No build step required.

---

## Project Status

| Feature | Status |
|---------|--------|
| Current conditions | ✅ Working |
| Air quality | ✅ Working |
| 3 day forecast | ✅ Working |
| Hourly temperature chart | ✅ Working |
| Hourly rain/snow chart | ✅ Working |
| Astronomy data | ✅ Working |
| Rain/snow conditional display | ✅ Working |
| Chart destroy on re-search | 📋 Planned |
| Celsius/Fahrenheit toggle | 📋 Planned |
| Geolocation support | 📋 Planned |
| Dark/light theme | 📋 Planned |

---

## What I Learned

- Working with complex nested API responses
- Rendering multiple dynamic Chart.js instances
- Using Alpine.js `$nextTick` to wait for DOM before rendering charts
- Parsing and displaying date/time data from an API
- Structuring a dashboard with multiple data sources from one API call

---

## Related Projects

- [Movie Finder](https://github.com/Darklord1234938/movie-finder) — Another Alpine.js + REST API project

---

## Author

**Quidon Roethof** — Software Developer, Netherlands

*Built to go beyond a basic weather app and explore how much data a single API call can actually contain.*
