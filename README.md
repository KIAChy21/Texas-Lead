# Texas-Lead

Lead Exposure Risk Map – Identifying Heavy Metal Contamination and Health Risks for Children in Texas
![image alt](https://github.com/KIAChy21/Texas-Lead/blob/Texas_Lead-issues/Industry_Texas.png?raw=true)

1. Project Overview
This project aims to map lead exposure risks in Texas by integrating industrial pollution, socioeconomic data, and child health vulnerability indicators. Using GIS and data science techniques, I identify high-risk zones and provide actionable insights.
2. Research Question
How do geolocation, socioeconomic conditions, and industrial toxic discharges contribute to increased lead exposure risks among children under five in Texas?

![image alt](https://github.com/KIAChy21/Texas-Lead/blob/Texas_Lead-issues/Income%20Level_Texas.png?raw=true)

3. Data Sources
The following datasets were used to develop this map:
Data Source	Description
Natural Earth	Base map and administrative boundaries
Census Bureau American Community Survey (ACS)	Socioeconomic vulnerability data
Texas Demographic Center	Population statistics
National Institute on Minority Health and Health Disparities	Income and disparity data
EPA United States Environmental Protection Agency	Lead discharge industries
World Bank Group 	Internet Usage Rate
Natural Earth Shapefile	GDP
EPA United States Environmental Protection Agency 	Lead Discharge Industries
Each dataset was cleaned, processed, and converted into a GIS-compatible format.

4. Software & Tools Used
•	QGIS – For geospatial analysis and visualization
•	GitHub – For project version control and sharing
•	Leaflet.js – For web-based map visualization
5. Data Processing Steps
Data Cleaning & Standardization:
•	Download datasets in CSV.
•	Remove null values and standardize projection (EPSG:4326 WGS 84).
Geospatial Analysis in QGIS:
•	Spatial Join: Match industrial sites with lead exposure reports.
•	Intersection Analysis: Identify census tracts with both high pollution and health impact.
•	Kernel Density Estimation (KDE): Generate a heatmap of contamination hotspots.
•	Choropleth Mapping: Display socioeconomic data with categorized risk levels.
Final Map Layout & Export:
•	Configure legend, title.
•	Export high-resolution world maps (600dpi and 1200dpi) and for heat maps (1200px and 8000px)
•	Save PNG files for Static web mapping.
6. Repository Structure
|-- data/                      # Raw and processed datasets
|-- maps/                      # Final exported maps (PNG)
|-- scripts/                   # Python scripts for automation (optional)
|-- docs/                      # Documentation and guide files
|-- README.md                  # Project overview and setup instructions
|-- lead_exposure_map.qgz      # QGIS project file
7. How to Recreate This Map
Step 1: Download the Repository
Clone the repository using Git:
git clone https://github.com/KIAChy21/Texas-Lead.git
Step 2: Load Data into QGIS
1.	Open QGIS and create a new project.
2.	Load the following layers: 
•	Base map: Natural Earth
•	Industrial sites: EPA United States Environmental Protection Agency
•	Health data: Texas Department of State Health Services
•	Socioeconomic data: National Institute on Minority Health and Health Disparities
•	Internet usage rate: World Bank Group
•	GDP: National Earth Shapefile
•	Population: Texas Demographic Center
3.	Reproject all layers to EPSG:4326 WGS 84.
Step 3: Perform Geospatial Analysis
Use QGIS Geoprocessing Tools:
•	Spatial Join: Match lead exposure reports with pollution sites.
•	Intersect: Find overlap between vulnerable communities and contamination.
•	Kernel Density Estimation: Identify pollution hotspots.
•	Choropleth Mapping: Visualize socioeconomic vulnerability.
Step 4: Export Final Map
1.	Open Print Layout in QGIS.
2.	Add title
3.	Export PNG (for world maps 600dpi and 1200dpi and for heat maps 1200px and 8000px)
![image alt](https://github.com/KIAChy21/Texas-Lead/blob/Texas_Lead-issues/gdp-Texas_Lead.png?raw=true)

![image alt](https://github.com/KIAChy21/Texas-Lead/blob/Texas_Lead-issues/pop%20density-Texas_Lead.png?raw=true)

8. Interactive Map Option
Using Python (Folium) to Create an Interactive Map
import folium

map = folium.Map(location=[31.0, -99.0], zoom_start=6)
folium.GeoJson("maps/Texas_Lead_Exposure.geojson", name="Lead Risk").add_to(map)
map.save("interactive_map.html")
This script generates an interactive web map with risk zones.
9. Expected Outcomes
•	Identification of lead exposure hotspots in Texas.
•	Data-driven insights for public health intervention and policy planning.
•	An open-access interactive map for researchers, activists, and government agencies.

10. Challenges and Future Work
Current Challenges:
•	Limited availability of high-resolution GIS datasets for lead contamination.
•	Socioeconomic data may not be granular enough for precise local analysis.
•	Computational load for large-scale spatial analysis.
Future Enhancements:
•	Incorporate machine learning for predictive risk assessment.
•	Expand mapping to additional environmental contaminants.
•	Integrate real-time data from IoT-based environmental sensors.
11. Contributing & Contact
How to Contribute
We welcome contributions from researchers, developers, and public health experts.
•	Submit feature requests and issues via GitHub.
•	Fork the repository, make improvements, and create pull requests.
•	Contact project maintainers for collaboration opportunities.
License
This project is released under the MIT License. Feel free to use, modify, and share with proper attribution.
Contact Information
For inquiries, reach out to kch365@uky.edu via GitHub Discussions 


