# Geoprocessing

## Stage-5 : Metro Station Accessibility Analysis (QGIS)

This project is the fifth stage of my GIS learning journey. In this stage, I used **OpenStreetMap (OSM) data** to identify metro stations and performed spatial analysis to determine the number of people living within **1 km of a metro station**.

## Objective

* Download metro station data from OpenStreetMap.
* Reproject the metro station layer into a suitable projected CRS.
* Create a 1 km buffer around metro stations.
* Use a population grid to estimate the population living within the buffer zones.
* Apply Zonal Statistics to calculate population within the 1 km metro accessibility areas.

## Tools Used

* QGIS
* QuickOSM Plugin
* OpenStreetMap (OSM)
* Population Grid
* Buffer Analysis
* Zonal Statistics
* Coordinate Reference Systems (CRS)

## Workflow

### Download OpenStreetMap Data

Used the **QuickOSM** plugin in QGIS to download metro station data from OpenStreetMap.

**Vector → QuickOSM → QuickOSM**

The downloaded vector layer contains the metro stations within the selected study area.

### Reproject Metro Stations

The downloaded OSM data was initially in **EPSG:4326 (WGS 84)**, where coordinates are measured in degrees.

Since buffer distances need to be measured in metres, the metro station layer was reprojected into a suitable **projected CRS**.

### Create 1 km Buffer

Created a **1,000 metre (1 km) buffer** around each metro station using the QGIS Buffer tool.

The resulting polygons represent the areas located within 1 km of the metro stations.

### Calculate Zonal Statistics

Loaded a population grid and overlaid it with the 1 km metro station buffer.

Used **Zonal Statistics** to calculate the population values within the buffer zones.

This helped determine the estimated number of people living within 1 km of each metro station.

## Key Insights

* Downloaded real-world metro station data from OpenStreetMap.
* Learned how CRS affects distance-based spatial analysis.
* Created 1 km accessibility zones around metro stations.
* Combined vector metro station data with population grid data.
* Used Zonal Statistics to estimate the population served by metro stations.
* Demonstrated how GIS can be used for **transportation accessibility and urban planning**.

## Course Reference

This project was completed while following the Introduction to QGIS course by Spatial Thoughts, particularly: https://courses.spatialthoughts.com/introduction-to-qgis.html
