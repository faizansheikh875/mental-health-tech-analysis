#  Mental Health in Tech — Data Analysis Projec

##  Project Overview

This project analyzes the **Open Source Mental Illness (OSMI) Mental Health in Tech Survey** conducted between **2014 and 2016**. The goal was to uncover patterns in how mental health affects tech industry employees across different countries, age groups, genders, and workplace environments.

> **Tools Used:** Microsoft Excel (Data Cleaning) · Power BI (Analysis & Visualization)

---

##  Dataset

- **Source:** [Kaggle — OSMI Mental Health in Tech Survey](https://www.kaggle.com/datasets/osmi/mental-health-in-tech-survey)
- **Period:** 2014 – 2016
- **Respondents:** ~1,260 tech industry professionals
- **Countries:** 50+ countries worldwide

---

##  Data Cleaning (Excel)

The following cleaning steps were performed before analysis:

- Removed invalid entries in `no_employees` column (date values like "June 20")
- Replaced **"Don't know"** responses with `NaN` across multiple columns
- Standardized `Gender` column (normalized inconsistent entries)
- Fixed `Age` column outliers (removed negative values and unrealistic ages)
- Created a new **`age_category`** column in Power BI using DAX:

```DAX
age_category = 
IF('survey'[Age] < 20, "Fresher",
    IF('survey'[Age] <= 35, "Intermediate",
        "Senior"))
```

---

##  Key Findings & Insights

###  1. Country / Region Analysis
- **United States** ranked **#1** with the highest number of survey respondents, indicating the largest representation of tech workers reporting mental health challenges globally.

---

###  2. Gender Impact
- **Male employees** are the most affected group, representing **77%** of total survey respondents.
- This reflects the gender makeup of the tech industry, where males are the dominant workforce.

---

###  3. Age Group Analysis
| Age Category | Age Range | % Affected |
|---|---|---|
| Fresher | Under 20 | Low representation |
| **Intermediate** | **20 – 35** | **Most Affected ✅** |
| Senior | Above 35 | Moderate |

- The **Intermediate (20–35)** age group is the **most affected**, representing the core working-age population in tech companies.

---

###  4. Tech Industry Impact
- **73%** of respondents work in **tech companies**, confirming this dataset is highly representative of the tech workforce and their unique mental health pressures.

---

###  5. Work Mode Analysis
- **76% of office-mode workers** reported being affected by mental health challenges, compared to remote workers.
- This suggests that **in-office environments** may contribute to higher mental health stress.

---

###  6. Mental Health Consequences at Work
- **24%** of respondents reported experiencing **negative mental health consequences** at their workplace.
- This means 1 in 4 tech workers face real professional consequences related to mental health.

---

###  7. Anonymity Awareness
- **66%** of respondents said they **"Don't Know"** whether their anonymity is protected when seeking mental health help.
- This reflects a significant **lack of communication** from employers about privacy policies.

---

###  8. Supervisors vs Coworkers
| Role | % Affected |
|---|---|
| **Supervisors** | **37%** |
| Coworkers | 15% |

- **Supervisors are more than twice as affected** as coworkers, likely due to higher responsibility, pressure, and accountability in their roles.
- This is a critical finding for companies designing mental health support programs — **leadership needs support too.**

---

##  Summary of Insights

| # | Insight | Key Stat |
|---|---|---|
| 1 | Top country represented | 🇺🇸 United States |
| 2 | Most affected gender | 👨 Male — 77% |
| 3 | Most affected age group | 🎯 Intermediate (20–35 yrs) |
| 4 | Tech company representation | 💻 73% |
| 5 | Office workers affected | 🏢 76% |
| 6 | Face workplace consequences | ⚠️ 24% |
| 7 | Unaware of anonymity protection | 🔒 66% |
| 8 | Supervisors vs Coworkers affected | 👔 37% vs 15% |

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Microsoft Excel** | Data Cleaning & Preprocessing |
| **Power BI** | Data Analysis, DAX Columns & Visualization |
| **Kaggle** | Dataset Source |




---

##  What I Learned

- How to clean **real-world survey data** with inconsistencies
- How to work with **categorical data** (different from numerical sales data)
- How to build **DAX calculated columns** in Power BI
- How to structure **HR Analytics insights** for business decisions
- The importance of **mental health support** in workplace environments


---

*Dataset Source: OSMI (Open Sourcing Mental Illness) — osmihelp.org*

