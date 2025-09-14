# 🌍 Real-Time Earthquake Visualizer – Production-Ready

A **production-grade, client-side web application** that visualizes **live earthquake data** from the **USGS GeoJSON feed** on an interactive, high-performance Leaflet map. The app combines **marker clustering**, **heatmaps**, and **dynamic styling** to provide a global overview of recent seismic activity. Designed for **performance**, **responsiveness**, and **clarity** using only **vanilla JavaScript** and **open-source libraries**.

---

## 📸 Demo

[**▶ Live Demo (GitHub Pages)**](https://fitandfine.github.io/Earthquake-Visualizer/)

---

## ✨ Features

| Feature                   | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| **Live USGS Data**        | Fetches earthquakes every 60 seconds from [USGS GeoJSON feeds](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php). |
| **Marker Clustering**     | `leaflet.markercluster` aggregates close points to improve map performance. |
| **Heatmap Layer**         | `leaflet.heat` visualizes quake density and magnitude.                      |
| **Depth-based Coloring**  | Colors encode depth: shallow (teal) → medium (gold/orange) → deep (purple).|
| **Magnitude-based Radius**| Circle markers scale radius proportionally to quake magnitude.              |
| **Auto-Fit Bounds**       | Zooms map to fit all earthquake markers after refresh.                      |
| **Responsive Design**     | Grid layout adapts for mobile and desktop screens.                          |
| **Interactive Popups**    | Each marker includes location, magnitude, depth, timestamp, and USGS link. |

---

## 🛠️ Technology Stack

- **Leaflet.js** – Core mapping engine for interactive maps.  
- **Leaflet.MarkerCluster** – Efficient clustering for hundreds of markers.  
- **Leaflet.heat** – Creates heatmaps from geospatial point data.  
- **OpenStreetMap Tiles** – Free, community-maintained basemap.  
- **Vanilla JavaScript (ES6)** – Fetching, DOM updates, event handling.  
- **HTML5 / CSS3 Grid & Flex** – Responsive layout and styling.  

---

