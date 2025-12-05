# CS210 Term Project – Health Data Exploration

**Student**: Beyza Balota  
**Student ID**: 31232  
**Course**: CS210 – Introduction to Data Science  
**Project Title**: Investigating Possible Correlations Between Sleep, Steps, and Menstrual Cycles

---

## Overview

This project explores the potential relationships between menstrual cycles, sleep quality, and physical activity (step count) using personal Apple Health data. The motivation stems from a desire for increased self-awareness and curiosity about how daily habits might influence reproductive health.

Due to the limited size and time span of the dataset (less than a year's worth of personal health records), the results remain inconclusive. However, the project serves as a foundational analysis and proof of concept for more comprehensive research in the future.

---

## Dataset Source

- **Origin**: Exported from Apple Health (iPhone)
- **Format**: XML file and manually extracted CSVs
- **Data Types Used**:
  - Sleep Analysis (`HKCategoryTypeIdentifierSleepAnalysis`)
  - Step Count (`HKQuantityTypeIdentifierStepCount`)
  - Menstrual Cycle (`HKCategoryTypeIdentifierMenstrualFlow`)
- **Privacy Note**:  
  This dataset contains **personal and sensitive health information**. To protect privacy, values have been masked or slightly modified. All identifiers and raw data are anonymized.

---

## Methodology

### 1. Data Cleaning
- Parsed Apple Health's XML export using `ElementTree`.
- Extracted relevant records and converted them into:
  - `sleep_data.csv`
  - `step_data.csv`
  - `menstrual_data.csv`
- Saved cleaned data locally as `.csv` files.

### 2. Aggregation & Merging
- Resampled both sleep and step data monthly.
- Computed monthly average sleep hours and step counts.
- Merged with menstrual cycle data based on month/year.

### 3. Preprocessing
- Filled missing cycle data with the mode.
- Replaced invalid (too low) sleep values with monthly mean (for values ≤ 2 hours).
- Created new `year` and `month` features from date.

### 4. Exploratory Data Analysis
- Correlation heatmaps
- Scatter plots and pair plots to visualize relationships

### 5. Model Building
- Performed regression with:
  - `Total Sleep Hours`
  - `Total Steps`
- Target variable: **Cycle Length**
- Used `DecisionTreeRegressor` with `GridSearchCV` for tuning `max_depth` and `min_samples_split`

---

## Key Observations

- **Correlation**: Sleep and step count had weak correlation with cycle length.
- **Sleep Data Issues**: Several months had incomplete or inaccurate sleep data due to Apple Watch syncing limitations.
- **Model Performance**:
  - Best R² Score: ~**-0.70** (very low, indicates poor fit)
  - Best MSE: ~**4.10**
  - Suggests that model couldn’t reliably predict cycle variation from current features
 
- Future work needed



