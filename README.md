# Gods Eye Weather

A god's eye view of weather around the world. A dark world map with live weather pins for major cities, built from free public data only.

Live site (after Pages is on): https://rd3-lil.github.io/gods-eye/

## What it does

- World map with 62 major cities, from Chicago to Tokyo to Sydney
- Each pin shows the current temperature, colored by how hot or cold it is
- Tap a pin for conditions, humidity, wind, and local time
- Hottest, coldest, and windiest city right now, at the top
- Search a city to fly to it, toggle F / C, refresh on demand
- Auto-refreshes every 15 minutes

## Data sources, all free, no key

- Weather: Open-Meteo (https://open-meteo.com), current temperature, humidity, wind, and WMO weather code. The site fetches it live in the browser, in batches of 20 cities.
- Map tiles: CARTO dark basemap, with OpenStreetMap data
- Map library: Leaflet

No API key, no login, no backend, no private data.

## Files

- `index.html` - the whole site
- `cities.json` - the city list. Add a city by adding one line with name, country, lat, lon.

## Run it locally

Open `index.html` with a local server, for example:

```
python3 -m http.server 8000
```

Then open http://localhost:8000

Opening the file directly will not load `cities.json` in some browsers, so use the server command above.

## Enable GitHub Pages

1. Settings, Pages
2. Source: Deploy from a branch
3. Branch: main, folder / (root), Save
4. Give it a minute, then open the live link above

## Next ideas, not built yet

- Live planes layer from OpenSky Network, same map, plane dots on top of weather
- Rain radar overlay from RainViewer
- More cities, or a city picker by region
