# US Accidents Data Analysis — Task 4

A comprehensive data analysis project on the **US Accidents dataset**, completed as part of the **SkillCraft Technology Data Science Internship — Task 4**.

The project focuses on understanding accident severity, temporal patterns, geographical hotspots, weather conditions, and reported accident circumstances using Python-based data analysis and visualization.

---

## Project Overview

The US Accidents dataset contains millions of accident records collected across the United States.

The objective of this project is to analyze the dataset and identify meaningful patterns related to:

- Accident severity
- Time and date patterns
- State and city hotspots
- Weather conditions
- Road and traffic circumstances
- Accident duration
- Visibility
- High-severity accident patterns

Because the dataset is very large, **chunk-based processing** was used to perform analysis efficiently without loading the entire dataset into memory at once.

---

## Dataset

**Dataset:** US Accidents

**Source:** Kaggle — Sobhan Moosavi

Dataset link:  
https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents

The dataset contains **7,728,394 accident records** and 46 original attributes.

---

## Data Cleaning & Preprocessing

The project included several data quality checks and preprocessing steps:

- Missing-value analysis
- Duplicate-record detection
- Data-type verification
- Geographic coordinate validation
- Accident severity validation
- Numerical-range validation
- Date/time standardization
- Accident duration calculation
- Handling selected categorical missing values

The cleaned dataset was validated to ensure:

- No missing accident IDs
- No invalid severity values
- No invalid latitude/longitude values
- No negative accident distances
- No negative accident durations

---

## Feature Engineering

Additional features were created to support deeper analysis:

- `Year`
- `Month`
- `Month_Name`
- `Day`
- `Day_of_Week`
- `Hour`
- `Is_Weekend`
- `Time_Period`
- `Accident_Duration_Hours`
- `Duration_Category`

These features helped identify temporal and duration-based accident patterns.

---

## Analysis & Visualizations

The project analyzes:

### 1. Accident Severity
The distribution of accidents across Severity 1–4 was examined.

### 2. Accident Trends by Year
Yearly accident patterns were analyzed to identify changes over time.

### 3. State-Level Analysis
The states with the highest number of reported accidents were identified.

### 4. Time-of-Day Analysis
Accident frequency was analyzed across all 24 hours of the day.

### 5. High-Severity Accident Windows
Day-and-hour combinations with unusually high proportions of Severity 3 and 4 accidents were identified.

### 6. Weather & Severity
Different weather conditions were compared based on their association with high-severity accidents.

### 7. Accident Circumstances
The `Description` field was analyzed using keyword-based patterns to identify reported circumstances such as:

- Lane blockage
- Shoulder blockage
- Traffic congestion and delays
- Vehicle crashes/collisions
- Ramp or exit incidents
- Weather-related conditions
- Emergency response
- Construction or road work
- Stationary or disabled vehicles

### 8. Geographic Hotspots
Cities with the highest numbers of reported accidents were identified.

---

## Key Findings

- The dataset contains **7,728,394 accident records**.
- **19.46%** of accidents were classified as high severity (Severity 3 or 4).
- Friday recorded the highest number of reported accidents.
- Accident patterns vary significantly by time of day and day of the week.
- Certain weekend morning periods showed substantially higher high-severity accident shares.
- Thunderstorm-related weather conditions showed some of the highest high-severity accident proportions among sufficiently frequent weather conditions.
- Ramp/exit incidents, lane blockages, and shoulder blockages showed strong associations with high-severity accidents.
- Traffic congestion and delay-related descriptions were very common but showed a comparatively low proportion of high-severity accidents.
- California had the highest number of reported accidents in the dataset.

> **Note:** Circumstance and weather findings represent associations observed in the dataset and should not be interpreted as proof of causation.

---

## Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Google Colab**
- **Kaggle Dataset**

---

## Repository Contents

```text
SCT_DS_4/
│
├── SCT_DS_Task4.ipynb
│
├── 01_severity_distribution.png
├── 02_accidents_by_year.png
├── 03_top_10_states.png
├── 04_accidents_by_hour.png
├── 05_high_severity_time_windows.png
├── 06_weather_severity.png
├── 07_circumstances_severity.png
└── 08_top_accident_cities.png
