# MainCraft-Internship

## Task 1: Student Performance Analysis

### Overview
This project performs a comprehensive analysis of student performance using the **student-mat dataset**. The analysis explores various factors that influence student academic performance, including study habits, demographics, and social factors.

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

### Tools & Libraries Used
- **Pandas**: Data manipulation and analysis
- **Matplotlib**: Data visualization
- **Seaborn**: Advanced statistical graphics
  - Plot style: whitegrid for professional appearance

### Key Findings
1. Males perform slightly better than females on average
2. Study time has a weak positive correlation with grades (0.0978)
3. No missing data issues; dataset is well-maintained
4. Grade performance shows moderate variance across students
5. Multiple factors influence student performance beyond just study time

### Files
- `maincraft_task1.ipynb`: Jupyter notebook with complete analysis and code
- `README.md`: This documentation file

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

### Insights & Recommendations
- **Study habits** are not the only predictor of success; consider socioeconomic factors
- **Gender differences** in performance may warrant further investigation
- **Support systems** (family and school support) should be explored further
- **Data-driven interventions** can be tailored based on this analysis

---

*MainCraft Internship - Task 1 Completed*
