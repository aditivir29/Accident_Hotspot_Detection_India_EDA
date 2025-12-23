# Accident_Hotspot_Detection_India_EDA
Exploratory data analysis of Indian road accident data to study accident patterns and assess the feasibility of hotspot detection using limited real world data.

# Accident Hotspot Detection in India

## Project Overview
This project performs an exploratory data analysis (EDA) on Indian road accident data to study accident patterns and evaluate the feasibility of accident hotspot detection. The analysis focuses on understanding how factors such as human behavior, weather conditions, road categories, and time influence accident occurrences, while also highlighting the limitations of working with aggregated real world data.

The project is implemented using Python in a Jupyter Notebook and emphasizes analytical reasoning rather than predictive modeling.

## Objective
The primary objective of this project is to analyze road accident data in India and determine whether meaningful accident hotspots can be identified using publicly available datasets. A key goal is to understand how data granularity affects hotspot prediction and to identify gaps that limit precise spatial analysis.

## Data Source
The dataset used in this project is derived from the Ministry of Road Transport and Highways (MoRTH), Government of India, based on the Road Accidents in India 2023 report.

## Dataset Description
The project uses multiple CSV files containing aggregated accident statistics, including:
- State wise road accident counts
- Accident hotspot indicators at the state level
- Human factor related accident and fatality data
- Weather condition based accident statistics
- Road category and road feature related accidents
- Month wise accident and fatality counts

The data is aggregated at state or category level and does not include latitude, longitude, or road segment identifiers.

## Project Structure
The repository is organized as follows:

accident-hotspot-detection-india  
├── data  
│   └── raw  
│       ├── statewise_road_accidents.csv  
│       ├── state_accident_hotspots.csv  
│       ├── state_accident_hotspots_simple.csv  
│       ├── human_factors.csv  
│       ├── monthwise_accidents_fatalities.csv  
│       ├── road_category_accidents_fatalities_injured.csv  
│       ├── road_feature_accidents_killed_injured.csv  
│       └── weather_condition_accidents_killed_injured.csv  
│  
├── notebooks  
│   └── accident_hotspot_eda.ipynb  
│  
├── outputs  
│   └── figures  
│       ├── accidents_by_weather_condition.png  
│       ├── human_factors_accidents_deaths.png  
│       ├── human_factors_impact.png  
│       ├── human_factors_impact_nh.png  
│       └── human_factors_national_impact.png  
│  
├── README.md  
├── requirements.txt  
└── .gitignore  

## Workflow and Steps
The analysis in the notebook follows a clear and structured workflow:

### Step 1 Data Collection
Multiple datasets related to road accidents were collected from the MoRTH 2023 report. Each dataset represents a different dimension of accident analysis such as state distribution, human factors, weather conditions, and road characteristics.

### Step 2 Data Loading and Inspection
- Loaded all datasets using Pandas
- Inspected data shapes, column names, and data types
- Checked for missing values and inconsistencies

### Step 3 Data Cleaning and Preparation
- Renamed columns for clarity
- Ensured consistency in categorical values
- Selected relevant columns for analysis
- Prepared data for visualization

### Step 4 Exploratory Data Analysis
The EDA was conducted across multiple dimensions:

#### State Wise Analysis
- Analyzed accident counts across Indian states
- Identified states with higher reported accident frequencies

#### Human Factors Analysis
- Studied accidents and fatalities caused by human related factors
- Compared national level and highway specific impacts
- Visualized relationships between human factors and accident severity

#### Weather Condition Analysis
- Analyzed accident patterns under different weather conditions
- Compared accident counts, fatalities, and injuries
- Visualized weather related risk patterns

#### Road Category and Road Feature Analysis
- Examined accidents across road categories and road features
- Analyzed fatality and injury trends for different road types

#### Temporal Analysis
- Analyzed month wise accident and fatality trends
- Observed seasonal variations in accident occurrence

### Step 5 Visualization
- Created bar charts and comparative plots to highlight patterns
- Saved key visual outputs for interpretation and reporting

### Step 6 Interpretation and Insights
- Interpreted observed patterns in relation to data limitations
- Evaluated the feasibility of hotspot detection using aggregated data

## Key Insights
- Accident patterns vary significantly across states and contributing factors
- Human behavior plays a major role in accident occurrence and severity
- Weather and road characteristics influence accident outcomes
- Aggregated data hides location specific accident clusters
- State level hotspot identification is possible, but precise road level hotspot detection is not feasible

## Limitations
- Lack of latitude and longitude prevents geospatial hotspot mapping
- Aggregated state level data masks micro level accident locations
- No information on traffic volume, time of day, or road geometry
- Hotspot prediction models cannot be reliably built with current data

This project intentionally highlights these limitations to demonstrate the importance of data quality and granularity in analytical tasks.

## Tools and Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Conclusion
The analysis shows that while exploratory data analysis can uncover meaningful accident trends, accurate hotspot detection requires more granular and geospatially detailed data. This project demonstrates how EDA can be used not only to find patterns, but also to evaluate the suitability of data for advanced analysis and modeling.

## Future Scope
- Integration of GIS based accident location data
- Road segment level hotspot detection
- Inclusion of traffic density and time based variables
- Application of spatial clustering techniques with enriched datasets
