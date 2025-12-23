# Accident Hotspot Detection in India

## Project Overview
This project performs an exploratory data analysis (EDA) on Indian road accident data to study accident patterns and evaluate the feasibility of accident hotspot detection. The analysis focuses on understanding how factors such as human behavior, weather conditions, road categories, and time influence accident occurrences, while also highlighting the limitations of working with aggregated real world data.

The project is implemented using Python in a Jupyter Notebook and emphasizes analytical reasoning rather than predictive modeling.

## Objective
The primary objective of this project is to analyze road accident data in India and determine whether meaningful accident hotspots can be identified using publicly available datasets. A key goal is to understand how data granularity affects hotspot prediction and to identify gaps that limit precise spatial analysis.

## Data Source
The data used in this project is sourced from the Ministry of Road Transport and Highways (MoRTH), Government of India.  
It is based on the official publication:

Road Accidents in India 2023 Report  
Ministry of Road Transport and Highways, Government of India

The report provides aggregated national and state level statistics on road accidents, fatalities, and injuries across multiple dimensions such as human factors, weather conditions, road categories, and temporal distribution.

## Dataset Description
The project uses multiple CSV files extracted and organized from the MoRTH 2023 report, including:
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

### Step 1 Data Collection
Accident related datasets were compiled from the Road Accidents in India 2023 report published by MoRTH. Each dataset represents a different analytical dimension such as state wise distribution, human factors, weather conditions, road characteristics, and temporal trends.

### Step 2 Data Loading and Inspection
- Loaded all datasets using Pandas
- Inspected data structure, column names, and data types
- Checked for missing values and reporting inconsistencies

### Step 3 Data Cleaning and Preparation
- Renamed columns for clarity and consistency
- Selected relevant attributes for analysis
- Prepared datasets for visualization and comparison

### Step 4 Exploratory Data Analysis
EDA was conducted across multiple dimensions:

State Wise Analysis  
Human Factors Analysis  
Weather Condition Analysis  
Road Category and Road Feature Analysis  
Temporal Analysis

Each analysis focused on identifying patterns, variations, and anomalies in accident distribution.

### Step 5 Visualization
- Created bar charts and comparative plots
- Visualized accident counts, fatalities, and injuries across categories
- Saved key visual outputs for interpretation

### Step 6 Interpretation and Insights
- Interpreted observed patterns in the context of data limitations
- Assessed the feasibility of hotspot detection using aggregated data

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
