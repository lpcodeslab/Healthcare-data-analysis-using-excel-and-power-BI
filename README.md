# 🩺 Cirrhosis Patient Data Analysis | Power BI Dashboard

<p align="center">
  📊 <b>Healthcare Analytics</b> • 🧬 <b>Patient Outcomes</b> • 📈 <b>Power BI</b> • 🔍 <b>Data Insights</b>
</p>

---

## 📝 Project Overview

This project presents an **interactive Power BI dashboard** developed to analyze patient data from a study of **Primary Biliary Cirrhosis (PBC) of the liver** conducted at the Mayo Clinic between 1974 and 1984.

The dashboard transforms the cleaned patient dataset into an interactive analytical report covering **demographic characteristics, clinical conditions, laboratory measurements, treatment, disease stages, and patient outcomes**.

🎯 **Main Objective:**
To identify meaningful patterns in patient outcomes and transform healthcare data into clear visual insights and recommendations.

---

## 🗃️ Data Source

🏥 **Source:** Mayo Clinic
🧬 **Study:** Primary Biliary Cirrhosis (PBC) of the liver
📅 **Study Period:** 1974–1984
📊 **Data Focus:** Patient demographics, clinical characteristics, laboratory measurements, treatment, disease stage, and patient status.

---

## 🧹 Data Preparation & Cleaning

The dataset was prepared before analysis through several data-cleaning and transformation steps:

| 🔧 Process              | 📌 Description                                                                              |
| ----------------------- | ------------------------------------------------------------------------------------------- |
| 🔍 Duplicate Check      | No duplicate records were found                                                             |
| ❓ Missing Values        | Missing values were identified and handled                                                  |
| 📊 Numerical Imputation | Median values were used for selected numerical variables                                    |
| 🏷️ Categorical Values  | Missing categorical values were assigned as **Unknown**                                     |
| 🔄 Standardization      | Categories such as Sex, Status, Ascites, Hepatomegaly, Spiders, and Edema were standardized |
| 🎂 Age Transformation   | Age in days was converted into years                                                        |
| 👥 Age Categorization   | Patients were grouped into Young, Middle, and Older Adulthood                               |

### 📐 Age Categories

* 🧑 **Young Adulthood:** 25–39
* 👨 **Middle Adulthood:** 40–59
* 👴 **Older Adulthood:** 60+

---

## 📊 Data Analysis

Excel Pivot Tables were created to investigate relationships between **patient status** and different patient characteristics.

### 🔹 Analysis Areas

👥 **Demographic Characteristics**

* Age Category
* Sex

🩺 **Clinical Factors**

* Ascites
* Hepatomegaly
* Spiders
* Edema

🧪 **Laboratory Measurements**

* Bilirubin
* Cholesterol
* Albumin
* Copper
* Alk_Phos
* SGOT
* Triglycerides
* Platelets
* Prothrombin

🧬 **Disease Stage**

* Stage 1
* Stage 2
* Stage 3
* Stage 4

💊 **Treatment**

* D-penicillamine
* Placebo

---

# 📈 Power BI Dashboard

The dashboard consists of **five analytical pages**, each designed for a specific purpose.

---

## 🏠 1. Patient Health Executive Overview

Provides a high-level summary of the patient dataset using KPI cards, interactive slicers, and a donut chart.

📌 **Key Features:**

* 🔢 KPI cards for patient outcomes
* 🎛️ Gender button slicer
* 🔎 Patient Status and Age Category input slicers
* 📋 Stage and Drug list slicers
* 🍩 Donut chart showing patient-status distribution

---

## 👥 2. Demographic & Clinical Analysis

Focuses on demographic characteristics and clinical signs associated with patient status.

📌 **Visualizations include:**

* 📊 Stacked Column Chart – Age Category vs Patient Status
* 📊 100% Stacked Bar Chart – Gender vs Patient Status
* 🥧 Pie Chart – Ascites vs Patient Status
* 📊 Clustered Bar Chart – Hepatomegaly vs Patient Status
* 💧 Waterfall Chart – Spiders vs Patient Status
* 🎗️ Ribbon Chart – Edema vs Patient Status
* 🎛️ Clinical-condition slicers

---

## 🧪 3. Laboratory & Treatment Analysis

Examines laboratory measurements, disease stage, and treatment patterns.

📌 **Visualizations include:**

* 🔢 KPI cards for laboratory measurements
* 🧮 Matrix – Laboratory Measurements vs Patient Status
* 🔬 Scatter Chart – SGOT vs Bilirubin
* 🔻 **Funnel Chart** – used to compare different stages with patient status
* 🗂️ **Treemap** – used to compare different drugs with patient status
* 🎛️ Status, Stage, and Drug slicers

---

## 💡 4. Key Insights

This page presents the **major findings and patterns** identified from the patient health data.

### 👥 Demographic Insights

📌 **Age:** Middle adulthood has the highest number of deaths, followed by older adulthood.

📌 **Sex:** Females account for most deaths in the dataset, reflecting the female-dominant dataset composition.

### 🩺 Clinical Insights

💧 **Ascites:** Present ascites is observed among patients with death outcomes.

🫀 **Hepatomegaly:** Hepatomegaly appears frequently among death outcomes.

🕷️ **Spiders:** Spider angiomas are observed among patients with death outcomes.

🦵 **Edema:** Refractory edema is associated with severe disease outcomes.

### 💊 Treatment Insight

💊 Mortality is similar between **D-penicillamine and placebo** groups in this dataset, showing no clear survival benefit.

### 🧬 Disease Stage

⚠️ **Stage 4** has the highest mortality, followed by **Stage 3**, highlighting the importance of monitoring disease progression.

### 🧪 Laboratory Insights

The analysis shows differences between death and censored groups across several laboratory measurements, including:

🔺 Bilirubin
🔺 Alkaline Phosphatase
🔺 Copper
🔺 Cholesterol
🔺 SGOT
🔺 Triglycerides
🔺 Prothrombin Time

While:

🔻 Albumin
🔻 Platelets

show lower average values among death cases compared with censored cases.

---

# 🎯 5. Recommendations

The recommendations page translates the identified findings into practical areas for attention.

### 👥 Demographics

🎯 Prioritize monitoring of middle-aged and older adults due to their higher observed mortality.

⚖️ Encourage balanced sampling in future studies to reduce the effect of dataset imbalance.

### 🩺 Clinical Signs

💧 Strengthen routine monitoring of ascites.

🫀 Treat hepatomegaly as an important clinical warning sign.

🕷️ Monitor spider angiomas as a supportive indicator of advancing liver disease.

🦵 Give particular attention to refractory edema because of its association with severe disease.

### 💊 Treatment

🔬 Reassess treatment outcomes and explore alternative therapeutic approaches where appropriate, as similar mortality was observed between D-penicillamine and placebo groups.

### 🧬 Disease Stage

🚨 Focus on early detection and intervention to reduce progression toward advanced disease stages.

### 🧪 Laboratory Indicators

📈 Closely monitor important laboratory indicators, particularly bilirubin, alkaline phosphatase, copper, SGOT, cholesterol, triglycerides, and prothrombin time.

📉 Monitor lower albumin and platelet levels as part of overall patient assessment.

---

# 🎛️ Interactive Features

The Power BI report includes several interactive features that allow users to explore the data dynamically.

🎚️ **Slicers**

* Patient Status
* Age Category
* Gender
* Disease Stage
* Drug
* Clinical Conditions

🧭 **Page Navigator**
Allows users to move between the different dashboard pages.

🔄 **Reset Button**
Allows users to return the dashboard to its default filter state.

These features make the dashboard more interactive, user-friendly, and suitable for exploring the dataset from multiple perspectives.

---

# 🛠️ Tools & Technologies

| 🧰 Tool               | 🎯 Purpose                            |
| --------------------- | ------------------------------------- |
| 📗 Microsoft Excel    | Data cleaning & Pivot Table analysis  |
| 📊 Microsoft Power BI | Dashboard development & visualization |
| 📈 Power BI Visuals   | Interactive data analysis             |

---

# 🧠 Skills Demonstrated

🔹 Data Cleaning
🔹 Missing Value Treatment
🔹 Data Transformation
🔹 Data Standardization
🔹 Exploratory Data Analysis
🔹 Pivot Table Analysis
🔹 Healthcare Data Analytics
🔹 Data Visualization
🔹 Power BI Dashboard Development
🔹 Interactive Dashboard Design
🔹 Insight Generation
🔹 Recommendation Development

---

# 🏁 Project Outcome

The completed dashboard transforms the cleaned cirrhosis patient dataset into an **interactive healthcare analytics solution**.

📊 It enables users to explore:

**Demographics → Clinical Conditions → Laboratory Measurements → Treatment → Disease Stage → Patient Outcomes**

and converts these findings into **key insights and practical recommendations**.

---

## ⭐ Project Highlights

> 🩺 **Healthcare Analytics**
> 📊 **Interactive Power BI Dashboard**
> 🧪 **Laboratory Analysis**
> 🧬 **Disease Stage Analysis**
> 💊 **Treatment Comparison**
> 💡 **Data-Driven Insights**
> 🎯 **Recommendations**

---

### 🔖 Topics

`power-bi` `data-analysis` `data-visualization` `healthcare-analytics` `cirrhosis` `patient-data-analysis` `powerbi-dashboard` `excel` `business-intelligence` `dashboard`
