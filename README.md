# Healthcare-data-analysis-using-excel-and-power-BI
An interactive Power BI dashboard for analyzing cirrhosis patient data, including demographic, clinical, laboratory, treatment, insights, and recommendations.
DATA:
The dataset was sourced from the Mayo Clinic and is based on a study of primary biliary cirrhosis (PBC) of the liver conducted between 1974 and 1984. Mayo Clinic is a private American academic medical centre focused on integrated healthcare, education, and research.
Variable Name
	Role	Type	Description	Units	Missing Values
ID	ID	Integer	unique identifier		no
N_Days	Other	Integer	number of days between registration and the earlier of death, transplantation, or study analysis time in July 1986		no
Status	Target	Categorical	status of the patient 
C (censored), 
CL (censored due to liver tx), or 
D (death)		no
Drug	Feature	Categorical	type of drug D-penicillamine or placebo		yes
Age	Feature	Integer	age	days	no
Sex	Feature	Categorical	M (male) or 
F (female)		no
Ascites	Feature	Categorical	presence of ascites 
N (No) or 
Y (Yes)		yes
Hepatomegaly	Feature	Categorical	presence of hepatomegaly 
N (No) or 
Y (Yes)		yes
Spiders	Feature	Categorical	presence of spiders 
N (No) or 
Y (Yes)		yes
Edema	Feature	Categorical	presence of edema
N (no edema and no diuretic therapy for edema), 
S (edema present without diuretics, or edema resolved by diuretics), or 
Y (edema despite diuretic therapy)		no
Bilirubin	Feature	Continuous	serum bilirubin	mg/dl	no
Cholesterol	Feature	Integer	serum cholesterol	mg/dl	yes
Albumin	Feature	Continuous	albumin	gm/dl	no
Copper	Feature	Integer	urine copper	ug/day	yes
Alk_Phos	Feature	Continuous	alkaline phosphatase	U/liter	yes
SGOT	Feature	Continuous	SGOT	U/ml	yes
Tryglicerides	Feature	Integer	Tryglicerides		yes
Platelets	Feature	Integer	platelets per cubic	ml/1000	yes
Prothrombin	Feature	Continuous	prothrombin time	s	yes
Stage	Feature	Categorical	histologic stage of disease (1, 2, 3, or 4)		yes

PROCEDURE:
I.	Data cleaning
1.Checked for duplicates-no duplicates found
2.Checked for missing vales -missing values found
3.methods for dealing with missing values-
Numerical variables
For variables such as:
Variable	Imputation performed	Value imputed
Cholesterol	Median	309.5
Copper	Median	73
Alk_Phos	Median	129
SGOT	Median	114.7
Tryglicerides	Median	108
Platelets	Median	251
Prothrombin	Median	10.6
Stage	Median	3

Medical measurements often have skewed distributions and extreme values. The median is less affected by those extremes. 
Categorical variables
For:
•	Drug -Unknown
•	Ascites -Unknown 
•	Hepatomegaly -Unknown 
•	Spiders -Unknown 
•	Edema -Unknown 
4. Standardizing variables
•	The Sex categories were standardized by converting “F” to “Female” and “M” to “Male” to ensure consistency and improve data readability.
•	Status- 
C = Censored 
CL = Censored due to liver transplant 
D = Death
•	Ascites-
Y=Present
N=Absent
•	Hepatomegaly-
Y=Present
N=Absent
•	Spiders-
Y=Present
N=Absent
•	Edema-
N = No edema 
S = Edema present/controlled 
Y = Edema refractory to diuretics
5.Creating calculated fields
The original Age variable was recorded in days. To make the variable easier to   interpret and use in the analysis, a new calculated field, “Age_years”, was created by dividing age in days by 365.25. Rounded to the nearest whole number. Then they are grouped into three categories to make better demographic analysis under the column name  “  Age_category ”. The following age groups were used:

Age Range	Age Category
25–39	Young Adulthood
40–59	Middle Adulthood
60+	Older Adulthood

II.	DATA ANALYSIS

Pivot Tables were created using Excel to analyse the cleaned dataset and identify relationships between different factors and patient status. The following Pivot Tables were prepared:

1.	Demographic Characteristics vs Patient Status 
•	Age Category 
•	Sex 
2.	Clinical Factors vs Patient Status 
•	Signs & Symptoms: Ascites, Hepatomegaly, Spiders, Edema 
•	Laboratory Measurements: Bilirubin, Cholesterol, Albumin, Copper, Alk_Phos, SGOT, Tryglicerides, Platelets, Prothrombin 
3.	Stage vs Patient Status 
•	Stage 
4.	Treatment vs Patient Status 
•	Drug

III.	DATA VISUALIZATION AND INTERPRETATION

The cleaned patient dataset was analyzed and visualized using Microsoft Power BI. The dashboard was designed to provide a clear and interactive view of patient demographics, clinical characteristics, laboratory measurements, treatment information, disease stage, and patient status. Different types of visualizations were selected according to the nature of the variables and the purpose of the analysis.

1.	Patient Health Executive Overview
The first dashboard page provides an overall summary of the patient dataset. 
•	Key Performance Indicator (KPI) cards are used to display the total number of patients, number of deaths, number of censored patients, censored due to liver transplant. These indicators allow users to understand the main characteristics of the dataset immediately.
•	Button slicer – used to indicate and filter Gender.
•	Input slicer – used to filter Patient Status and Age Category by entering or selecting values.
•	List slicer – used to select and filter Stage and Drug from a list of available categories.
•	A Donut Chart is used to display the distribution of patients according to their status. The chart compares the proportion of patients classified as Death, Censored, or Censored due to liver transplant.

2.	Demographic and Clinical Analysis
The second page focuses on demographic and clinical characteristics associated with patient status.
•	KPI cards provide summary information of average age of patients
•	Slicers for filtering across clinical conditions such as ascites, hepatomegaly,  spiders, edema .
•	A Stacked Column Chart is used to compare patient counts across age categories. The chart helps identify which age groups contain the largest number of patients and how patient status varies between them.
•	A 100% Stacked Bar Chart compares patient status by gender. This provides an easy visual comparison of outcomes between the two gender categories.
•	A Pie Chart is used to show the distribution of patients with and without ascites. Because ascites contains a small number of categories, a pie chart provides a simple representation of the proportion of patients in each group.
•	A Clustered Bar Chart is used to examine hepatomegaly in relation to patient status. The use of percentages allows the distribution of status within the clinical categories to be compared more easily.
•	A Waterfall Chart displays the distribution of patients according to the presence or absence of spiders. This provides a quick overview of this clinical characteristic.
•	A Ribbon Chart is used to visualize changes in the relative ranking of edema categories across patient status. This helps users compare the composition of clinical conditions between outcome groups.

3.	Laboratory and Treatment Analysis
The third dashboard page focuses on laboratory measurements and treatment information.
•	KPI cards summarize important laboratory measurements, including average of bilirubin, cholesterol, albumin, copper, alkaline phosphatase, SGOT, triglycerides, platelets, and prothrombin levels.
•	A Matrix Visualization provides a detailed comparison of laboratory measurements between patient-status groups. The matrix contains the average values of bilirubin, cholesterol, albumin, copper, alkaline phosphatase, SGOT, triglycerides, platelets, and prothrombin.
•	A Scatter Chart is used to examine the relationship between SGOT and bilirubin. Patient status is used as the legend so that the distribution of the two outcome groups can be compared. Scatter plots are appropriate for laboratory data because both variables are numerical and the visualization can reveal patterns, clustering, or possible relationships between measurements.
•	Funnel Chart is used to compare different stages with patient status. 
•	Treemap is used to compare different drugs with patient status.
•	Slicers for Status, Stage, and Drug allow users to investigate laboratory and treatment patterns for specific patient groups.



4.	 Key Insights

•	Insights, the page is used to present the key findings identified from the patient health data analysis. It highlights the major patterns and relationships observed across demographic, clinical, laboratory, treatment, and disease-stage factors.
•	Insights include: 
⭐ Demographics
•	Age: Middle adulthood has the highest deaths (101) followed by older adulthood (88).
•	Sex: Females account for most deaths (137) compared to males (24) due to dataset imbalance.
⭐ Clinical Signs
•	Ascites: Present ascites is seen in 24 deaths, indicating more advanced disease.
•	Hepatomegaly: Hepatomegaly appears in 88 deaths, showing strong association with poor outcomes.
•	Spiders: Spider angiomas occur in 52 deaths, marking visible liver deterioration.
•	Edema: Refractory edema is linked to severe disease with 20 deaths, while controlled edema shows 26 deaths.
⭐ Treatment
•	Drug: Mortality is similar between D penicillamine (65 deaths) and placebo (60 deaths), showing no clear survival benefit.
⭐ Disease Stage
•	Stage: Stage 4 has the highest mortality (84 deaths), followed by stage 3 (52 deaths).
⭐ Key Lab Indicators
•	Bilirubin: Death cases show much higher bilirubin (5.54) than censored (1.57).
•	Albumin: Albumin is lower in deaths (3.36) compared to censored (3.59).
•	Alkaline Phosphatase: Death cases have significantly higher values (2295) than censored (1490).
•	Copper: Copper is elevated in deaths (121) versus censored (68).
•	Prothrombin Time: Higher in deaths (11.18) than censored (10.45).
•	Platelets: Slightly lower in deaths (243) compared to censored (260).
•	Cholesterol: Higher in deaths (385) than censored (320).
•	SGOT: Elevated in deaths (136) compared to censored (109).
•	Triglycerides: Higher in deaths (131) than censored (110).

5.	Recommendations
The page is used to provide practical recommendations based on the key insights identified from the analysis. It translates the findings into useful actions, such as giving greater attention to patients with advanced disease stages, monitoring important clinical symptoms and laboratory indicators, providing closer follow-up for high-risk patients, and carefully evaluating treatment outcomes.
⭐ Demographics
•	Age: Prioritise early monitoring for middle aged and older adults since they show the highest mortality.
•	Sex: Ensure balanced sampling in future studies to avoid female dominant datasets that may skew interpretation.
⭐ Clinical Signs
•	Ascites: Strengthen routine screening and early management of ascites to prevent progression.
•	Hepatomegaly: Treat hepatomegaly as a red flag indicator and escalate care when present.
•	Spiders: Use spider angiomas as supportive evidence of advancing liver disease and monitor closely.
•	Edema: Pay special attention to refractory edema, as it signals severe disease requiring urgent intervention.
⭐ Treatment
•	Drug: Since D penicillamine and placebo show similar outcomes, consider reassessing treatment protocols and exploring alternative therapies.
⭐ Disease Stage
•	Stage: Focus on early-stage detection and intervention to prevent progression to stage 4, where mortality is highest.
⭐ Key Lab Indicators
•	Bilirubin: Use rising bilirubin as an early warning sign for deterioration and intensify monitoring.
•	Albumin: Address low albumin promptly through nutritional and medical support to improve liver function.
•	Alkaline Phosphatase: Treat high alkaline phosphatase as a marker of severe disease and investigate underlying causes.
•	Copper: Monitor copper levels regularly, as elevated values indicate metabolic imbalance.
•	Prothrombin Time: Use prolonged prothrombin time to identify patients at risk of bleeding complications.
•	Platelets: Watch for declining platelets as a sign of portal hypertension or worsening liver function.
•	Cholesterol: Consider high cholesterol as part of the metabolic profile of advanced disease.
•	SGOT: Use elevated SGOT to track liver inflammation and adjust care accordingly.
•	Triglycerides: Monitor triglycerides as part of overall metabolic assessment in severe cases.

	Interactive Features
The Power BI report contains several interactive features to improve data exploration. Slicers allow users to filter the dashboard by patient status, age category, sex, disease stage, and drug treatment.

A Page Navigator is positioned at the top of each dashboard page. It allows users to move easily between the Executive Overview, Demographic and Clinical Analysis, Laboratory and Treatment Analysis, and Insights and Recommendations pages.

A Reset Button is also included so that users can return the dashboard to its default filter state after applying different selections.
These interactive features make the dashboard more user-friendly and allow the same dataset to be analyzed from multiple perspectives.

6.	Overall Visualization Approach

The visualization strategy was designed to match each visual with the type of information being presented. KPI cards provide quick numerical summaries, bar and column charts support category comparisons, pie and donut charts display proportions, line charts represent ordered disease-stage patterns, treemaps show treatment distributions, scatter charts examine relationships between numerical laboratory measurements, and matrix visualizations provide detailed comparisons.
Overall, the Power BI dashboard transforms the cleaned patient dataset into an interactive analytical report. It enables users to explore demographic characteristics, clinical conditions, laboratory measurements, treatment patterns, disease stages, and patient outcomes in a clear and structured manner.
