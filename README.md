# Healthcare Analytics for Doctor Visits

A Python-based exploratory data analysis project that explores patterns and associations related to doctor visits using healthcare-related data.

**VOIS × AICTE TIRTC DIY Project**  
**Mehak Abid · B.Tech. CSE · Jamia Hamdard**

---

## 📌 Project Overview

Healthcare datasets contain information about demographics, health conditions, financial background, chronic conditions, healthcare support, and doctor visits.

This project uses **Python-based Exploratory Data Analysis (EDA)** to identify useful patterns and relationships associated with the number of doctor visits.

> **Interpretation note:** The findings describe associations observed in the dataset. They do not establish causation.

---

## 🎯 Problem Statement

The objective of this project is to analyze healthcare-related data and identify patterns associated with doctor visits.

The analysis focuses on:

- Gender
- Age
- Income
- Illness
- Health condition
- Reduced activity
- Chronic conditions
- Healthcare support
- Number of doctor visits

### Key Question

**Which demographic and health-related factors are associated with doctor visits?**

---

## 📊 Dataset

The dataset contains **5,190 records** and **13 original columns**.

| Dataset Detail | Value |
|---|---:|
| Total records | 5,190 |
| Original columns | 13 |
| Missing values | 0 |
| Unique record IDs | 5,190 |
| Doctor visit range | 0–9 |
| Gender categories | Female, Male |

The `Unnamed: 0` column is treated as a **record identifier** and is excluded from analytical calculations.

The `age` variable is stored using decimal values. Therefore, the original numerical age values are used without creating artificial conventional age groups.

---

## 🔄 Project Workflow

```text
Load Data
    ↓
Data Quality Check
    ↓
Preprocessing
    ↓
Univariate Analysis
    ↓
Bivariate Analysis
    ↓
Multivariate Analysis
    ↓
Correlation Analysis
    ↓
Interpretation
```

---

## 🧹 Data Quality & Preprocessing

The project performs:

- Dataset inspection
- Data type checking
- Missing-value checking
- Record-ID uniqueness checking
- Duplicate analysis
- Removal of the record identifier from analytical calculations

No observations were removed during duplicate handling because identical analytical rows can correspond to different original record IDs.

---

# 📈 Exploratory Data Analysis

## 1. Doctor Visits Distribution

The dataset contains mostly records with zero doctor visits, followed by records with one or more visits.

<img width="792" height="479" alt="image" src="https://github.com/user-attachments/assets/920f1d2d-e2df-4ef1-9fb1-9cc25a78edc6" />

---

## 2. Age Distribution

The dataset contains 12 distinct decimal age values. The original values are retained for analysis.

<img width="870" height="498" alt="image" src="https://github.com/user-attachments/assets/613f9cc5-01a5-404a-9f71-f880a357fd89" />

---

## 3. Average Doctor Visits by Gender

- Female average visits: **0.362**
- Male average visits: **0.236**

<img width="633" height="479" alt="image" src="https://github.com/user-attachments/assets/cd394b9a-1dca-40d6-ab6c-9e9a41ae5e97" />

---

## 4. Illness Score vs Average Doctor Visits

Average doctor visits generally increase as the illness score increases.

- Illness score 0 → **0.079** average visits
- Illness score 5 → **0.814** average visits

<img width="778" height="479" alt="image" src="https://github.com/user-attachments/assets/b215affe-8eac-4643-bd31-fcbb2f2d0824" />

---

## 5. Health Condition vs Average Doctor Visits

The analysis compares the health-condition indicator with average doctor visits across the observed values.

<img width="856" height="479" alt="image" src="https://github.com/user-attachments/assets/585eefb9-181e-46e5-9c71-f8c70d05c2a3" />

---

## 6. Reduced Activity vs Average Doctor Visits

Reduced activity has the strongest positive correlation with doctor visits among the numerical variables analyzed.

**Correlation with visits: 0.419**

<img width="841" height="479" alt="image" src="https://github.com/user-attachments/assets/73ab0329-6983-484d-9abc-dd36e36df890" />

---

## 7. Long-Term Chronic Condition vs Average Doctor Visits

- Chronic condition = Yes → **0.603** average visits
- Chronic condition = No → **0.262** average visits

<img width="701" height="479" alt="image" src="https://github.com/user-attachments/assets/25dc05f0-bf87-437a-a913-0906e4320212" />

---

## 8. Correlation Analysis

| Variable | Correlation with Doctor Visits |
|---|---:|
| Reduced activity | **0.419** |
| Illness | **0.224** |
| Health | **0.193** |
| Age | **0.125** |
| Income | **-0.077** |

<img width="718" height="609" alt="image" src="https://github.com/user-attachments/assets/fba14090-b0e0-4e92-ac12-a101942093af" />

---

# 🔎 Key Findings

- The dataset contains **5,190 records** with no missing values and **5,190 unique record IDs**.
- The average number of doctor visits is **0.302**, while the median is **0**.
- The maximum recorded number of doctor visits is **9**.
- Female participants have a higher average number of doctor visits (**0.362**) than male participants (**0.236**).
- Average doctor visits generally increase with illness score.
- Participants with a long-term chronic condition have a higher average number of doctor visits (**0.603**) than those without one (**0.262**).
- Reduced activity shows the strongest positive correlation with doctor visits among the numerical variables analyzed (**0.419**).
- Illness and health also show positive correlations with doctor visits.
- Age shows a weaker positive correlation, while income shows a weak negative correlation.

---

# 🛠️ Technologies Used

### Programming & Environment
- Python
- Google Colab

### Data Analysis
- Pandas
- NumPy

### Data Visualization
- Matplotlib
- Seaborn

### Analysis Techniques
- Univariate Analysis
- Bivariate Analysis
- Multivariate Analysis
- Grouped Statistics
- Correlation Analysis

---

# 📁 Repository Structure

```text
healthcare-analytics-doctor-visits/
│
├── README.md
├── Healthcare_Analytics_for_Doctor_Visits.ipynb
│
├── data/
│   └── healthcare_doctor_visits.csv
│
├── images/
│   ├── doctor-visits-distribution.png
│   ├── age-distribution.png
│   ├── average-visits-by-gender.png
│   ├── illness-vs-average-visits.png
│   ├── health-vs-average-visits.png
│   ├── reduced-activity-vs-average-visits.png
│   ├── chronic-condition-vs-average-visits.png
│   └── correlation-heatmap.png
│
└── presentation/
    └── Healthcare_Analytics_for_Doctor_Visits.pptx
```

---

# 👥 End Users

### Healthcare Analysts
Explore patterns in healthcare-related datasets.

### Students & Educators
Learn practical data analysis, statistics, and visualization.

### Healthcare Researchers
Explore variables associated with doctor visits.

### Data-Driven Decision Makers
Review summarized patterns for further analysis.

The project is an exploratory analytics project and does not provide clinical diagnosis or medical recommendations.

---

# 📄 Project Files

| File | Description |
|---|---|
| `Healthcare_Analytics_for_Doctor_Visits.ipynb` | Complete Python/Colab analysis notebook |
| `data/healthcare_doctor_visits.csv` | Healthcare doctor-visit dataset |
| `presentation/Healthcare_Analytics_for_Doctor_Visits.pptx` | Project presentation |
| `images/` | Graphs used in the project documentation |

---

# 🎓 Project Outcome

The project demonstrates how Python-based data analytics and visualization can be used to explore healthcare-related datasets and identify patterns associated with doctor visits.

The analysis combines **data cleaning, exploratory analysis, grouped statistics, visualization, and correlation analysis** to turn raw records into interpretable insights.

---

# ⚠️ Disclaimer

This project is intended for **academic and educational purposes**.

The analysis describes patterns and statistical associations present in the dataset. It should not be interpreted as medical advice, clinical diagnosis, or evidence of causal relationships.

---

# ✅ Conclusion

This project analyzed **5,190 healthcare-related records** to identify patterns associated with doctor visits.

The analysis found noticeable relationships between doctor visits and several health-related variables. Reduced activity showed the strongest positive correlation among the numerical variables analyzed. Illness score and long-term chronic-condition status also showed differences in average doctor visits.

Overall, the project demonstrates the use of exploratory data analysis and visualization to understand patterns in healthcare-related data.

---

## 👤 Author

**Mehak Abid**  
B.Tech. CSE · Jamia Hamdard

**VOIS × AICTE TIRTC DIY Project**
