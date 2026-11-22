# API and Demo Guide

## Data flow
1. The user searches for a city.
2. Open-Meteo Geocoding converts the city name into latitude and longitude.
3. The Forecast API returns current conditions and a seven-day forecast.
4. The Air Quality API supplies current AQI information when available.
5. Leaflet displays OpenStreetMap tiles and city markers.
6. The interface turns forecast values into clear summaries, charts and rule-based travel indicators.

## Why no API key?
The selected Open-Meteo endpoints are used here as public educational endpoints and do not require a personal key for this demo. Always review the providers' latest terms, rate limits and attribution requirements before publishing or scaling.

## Suggested future upgrades
- A backend proxy with caching and rate limiting for a larger audience.
- Official meteorological warning feeds for the target country.
- A routing provider for actual road distance and estimated travel time.
- Verified flight, hotel and public transport APIs (with keys stored securely on a backend, never in frontend JavaScript).
- User accounts and cloud-synced saved trips.
- Accessibility testing, automated tests and deployment monitoring.

## Security
This is a frontend-only project. Do not paste private API keys into `app.js`. If you later use paid or private APIs, call them from a backend and store secrets in server-side environment variables.
