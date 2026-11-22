# SkyScout Pro — Weather & Travel Intelligence

A polished, beginner-friendly hackathon project that helps people understand weather and plan trips using real public data.

## Run the project
1. Extract `SkyScout_Pro_Master_Project.zip`.
2. Open the `SkyScout_Pro_Master_Project` folder in VS Code.
3. Install the **Live Server** extension (recommended).
4. Right-click `index.html` → **Open with Live Server**.
5. Keep an internet connection active. The project loads its map, fonts and live data from public services.

You can also open `index.html` directly in a modern browser, but Live Server is more reliable.

## Features
- Search locations worldwide using place-name geocoding.
- Optional browser location permission (the user chooses whether to share it).
- Current weather: temperature, feels-like temperature, humidity, wind, rainfall and UV index.
- Seven-day forecast with high/low temperatures, rain probability, wind and UV.
- Interactive OpenStreetMap map: zoom, pan, city markers and click-to-explore reverse geocoding.
- Air quality panel using current US AQI, PM2.5 and PM10 data where available.
- Weather indicators for high rain probability, high temperatures, strong winds and thunderstorm codes.
- Weather-aware trip planner with departure/return dates, forecast check, rough straight-line distance and packing checklist.
- Weekly charts, printable report, Celsius/Fahrenheit switch and saved last location.
- Responsive layout for desktop, tablet and mobile.

## Public APIs and libraries
1. **Open-Meteo Geocoding** — `https://geocoding-api.open-meteo.com/v1/search` and reverse lookup.
2. **Open-Meteo Forecast** — `https://api.open-meteo.com/v1/forecast`
3. **Open-Meteo Air Quality** — `https://air-quality-api.open-meteo.com/v1/air-quality`
4. **OpenStreetMap** — map tiles, displayed with Leaflet.
5. **Leaflet** — interactive map library.

This demo does not require a personal API key. Public service availability, fair-use limits and terms can change; review each provider's current terms before a public/commercial deployment. Keep required attribution visible.

## Important honesty for your hackathon presentation
- Weather data is fetched from a real public forecast service. Forecasts are estimates and can change.
- The seven-day forecast is not a long-range seasonal prediction.
- Weather alerts in this student project are **rule-based indicators** derived from forecast values. They are not official government warnings and do not replace emergency services.
- The travel comfort score is a transparent student-designed calculation, not a certified safety score.
- Air-quality readings are supplied by a separate model/service and may be unavailable for some locations.
- Trip distance is a straight-line estimate between geocoded places, not driving distance or a route.
- The trip planner checks weather on the departure date when it is inside the provider's available forecast window. For dates outside that window, it clearly says the forecast is unavailable.
- Crowd levels, hotel prices, live flight status, bookings and actual road traffic are **not** included because this version does not have verified data sources for them. Do not claim those are live features.

## Explain the travel comfort score
The score begins at 100 and subtracts simple penalties:
- Rain probability × 0.35
- If maximum temperature is above 35°C: 2.2 points per degree above 35
- If minimum temperature is below 5°C: 1.5 points per degree below 5
- If maximum wind is above 35 km/h: 0.8 points per km/h above 35
The result is limited to 0–100. This is only a simple planning indicator.

## Suggested live demo
1. Search Hyderabad and explain the current conditions.
2. Switch to Fahrenheit and back to Celsius.
3. Open Forecast and explain the high, low and rain chance.
4. Open World Map, zoom and click another region/city.
5. Open Air Quality and explain the AQI in plain language.
6. Open Trip Planner, select Goa and a date in the next seven days.
7. Show the packing checklist and tick items.
8. Open Alerts and explain that they are indicators, not official warnings.
9. Open Insights & Reports and use Print report.

## Before submitting
- Test the project on the actual presentation laptop and mobile.
- Check that the network permits the Open-Meteo and OpenStreetMap domains.
- Keep a few screenshots ready in case the venue internet is unreliable.
- Read the hackathon rubric carefully. No project can guarantee a particular score; judges assess the demo, implementation, originality, usefulness, reliability and presentation.

## Advanced Edition upgrades
- Multi-result worldwide city search: choose the correct city when names are repeated.
- Request timeout and clearer network-error messages.
- Local-calendar date handling for trip date inputs.
- Live road route, route geometry and estimated driving time through the public OSRM routing demo service; if it is unavailable, the report falls back to a clearly labelled straight-line estimate.
- Trip forecast summary across the available forecast days in the selected date window.
- Save trip summaries in this browser and download a plain-text trip report.
- A weather-based suggestion panel that turns forecast values into practical tips. It is a transparent rule-based helper, not a generative AI service.

## Advanced APIs used
- Open-Meteo Geocoding API: worldwide city search and reverse geocoding.
- Open-Meteo Forecast API: current, hourly and seven-day weather.
- Open-Meteo Air Quality API: current US AQI and particulate readings when available.
- OSRM public routing demo: road route geometry, approximate distance and duration.
- OpenStreetMap tiles + Leaflet: interactive maps and trip route display.

The OSRM public demo is a community/demo service and is not a guaranteed production service. For a public deployment, use a routing provider with a suitable service agreement and follow its usage policy. All public APIs can have availability and rate limits. This frontend app intentionally contains no private API keys.
