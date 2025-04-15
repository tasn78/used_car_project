# Assignment 2 – Used Car Price Analysis

This project performs data cleaning, feature engineering, and exploratory analysis on a dataset of used cars, following structured data science workflows.

## Project Structure


## Tasks Completed

### (a) Handling Missing Values
- **Dropped** rows with missing values in `Mileage`, `Engine`, and `Seats` (each had <1% missing).
- **Dropped** `New_Price` due to ~85% missing values.
- Avoided blind imputation in favor of justified data integrity.

### (b) Unit Removal
- Removed units from:
  - `Mileage` → `Mileage_kmpl`
  - `Engine` → `Engine_CC`
  - `Power` → `Power_bhp`
- Renamed columns accordingly to retain clarity of measurement.

### (c) One-Hot Encoding
- Categorical variables `Fuel_Type`, `Transmission`, and `Owner_Type` were one-hot encoded using `pd.get_dummies()`.

### (d) Feature Engineering
- **Car_Age**: Calculated as `2025 - Year`
- **Kms_per_Year**: Derived as `Kilometers_Driven / Car_Age`
- **Is_Luxury**: Boolean flag for brands like BMW, Audi, Mercedes
- **Optional**: Added `Power_per_CC` and `Price_per_bhp` for performance profiling

### (e) Data Operations (R-equivalent in Python)
Performed all six operations:
- `select`: Extracted key columns
- `filter`: Subset cars by age and price
- `rename`: Renamed columns for clarity
- `mutate`: Added new features (`Car_Age`, etc.)
- `arrange`: Sorted by key variables
- `summarize + group_by`: Aggregated price and mileage by luxury status

---

## Files

- `train.csv`: Original dataset
- `cleaned_used_car_data.csv`: Final dataset used for analysis
- `assignment2_analysis.ipynb`: All steps with code, comments, and markdown explanations

---

## Submission Info

> GitHub repository submitted for Assignment 2 as per instructions.

