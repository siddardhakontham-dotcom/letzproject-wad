# SkyScout Pro — Live Demonstration Guide

## Before the demonstration
1. Extract the ZIP file.
2. Open the `SkyScout_Pro_Master_Project` folder in VS Code.
3. Open `index.html` with Live Server.
4. Confirm that the laptop has internet access.
5. Keep a backup screenshot or the app open before the presentation in case the venue network blocks a public API.

## Live demonstration sequence (about 4 minutes)

### 1. Show the dashboard
- The app starts with Hyderabad as the default city.
- Explain that the temperature, humidity, wind, rain and forecast are fetched from Open-Meteo.
- Click the °C button to change to °F, then change back.

### 2. Search another city
- Search for `Tokyo` and click Search.
- For a name shared by multiple places, choose the correct result from the dropdown.
- Explain that the Geocoding API converts a place name into coordinates.

### 3. Forecast and air quality
- Open Forecast and show the seven-day table and hourly cards.
- Return to Overview and show the air-quality panel.
- Explain that AQI can be unavailable for some places because it comes from a separate data service.

### 4. Interactive map
- Open World Map.
- Zoom and pan; click a map location to load weather for the selected place.
- Explain that Leaflet displays OpenStreetMap tiles.

### 5. Smart trip planner
- Open Plan your trip.
- Use `Hyderabad` as the start and `Goa` as the destination.
- Choose a departure date within the next seven forecast days and a return date a few days later.
- Click Check my trip conditions.
- Show the route line, estimated road distance and driving time if the OSRM service responds.
- Show the available day-by-day forecast, weather comfort indicator and packing checklist.
- Click Save this trip, then Download trip report.

### 6. Weather indicators and report
- Open Weather alerts and explain that these are rule-based forecast indicators, not official government warnings.
- Open Insights & reports and select Print report.

## Short explanation of the technology
"SkyScout Pro is built with HTML, CSS and JavaScript. It uses Open-Meteo APIs for geocoding, weather and air quality. It uses Leaflet and OpenStreetMap for interactive maps, and OSRM for a road-route estimate. The website fetches live data when a user searches or plans a trip."

## Important presentation honesty
- Weather forecasts are estimates and can change.
- The weather comfort score and weather indicators are simple educational calculations, not official safety assessments.
- Road distance and travel time are estimates from the public OSRM demo service; they are not live traffic predictions.
- If a service is unavailable, some panels may show an unavailable message or a fallback estimate. This is why a stable internet connection is needed.
