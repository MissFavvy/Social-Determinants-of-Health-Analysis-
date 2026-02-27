# Social Determinants of Health Analysis

<img width="457" height="173" alt="image" src="https://github.com/user-attachments/assets/fc902ed0-e345-48b5-a19f-b1a8cf3c2659" />

INTRODUCTION

This project presents an exploratory and analytical study of a health dataset with a focus on understanding demographic and socioeconomic characteristics, particularly employment status, education level, salary, and credit score eligibility. The analysis was conducted using Excel to clean, transform, analyze, and visualize the data in order to uncover realistic patterns that reflect real-world financial and social behavior.
The goal of this analysis is not only to build charts, but to tell a clear data story, highlighting how employment and education influence credit eligibility while ensuring data consistency and transparency.

PROBLEM STATEMENT

The dataset contains multiple demographic and financial attributes that requires proper cleaning and structuring to support meaningful analysis. Without preprocessing, inconsistencies such as duplicated employment categories, non-applicable credit scores, and ungrouped numerical values make interpretation difficult.
The goal of this project is to:

1. Clean and standardize key variables
2. Analyze age group distribution, employment status, education level, and credit score
3. Understand the relationship between employment, education, and credit score eligibility
4. Identify realistic socioeconomic patterns while ensuring data consistency
5. Build a clear, story-driven Excel dashboard for insights and decision-making
   
TOOLS USED

1.  Excel

SKILLS DEMONSTRATED

1. Data cleaning and preprocessing
2. Feature engineering using Excel formulas
3. Exploratory data analysis (EDA)
4. Pivot table analysis
5. Dashboard storytelling
6. Logical validation of data patterns

DATA EXPLORATION AND CLEANING

Initial data exploration revealed inconsistencies, formatting issues and raw numerical values that affected analysis accuracy and required transformation for effective analysis.
Cleaning Actions Performed;
1: Employment Status Cleaning:
Duplicate employment categories were caused by extra spaces in the Employment Status column.
To resolve this, the following formula was applied to Column1:
=TRIM(I2) 
Autofilled down I column, adjusting row refs.
This ensured consistent categorization and eliminated duplicated values during analysis.
2. Credit Score Eligibility Handling:
Some individuals had non-applicable credit score values, particularly students and unemployed individuals. These were retained and reclassified appropriately as “Not Eligible” rather than removed to reflect real-world credit eligibility .
3. Unknown Blood Types:
A small number of unknown blood type values were observed, 8 precisely. These values were retained but not represented in chart.

Raw Dataset
<img width="767" height="135" alt="image" src="https://github.com/user-attachments/assets/0f319a10-150e-41b0-82b7-79e4a251fb76" />

Cleaned Dataset
<img width="767" height="159" alt="image" src="https://github.com/user-attachments/assets/2c1601c6-a0e8-4610-9084-440b051a472e" />

Derived Columns Created: To enhance analysis and storytelling, the following columns were created:

1. Credit Score Category
Purpose: Categorize credit scores into categories
Formula:
=IFS(
N2="N/A","Not Eligible",
N2<580,"Poor",
N2<=669,"Fair",
N2<=739,"Good",
N2<=740,"Very Good",
N2>=800,"Excellent"
)
Autofilled down O column (Credit Score Category), adjusting row refs.
2. Age Group
Purpose: Categorize ages into groups
Formula:
=IFS(
C2<13,"Child",
C2<20,"Teen",
C2<40,"Young Adult",
C2<65,"Adult",
C2>=65,"Older Adult"
)
Autofilled down D column (Age Group), adjusting row refs.
3. Salary Band
Purpose:  Categorize salary into bands
Formula:
=IFS(
K2<30000,"Low",
K2<=50000,"Medium",
K2<=80000,"High",
K2>80000,"Very High"
)
Autofilled down L column (Salary Band), adjusting row refs.
4. Year
=YEAR(P2)
Autofilled down Q column, adjusting row refs.
5. Month
=TEXT(P2,"mmm")
Autofilled down R column, adjusting row refs.

DATA ANALYSIS

The analysis focused on identifying relationships between employment status, education level, salary, and credit score eligibility. Pivot tables were used to examine:

1. Age group distribution
2. Credit score distribution
3. Employment status versus credit score/ salary band
4. Education level versus credit score
Patterns were carefully reviewed to ensure they reflected logical real-world behavior, rather than treated as anomalies or forced interpretations.

DATA VISUALIZATION

A multi-page Excel dashboard was developed, with each page telling a specific story:
1. Patient Admissions Overview
Story:
“This page represents patient admissions with clear demographic, health, and financial patterns.”
This page answers:
How many patients?
Who they are (gender, employment)?
How admissions change over time?
<img width="437" height="184" alt="image" src="https://github.com/user-attachments/assets/17733da2-fb7a-4b97-9672-21937931642b" />

2. Demographic Profile of Patients.
Story:
“Most admissions come from specific age groups, cities, and education levels.”
This page answers:
Who are the patients?
Where are they coming from?
Which age groups dominate?
What is their educational status?
<img width="438" height="178" alt="image" src="https://github.com/user-attachments/assets/877193bf-2644-464b-83fb-d7908100e682" />

3. Health Conditions Driving Patient Admissions.
Story:
“Certain health conditions drive admissions, and they vary by age and gender.”
This page answers:
What health issues are common?
Who is most affected?
<img width="444" height="184" alt="image" src="https://github.com/user-attachments/assets/825fd6b7-1bd9-495c-b796-4e4644ea0908" />

4. Socioeconomic and credit score of Patients.
Story:
“Patients’ financial, education and employment status show patterns that may influence access to care and risk.”
This page connects:
Salary
Employment
Education &
Credit score
<img width="442" height="207" alt="image" src="https://github.com/user-attachments/assets/c9d9f142-1f15-48fd-9bfa-a4486b71252d" />

5. Risk Indicators and Vulnerable Patient Groups.
Story:
“Some groups appear more vulnerable based on age, income, credit score, and health conditions.”
<img width="443" height="211" alt="image" src="https://github.com/user-attachments/assets/3d5d1cba-0671-4945-ac45-90da7a5ef0c8" />

Column, stacked column, line and donut charts were used to clearly compare categories and highlight relationships.

INSIGHTS

1. Over 68% of individuals with a salary of $0 are unemployed, confirming logical data consistency rather than data entry errors.
2. Credit ineligibility is concentrated mainly among unemployed and students.
3. Employment status influences credit eligibility more than education level

RECCOMENDATIONS

1. Financial inclusion programs should prioritize unemployed individuals and students, who are more likely to be credit-ineligible.
2. Employment-driven interventions may have a greater impact on improving credit eligibility than education alone.
3. Credit awareness and financial literacy programs could support long-term financial stability.
4. Future datasets should aim for improved completeness in financial and medical attributes.

This analysis supports data-driven decision-making in healthcare and financial risk assessment.
   
