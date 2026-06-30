# MainCraft-Internship

## Overview
This repository contains completed tasks for the MainCraft Internship program, focusing on data analysis and exploratory data analysis (EDA) using Python libraries like Pandas, Matplotlib, and Seaborn. The work demonstrates practical end-to-end EDA, feature engineering, and visualization skills applied to real-world datasets.

---

## Task 1: Student Performance Analysis

### Overview
This project performs a comprehensive analysis of student performance using the **student-mat dataset**. The analysis explores various factors that influence student academic performance, including demographics, parental background, study patterns, and extracurricular factors.

### Dataset
- **Dataset Name**: student-mat
- **Total Records**: 395 students
- **Total Features**: 33 columns
- **No Missing Values**: Dataset is clean with no null values

### Data Features
The dataset includes:
- **Personal Information**: School, sex, age, address, family size, parental status
- **Parental Background**: Mother's and Father's education, occupation
- **Academic Information**: Travel time, study time, failures, previous grades (G1, G2)
- **Support Systems**: School support, family support, paid classes
- **Lifestyle Factors**: Activities, internet access, romantic relationships, alcohol consumption
- **Performance Metrics**: Final grade (G3), absences, health status

### Key Analyses Performed

#### 1. Data Exploration & Cleaning
- ✅ Loaded dataset using Pandas with semicolon separator
- ✅ Checked for missing values (confirmed no nulls)
- ✅ Removed duplicate records
- ✅ Inspected data shape and types
- ✅ Validated data integrity by checking unique values

#### 2. Statistical Insights
- **Average Final Grade (G3)**: 10.42
- **Students Scoring Above 15**: 40 students
- **Study Time & Performance Correlation**: 0.0978 (weak positive correlation)
- **Gender Performance**: 
  - Female average: 9.97
  - Male average: 10.91
  - *Males perform slightly better on average*

#### 3. Grade Trajectory Analysis
- Tracked student improvement/decline between first and second period grades
- Calculated `grade_trajectory` = G2 - G1 for each student

#### 4. Visualizations

##### Distribution of Final Grades
- Histogram with KDE (Kernel Density Estimation)
- Color: Royal Blue
- Shows grade distribution across all students

##### Study Time vs Final Grades
- Scatter plot with regression line
- Shows weak positive correlation between study time and performance
- Helps identify study effectiveness patterns

##### Gender Performance Comparison
- Bar chart comparing average G3 scores by gender
- Visualizes performance gap between males and females

##### Correlation Matrix
- Heatmap of numeric features
- Identifies relationships between various factors and academic performance
- Includes color-coded correlation strengths

### Key Findings
1. Males perform slightly better than females on average
2. Study time has a weak positive correlation with grades (0.0978)
3. No missing data issues; dataset is well-maintained
4. Grade performance shows moderate variance across students
5. Multiple factors influence student performance beyond just study time

### Files
- `maincraft_task1.ipynb`: Jupyter notebook with complete analysis and code

### How to Run
1. Ensure you have the required libraries installed:
   ```
   pip install pandas matplotlib seaborn
   ```
2. Load the student-mat.csv dataset with semicolon separator
3. Run the notebook cells sequentially to:
   - Load and clean the data
   - Perform statistical analysis
   - Generate visualizations
   - Export insights

### Tools & Libraries Used
- **Pandas**: Data manipulation and analysis
- **Matplotlib**: Data visualization
- **Seaborn**: Advanced statistical graphics (whitegrid style)

---

## Task 2: Titanic Survival Analysis

### Overview
This project performs exploratory data analysis (EDA) on the **Titanic dataset** to understand passenger survival patterns. The analysis investigates how demographic factors such as gender, passenger class, age, and family composition influenced survival rates.

### Dataset
- **Dataset Name**: train_and_test2.csv
- **Key Columns**: PassengerId, Age, Fare, Sex, SibSp, Parch, Survived, Pclass, Embarked
- **Data Cleaning**: Handled missing values in Age and Embarked columns

### Data Features
The dataset includes:
- **Passenger Information**: PassengerId, Name, Age
- **Demographic Data**: Sex, Passenger Class (Pclass)
- **Family Information**: SibSp (Siblings/Spouse aboard), Parch (Parents/Children aboard)
- **Ticket Information**: Ticket number, Fare paid
- **Embarkation**: Port of embarkation (C, Q, S)
- **Target Variable**: Survived (0 = Did not survive, 1 = Survived)

### Key Analyses Performed

#### 1. Data Auditing & Cleaning
- ✅ Identified and fixed missing values in the `Embarked` column (filled with mode)
- ✅ Renamed non-standard column (`2urvived` → `Survived`)
- ✅ Mapped numeric Sex values (0/1) to readable labels (Male/Female)
- ✅ Validated data integrity post-cleaning

#### 2. Statistical Insights

##### Survival Rate by Gender
- **Female**: 50.00% survival rate
- **Male**: 12.93% survival rate
- *Strong gender disparity showing priority to women for lifeboats*

##### Survival Rate by Passenger Class
- **1st Class**: 42.11% survival rate
- **2nd Class**: 31.41% survival rate
- **3rd Class**: 16.78% survival rate
- *Clear socio-economic stratification effect*

##### Survival Rate by Age Group
- **Child (0-12)**: 42.55% survival rate
- **Teenager (13-18)**: 30.30% survival rate
- **Young Adult (19-35)**: 23.80% survival rate
- **Adult (36-60)**: 26.99% survival rate
- **Senior (60+)**: 15.15% survival rate
- *Children prioritized; seniors had lowest survival rates*

#### 3. Feature Engineering
- **AgeGroup**: Segmented passengers into 5 demographic life stages for deeper analysis
- Enhanced understanding of protective patterns (e.g., "women and children first" policy)

#### 4. Visualizations

##### Survival by Gender
- Bar chart with coolwarm palette
- Shows stark survival probability difference between genders

##### Survival by Passenger Class
- Bar chart with Set2 palette
- Demonstrates structural class-based survival hierarchy

##### Age Distribution by Survival Status
- Stacked histogram showing passenger age distribution
- Colored by survival status (muted palette)
- Reveals age-based survival patterns

##### Combined Gender & Class Effect
- Multi-hue bar chart analyzing intersection of class and gender
- Shows how socio-economic status and gender jointly affected survival
- Uses pastel palette for clarity

### Key Findings
1. **Gender Disparity**: Female passengers had ~4x higher survival rate than males (50% vs 12.93%)
2. **Class Effect**: First-class passengers were ~2.5x more likely to survive than third-class passengers
3. **Age Priority**: Children and teenagers had higher survival rates than adults
4. **Intersectionality**: First-class women had drastically higher survival rates than third-class men
5. **Historical Validation**: Analysis confirms the "women and children first" evacuation policy and class-based resource allocation

### Files
- `Task2.ipynb`: Jupyter notebook with complete EDA, analysis, and visualizations

### How to Run
1. Ensure you have the required libraries installed:
   ```
   pip install pandas numpy matplotlib seaborn
   ```
2. Place the Titanic dataset (`train_and_test2.csv`) in the appropriate directory
3. Run the notebook cells sequentially to:
   - Load and clean the data
   - Perform statistical analysis
   - Generate demographic breakdowns
   - Visualize survival patterns
   - Draw conclusions

### Tools & Libraries Used
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical operations
- **Matplotlib**: Data visualization
- **Seaborn**: Advanced statistical graphics (ticks style for professional appearance)

---

## Task 3: Titanic Mini Exploratory Data Analysis (EDA)

### Overview
This deliverable (Task 3) provides a compact, focused EDA on the Titanic dataset with an emphasis on robust cleaning, advanced group-by analyses, and clear visual storytelling. The notebook demonstrates smart imputation, feature engineering (AgeGroup, FamilySize), and multi-dimensional survival insights.

> Deliverable Notebook: `Task3.ipynb`

### Dataset
- **Dataset Name**: train_and_test2.csv (same preprocessed file used across Titanic tasks)
- **Key Columns**: Passengerid, Age, Fare, Sex, sibsp, Parch, Pclass, Embarked, Survived
- **Notes**: The dataset included some non-standard column names (e.g., `2urvived`) that were standardized in the notebook. Missing values in `Age` (if present) are imputed with the mean and `Embarked` is filled with the mode.

### Key Analyses Performed

1. Environment setup and data loading with Pandas, NumPy, Matplotlib, and Seaborn.
2. Data cleaning and schema standardization:
   - Renamed non-standard columns, created `Sex_Label` mapping, and dropped extraneous tracking columns.
   - Imputed `Age` (mean) and `Embarked` (mode) where necessary.
3. Feature engineering:
   - `AgeGroup` (Child, Teenager, Young Adult, Adult, Senior)
   - `FamilySize` = `sibsp` + `Parch`
   - `Port_Label` mapping for embarkation codes
4. Group-by analyses answering targeted questions:
   - Survival rate by `AgeGroup`
   - Survival rate by embarkation port (`Port_Label`)
   - Survival rate by `FamilySize`
5. Visual storytelling with histograms, correlation heatmap, and survival-by-family-size bar chart.

### Representative Results (from the notebook)
- Survival Rate by Age Group:
  - Child: 42.55%
  - Teenager: 30.30%
  - Young Adult: 23.80%
  - Adult: 26.99%
  - Senior: 15.15%

- Survival Rate by Embarkation Port:
  - Cherbourg: 34.44%
  - Queenstown: 24.39%
  - Southampton: 23.91%

- Survival Rate by Family Size (examples):
  - FamilySize = 0: 20.63%
  - FamilySize = 1: 37.87%
  - FamilySize = 3: 48.84%

### Visualizations
- Age distribution histogram with KDE
- Correlation heatmap of numeric features (Age, Fare, Sex, Pclass, FamilySize, Survived)
- Bar chart showing survival probability by `FamilySize`

### Key Takeaways
- Small family groups (1–3 members) tend to have higher survival probabilities; very large families and solo travelers show lower survival.
- `Pclass` and `Fare` show notable relationships with survival, reinforcing socio-economic effects.
- Survival rates differ by embarkation port, which likely reflects passenger socio-economic distributions.

### Files
- `Task3.ipynb`: Jupyter notebook with the Task 3 deliverable analysis

### How to Run
1. Ensure you have the required libraries installed:
   ```
   pip install pandas numpy matplotlib seaborn
   ```
2. Place `train_and_test2.csv` in the same working directory as the notebook.
3. Run the notebook cells sequentially to reproduce the analysis and plots.

---

## Repository Structure
```
MainCraft-Internship/
├── README.md                    # This file
├── maincraft_task1.ipynb        # Task 1: Student Performance Analysis
├── Task2.ipynb                  # Task 2: Titanic Survival Analysis
└── Task3.ipynb                  # Task 3: Titanic Mini EDA (deliverable)
```

## Summary
This internship project demonstrates proficiency in:
- **Data Cleaning & Preprocessing**: Handling missing values, renaming columns, data validation
- **Exploratory Data Analysis**: Statistical analysis and insight generation
- **Feature Engineering**: Creating meaningful segments for deeper analysis
- **Data Visualization**: Professional, publication-ready charts and graphs
- **Python Libraries**: Pandas, NumPy, Matplotlib, and Seaborn

Each task involves real-world datasets and provides actionable insights through rigorous analytical approaches.

---

*MainCraft Internship - Tasks Completed*
