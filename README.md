# 🌍 Real-Time Earthquake Visualizer – Production

A **client-side, interactive web application** that visualizes global earthquakes in real-time using live **USGS GeoJSON feeds**.  
Built with **vanilla JavaScript**, **Leaflet.js**, **Leaflet.MarkerCluster**, and **Leaflet.heat**, this tool allows users to explore earthquakes by magnitude, depth, location, and timeframe, with enhanced interactivity and performance.

---

## 📸 Live Demo

[**▶ Try the demo on GitHub Pages**](https://fitandfine.github.io/Earthquake-Visualizer/)

---

## ✨ Features

| Feature                     | Description                                                                 |
|------------------------------|-----------------------------------------------------------------------------|
| **Live Earthquake Feed**     | Fetches latest quakes from [USGS GeoJSON API](https://earthquake.usgs.gov/) every 60 seconds. |
| **Marker Clustering**        | Efficiently renders hundreds of earthquake points using `leaflet.markercluster`. |
| **Heatmap Overlay**          | Optional `leaflet.heat` layer visualizes intensity and density of seismic activity. |
| **Magnitude & Depth Filters**| Users can filter earthquakes by minimum magnitude and maximum depth.       |
| **Time Frame Selection**     | Choose between last hour, last day, or last week for the displayed data.   |
| **Search by Place**          | Real-time search box filters earthquakes by location name.                  |
| **Rich Popups**              | Displays magnitude, depth, coordinates, UTC time, and a direct USGS link. |
| **Depth Color Coding**       | Circle markers are color-coded: teal→gold→orange→purple based on depth.   |
| **Auto-Fit Bounds**          | Map automatically zooms to show all relevant earthquakes.                  |
| **Responsive Layout**        | Sidebar collapses gracefully on smaller screens for mobile users.          |
| **Legend**                   | Visual depth legend helps interpret color-coded markers.                   |
| **Auto-Refresh**             | Updates earthquake data every 60 seconds without page reload.              |

---

## 🛠️ Technology Stack

- **Leaflet.js** – Core mapping engine for interactive map rendering.
- **Leaflet.MarkerCluster** – Aggregates markers for performance with large datasets.
- **Leaflet.heat** – Heatmap visualization for intensity/density analysis.
- **OpenStreetMap Tiles** – Open-source, community-maintained basemap.
- **Vanilla JavaScript (ES6)** – DOM manipulation, event handling, async data fetching.
- **HTML5/CSS3 Grid** – Responsive layout and modern styling.
- **USGS Earthquake GeoJSON Feeds** – Live seismic data source.

---


---

## ⚙️ Data Handling Logic

1. **Fetch Data**
   - Dynamically constructs the USGS GeoJSON feed URL based on selected timeframe (`all_hour`, `all_day`, `all_week`).
   - Fetches JSON asynchronously using `fetch()`.

2. **Filter & Process**
   - Filters earthquakes by user-defined minimum magnitude, maximum depth, and place name.
   - Extracts coordinates (`lat`, `lon`) and relevant properties (`mag`, `depth`, `place`, `time`, `url`).

3. **Map Visualization**
   - **Cluster Layer:** Uses `L.markerClusterGroup()` to render circle markers efficiently.
   - **Heat Layer:** Uses `L.heatLayer()` to create heat intensity map proportional to magnitude.
   - **Depth-based color coding:** Circle fill color based on depth thresholds.
   - **Magnitude-based radius scaling:** Ensures larger quakes are visually prominent.
   - **Popups:** Include formatted time, magnitude, depth, coordinates, and USGS link.
   - **Auto-fit bounds:** Zooms map to show all filtered earthquakes.

4. **User Interaction**
   - **Filters:** Inputs dynamically update displayed earthquakes.
   - **Search:** Filters by case-insensitive place name.
   - **Toggle Heatmap:** Add/remove heat overlay.
   - **Auto-refresh:** Data updates every 60 seconds without page reload.

---

## 🎨 User Interface

- **Sidebar:** Filters, search box, legend, statistics, and heatmap toggle.
- **Map Area:** Full-screen interactive Leaflet map with clustering and heatmap.
- **Popups:** Rich info display with external links.
- **Responsive Design:** Grid layout adjusts for mobile and desktop screens.

---

## 📈 Data Source

- **Primary Source:** [USGS Earthquake Feeds](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php)
  - GeoJSON feeds updated in real-time for hourly, daily, and weekly earthquakes.
- **Map Tiles:** [OpenStreetMap](https://www.openstreetmap.org/) – free and open-source.

---

## 🚀 Current Limitations / Next Steps for Production

1. **Error Handling**
   - Currently logs fetch errors to console; user-facing notifications could improve UX.

2. **Performance**
   - For extremely dense datasets (thousands of earthquakes), clustering performance may degrade slightly.

3. **Caching / Throttling**
   - Currently fetches every 60 seconds; caching responses could reduce unnecessary API calls.

4. **Accessibility**
   - Keyboard navigation and ARIA labels are not fully implemented.

5. **Analytics / Logging**
   - No analytics or logging of user interactions or errors.

6. **Security**
   - This is a client-only app; future production versions may require HTTPS enforcement, CSP, and input sanitization for safety.

7. **Deployment**
   - For true production readiness:
     - Serve via HTTPS-enabled hosting (GitHub Pages, Netlify, Vercel, or custom server).
     - Minify and bundle JS/CSS for faster load times.
     - Optionally, add service workers for offline support and caching.

---

## 📌 Credits

- **Earthquake Data:** United States Geological Survey ([USGS](https://earthquake.usgs.gov/))
- **Map Tiles:** OpenStreetMap contributors ([OSM](https://www.openstreetmap.org/))
- **Libraries:**  
  - [Leaflet.js](https://leafletjs.com/)  
  - [Leaflet.MarkerCluster](https://github.com/Leaflet/Leaflet.markercluster)  
  - [Leaflet.heat](https://github.com/Leaflet/Leaflet.heat)

---

## 💡 Future Enhancements

- Add **timeline slider** for interactive time exploration.
- Add **regional zoom presets** for specific continents/countries.
- Implement **alerts/notifications** for high-magnitude quakes.
- Store user preferences locally (filters, heatmap toggle) using `localStorage`.
- Add **dark/light theme switcher**.

---

## 📄 License

- Open-source under **MIT License**.




