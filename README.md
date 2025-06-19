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

### Repository Structure
```
├── .git/ # Git version control directory (hidden)
├── img/ # Image assets used on the website

├── styles.css # Custom CSS styling for the website
├── Drifting at 432 HZ - Unicorn Heads.mp3 # Background music for the research paper page
├── project_config_template.json # Template file for storing API key securely

├── index.html # Homepage of the project website
├── about_the_project.html # About the Project page
├── paper.html # Research paper with embedded music
├── visualizations.html # Project visualizations
├── code.html # Code snippets and explanations
├── faq.html # Frequently asked questions and key findings
├── about_us.html # Meet the Team page

├── capstone_report.pdf # Final research paper (downloadable)
├── Under Construction.pdf # Placeholder before final paper was uploaded

├── README.md # Project overview and documentation (this file)
```
# How to Run the Project

1. Clone the repository
   Open a terminal and run:
   git clone https://github.com/dncunes/healthcare-desierto.git
   cd healthcare-desierto
2. Install dependencies
   If you plan to run the Python scripts locally (for distance calculations, API calls, etc.) install the required libraries:
   pip install -r requirements.txt
3. Set up your API key
   This project uses a `project_config_template.json` file to securely handle API keys.
   
   - Copy the file and rename it to: `project_config.json`
   - Open `project_config.json` and replace the placeholder with your actual API key:
   - ```json
     {
        "API_KEY": "YOUR_API_KEY_HERE"
     }
     ```
     > For a detailed explanation, see the [API Key Configuration](#-api-key-configuration) section.
  5. Open the website
     You can open any of the .html files directly in a browser (e.g., index.html) or host the site using GitHub Pages or a local server.

# API Key Configuration
To keep your API key secure, this project uses a seperate config file instead of hardcoding the key directly into the code.
Follow these steps:
  1. Locate the file project_config_template.json in the root of the repository.
  2. Copy it and rename the new file to:
     project_config.json
3. Edit project_config.json and replace the placeholder value with your actual Google Maps API key:
   {
  "API_KEY": "YOUR_API_KEY_HERE"
   }
4. Protect your key:
   Make sure project_config.json is listed in your gitignore file to avoid uploading sensitive credentials.
   Add this line to gitignore if its not already there:
   project_config.json
   
This method keeps your credentials secure while allowing others to run the project with their own API key.

# Jupyter Notebook
You can view my full process in the Jupyter notebook included in this repository:
[View notebook](./final_project.ipynb)

This notebook includes:
- Using Google Maps APIs to locate healthcare facilities and gather key details
- Loading and cleaning bus stop data from local sources
- Calculating walking distances between each healthcare facility and nearby bus stops
- Computing summary statistics to assess overall accessibility
- Creating visualizations using Python (e.g., bar charts, distance distributions)
- Exporting and refining additional visualizations using R for use on the website

A code snippet from the distance calculation step:

<pre> ```python
  def get_walking_distance(lat1, lon1, lat2, lon2, API_KEY, mode='walking'):
  if not API_KEY:
    return "No API key is provided"

  # Round coordinates to the 6th decimal place
  lat1 = round((lat1), 6)
  lon1 = round((lon1), 6)
  lat2 = round((lat2), 6)
  lon2 = round((lon2), 6)

  # Set up url
  url = get_distance_matrix_base_url()

  # Set up params
  params = {
      'origins': f"{lat1},{lon1}",
      'destinations': f"{lat2},{lon2}",
      'mode': mode,
      'key': API_KEY
  } ``` </pre>

# Key Findings

- Approximately 90.4% of healthcare facilities are in walking distance of public transportation.
- There were 5 total healthcare facilities that did not have sufficient access to public transportation. 4 were hospitals and 1 was a primary care facility.
- The healthcare facility that was the farthest away from the nearest bus stop was Carondolet St. Raphael's Emergency Center located approximately 1.4 miles away.
- The closest healthcare facility to the nearest bus stop was ArchWell Health located approximately 6.5 feet away.
- The demographic with the highest accessibility was the middle income.
- The majority of healthcare facilities and accessible bus stops were located in central Tucson, especially near Downtown and along major transit corridors.
- The areas that are less well-served by transit infrastructure were the Southwest, Southeast, and some East side neighborhoods.
- The neighborhoods that were most affected by having the least amount of bus stops and facilities were South Tucson, Drexel Heights, and Valencia West.

### About Me

**Danielle Cunes**  
**B.S. in Information Science with a Data Science emphasis**  
**University of Arizona | Graduated Spring 2025**  

Passionate about solving real-world problems through data, APIs, and geospatial analysis.
Interested in data science, machine learning, and building tools that make information more accessible.

[LinkedIn Profile](https://www.linkedin.com/in/daniellecunes/)

---

Collected local bus stop data from Pima County and the City of Tucson, used Google Maps APIs to identify healthcare facilities and calculate distances to nearby bus stops, then analyzed accessibility using summary statistics and visualized the results in R.

This project was completed as part of a 3-person capstone team.
