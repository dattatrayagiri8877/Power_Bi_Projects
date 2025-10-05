# Power_Bi_Projects
Power BI is a cloud-based data analytics tool that helps you transform raw data into meaningful insights using interactive dashboards, reports, and visuals.

🩺 Power BI Project: Heart Disease Analysis Dashboard

🟩 1. Project Objective

To analyze health data of patients and identify key factors influencing heart disease risk.
The dashboard helps doctors, researchers, and hospitals monitor patterns and predict the likelihood of heart disease.

🟩 2. Tools Used

Power BI Desktop – for data analysis and visualization

Power Query – for data cleaning

DAX (Data Analysis Expressions) – for custom measures

Excel/CSV – as data source

🟩 3. Dataset Description

Typical dataset (e.g., from Kaggle or UCI Repository) includes:

Column Name	Description
Age	Age of the patient
Sex	Male / Female
ChestPainType	Type of chest pain (TA, ATA, NAP, ASY)
RestingBP	Resting blood pressure (mm Hg)
Cholesterol	Serum cholesterol (mg/dl)
FastingBS	Fasting blood sugar (1 = >120 mg/dl, 0 = normal)
RestingECG	Electrocardiographic results
MaxHR	Maximum heart rate achieved
ExerciseAngina	Exercise-induced angina (Y/N)
Oldpeak	ST depression induced by exercise
ST_Slope	Slope of the peak exercise ST segment
HeartDisease	Target variable (1 = Disease, 0 = No Disease)
🟩 4. Data Preparation (Power Query Steps)

Import dataset (CSV or Excel).

Remove duplicates and missing values.

Convert categorical columns (like Sex, ChestPainType) to text.

Create calculated columns for insights (e.g., Age Groups).

Load cleaned data into Power BI.

🟩 5. Data Modeling

Only one table needed (flat structure).

You can add an extra table for Age Groups or Risk Categories if desired.

Create relationships if using multiple tables (e.g., Patient → Hospital).

🟩 6. DAX Measures (Examples)
Total Patients = COUNT(HeartData[Age])

Patients with Heart Disease = CALCULATE(COUNT(HeartData[HeartDisease]), HeartData[HeartDisease] = 1)

Heart Disease % = DIVIDE([Patients with Heart Disease], [Total Patients]) * 100

Average Age = AVERAGE(HeartData[Age])

Average Cholesterol = AVERAGE(HeartData[Cholesterol])

🟩 7. Dashboard Visuals
Visualization	Purpose
Card Visuals	Total Patients, % with Heart Disease, Avg Age, Avg Cholesterol
Bar Chart	Heart Disease by Age Group
Donut Chart	Heart Disease by Gender
Column Chart	Heart Disease count by Chest Pain Type
Line Chart	Relationship between MaxHR and Age
Gauge	Average Cholesterol Level
Slicer	Filters – Gender, Age Group, Chest Pain Type
🟩 8. Key Insights

✅ Higher heart disease rates among males.
✅ Risk increases with age > 45 years.
✅ High cholesterol and blood pressure are major contributors.
✅ Patients with asymptomatic chest pain (ASY) show higher risk.
✅ Lower MaxHR often indicates presence of heart disease.

🟩 9. Dashboard Layout (Suggestion)

Top Section: KPIs (cards for total patients, % heart disease, avg age, avg cholesterol)

Left Panel: Filters/Slicers

Center Area: Bar/Column charts for age and chest pain

Right Side: Donut (Gender) + Gauge (Cholesterol)

Bottom: Line chart for Heart Rate vs Age

🟩 10. Project Outcome

The Heart Disease Analysis Dashboard helps visualize and interpret patterns in health data.
Doctors and analysts can:

Identify high-risk patients quickly.

Understand demographic trends.

Support preventive healthcare decisions.

🟩 11. Future Enhancements

Integrate machine learning predictions (using Python in Power BI).

Add real-time hospital data connection.

Build a Power BI App for hospital administrators.
