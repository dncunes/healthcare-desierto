# Healthcare Desierto Senior Capstone Project

# PROJECT OVERVIEW
This project investigates the spatial relationship between healthcare facilities and public transportation access in Tucson, Arizona. Using geospatial data, Google Maps APIs, and statistical analysis, we assess whether healthcare services are equitably accessible via public transit and identify underserved regions.

# Objectives
- Map and classify healthcare facilities by type and service coverage.
- Measure walking and straight-line distances to the nearest bus stops.
- Analyze accessibility disparities using transportation thresholds.
- Visualize results through maps, summary statistics, and charts.

# Tools & Technologies
- Python
  - pandas - data manipulation and analysis
  - requests, json, time - API handling and response management
  - geopy.distance.geodesic - calculating real-world distances between coordinates
  - math (radians, cos, sin, etc.) - Haversine formula and distance calculations
  - tqdm - progress bar visualization for loops
  - openpyxl - reading and working with Excel files
  - itertools - advanced iteration handling
- Google Colab - cloud-based Jupyter notebook environment for development and collaboration
- Google Maps API - retreiving place and distance data
- GitHub - version control, collaboration, and hosting the final website and project files
