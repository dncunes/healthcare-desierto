# Healthcare Desierto Senior Capstone Project

# PROJECT OVERVIEW
This project investigates the spatial relationship between healthcare facilities and public transportation access in Tucson, Arizona. Using geospatial data, Google Maps APIs, and statistical analysis, we assess whether healthcare services are equitably accessible via public transit and identify underserved regions.

# Project Website
This project includes a live website that showcases:
  - The research paper with background music
  - Static Visualizations
  - Code snippets from key analysis steps
  - A Key Findings/ FAQ page
  - A Meet the Team section

Visit the website
https://dncunes.github.io/healthcare-desierto/index.html

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

# Repository Structure

├── .git/                            # Git version control directory (hidden)
├── img/                             # Image assets used on the website

├── styles.css                       # Custom CSS styling for the website
├── Drifting at 432 HZ - Unicorn Heads.mp3   # Background music for the research paper page
├── project_config_template.json     # Template file for storing API key securely

├── index.html                       # Homepage of the project website
├── about_the_project.html           # About the Project page
├── paper.html                       # Research paper with embedded music
├── visualizations.html              # Project visualizations
├── code.html                        # Code snippets and explanations
├── faq.html                         # Frequently asked questions and key findings
├── about_us.html                    # Meet the Team page

├── capstone_report.pdf              # Final research paper (downloadable)
├── Under Construction.pdf           # Placeholder before final paper was uploaded

├── README.md                        # Project overview and documentation (this file)

# How to Run the Project

1. Clone the repository
   Open a terminal and run:
   git clone https://github.com/dncunes/healthcare-desierto.git
   cd healthcare-desierto
2. Install dependencies
   If you plan to run the Python scripts locally (for distance calculations, API calls, etc.) install the required libraries:
   pip install -r requirements.txt
3. Set up your API key
   This project uses a project_config_template.json file to securely handle API keys.
   - Copy project_config_template.json and rename it to project_config.json
   - Open it and replace the placeholder with your actual API key:
     {
        "API_KEY": "YOUR_API_KEY_HERE"
     }
  4. Open the website
     You can open any of the .html files directly in a browser (e.g., index.html) or host the site using GitHub Pages or a local server.


# API Key Configuration

# Key Findings

# About Me
