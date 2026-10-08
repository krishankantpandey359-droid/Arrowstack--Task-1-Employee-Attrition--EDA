# Arrowstack Data Science Internship - Task 1

## Comprehensive Exploratory Data Analysis (EDA) on Employee Attrition

**Project:** Employee Attrition Analysis  
**Internship:** Arrowstack Data Science Internship  
**Task:** Task 1 - Comprehensive Exploratory Data Analysis (EDA)  
**Dataset:** IBM HR Analytics Employee Attrition & Performance  
**Source:** Kaggle  
**Prepared by:** Srishti Pandey  
**Level:** Intermediate Data Science

---

## Project Overview

This project presents a comprehensive Exploratory Data Analysis (EDA) of the IBM HR Analytics Employee Attrition & Performance dataset.

The main objective is to understand employee attrition patterns and identify employee, job and workplace groups that show higher observed attrition rates.

The analysis follows a complete data science workflow:

**Business Problem → Dataset Understanding → Data Quality → Cleaning → EDA → Business Questions → Statistical Validation → Findings → Recommendations → Final Validation**

The analysis is descriptive. It identifies patterns and relationships in the dataset but does not claim that any factor directly causes employee attrition.

---

## Business Problem

Employee attrition can increase hiring and training requirements and may affect workforce stability and productivity.

The analysis focuses on understanding:

- Which employee groups show higher observed attrition?
- Which departments and job roles have higher attrition rates?
- Is overtime associated with higher attrition?
- How does job satisfaction differ across attrition groups?
- How does income differ between employees who stayed and those who left?
- Does distance from home show different attrition patterns?
- Does tenure relate to attrition?
- Does business travel show different attrition rates?

### Stakeholder

The main stakeholders considered for this analysis are:

- HR Management
- Workforce Planning Teams

### Main KPI

The primary descriptive KPI is the **overall observed employee attrition rate**.

The overall rate is used as the baseline for comparing employee groups.

---

## Dataset

The project uses the IBM HR Analytics Employee Attrition & Performance dataset available through Kaggle.

**Kaggle Dataset Identifier:**

`pavansubhasht/ibm-hr-analytics-attrition-dataset`

**Expected source file:**

`WA_Fn-UseC_-HR-Employee-Attrition.csv`

**Dataset size:**

- 1,470 employee records
- 35 source columns

The notebook downloads the dataset automatically, so the CSV does not need to be manually uploaded before running the project.

---

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Google Colab
- Jupyter Notebook
- Kaggle dataset

---

## Data Quality and Cleaning

The project includes several data quality checks before analysis.

### Checks performed

- Dataset shape
- Data types
- Missing values
- Duplicate rows
- Employee ID uniqueness
- Constant columns
- Categorical value checks
- Numeric range checks
- Logical workforce consistency checks
- Outlier review

The original dataframe is kept unchanged and a separate analytical copy is used for cleaning.

Constant columns that do not provide analytical information are removed from the analytical copy.

Unusual values are reviewed rather than being removed automatically.

---

## Exploratory Data Analysis

The analysis includes:

### Attrition Overview

Overall employee attrition is calculated and used as the baseline for group comparisons.

### Department Analysis

Attrition rates are compared across departments.

### Job Role Analysis

Different job roles are compared using both employee counts and within-group attrition rates.

### Overtime Analysis

Attrition is compared between employees working overtime and those who do not.

### Job Satisfaction Analysis

Job satisfaction levels are examined in relation to attrition.

### Income Analysis

Income distributions are compared between employees who stayed and employees who left.

### Distance from Home

Distance bands are used to examine differences in observed attrition.

### Tenure Analysis

Employee tenure bands are used to identify differences in attrition patterns.

### Business Travel

Attrition is compared across different business travel categories.

Additional analysis includes age, work-life balance, distributions, correlations and attrition-linked grouped analysis.

---

## Statistical Validation

Statistical tests are used as additional evidence rather than as proof of causation.

### Categorical Variables

The project uses:

- Chi-square tests
- Expected-count diagnostics
- Cramer's V effect size
- Benjamini-Hochberg False Discovery Rate (FDR) correction

### Numeric Variables

The project uses:

- Mann-Whitney U tests
- Rank-biserial effect size
- Benjamini-Hochberg FDR correction

### Confidence Intervals

Wilson 95% confidence intervals are calculated for important observed attrition rates to show uncertainty around the estimated group rates.

---

## Small-Group Safeguard

A high percentage alone can be misleading when a group contains very few employees.

Therefore, group sizes are checked before interpreting high attrition rates.

Groups with fewer than 30 records are flagged for careful interpretation.

This does not remove those groups from the dataset. It only prevents very small groups from being treated as equally strong evidence.

---

## Investigation Priority Rule

A group is treated as a higher investigation priority only when:

1. It is not flagged as a small group under the 30-record check, and
2. Its observed attrition rate is at least **5 percentage points above the overall observed attrition rate**.

This is a transparent project-level prioritization rule.

It is **not a universal HR policy or threshold**.

---

## Sensitivity Analysis

The investigation-priority threshold is also tested using different values:

- 3 percentage points
- 5 percentage points
- 7 percentage points

This helps show how the number of priority groups changes when the threshold becomes more or less strict.

---

## Key Observed Findings

The analysis found several groups with higher observed attrition rates than the overall baseline.

Examples include:

| Group | Observed Attrition |
|---|---:|
| Overall | 16.12% |
| Sales Department | 20.63% |
| Sales Representative | 39.76% |
| OverTime = Yes | 30.53% |
| Travel_Frequently | 24.91% |
| Distance 21+ | 22.06% |
| Tenure 0-1 years | 34.88% |

These figures describe patterns in the dataset. They should not be interpreted as proof that these factors independently cause employees to leave.

---

## Key Recommendations

Based on the observed patterns, the analysis recommends:

- Review overtime and workload patterns before deciding on retention actions.
- Investigate high-attrition job roles in more detail.
- Pay attention to early-tenure employee experience.
- Review travel and commute patterns together with other workplace conditions.
- Validate the findings using current organizational HR data.
- Combine quantitative analysis with employee feedback.
- Treat the results as investigation priorities rather than individual employee risk labels.

---

## Analytical Decisions and Trade-offs

Several analytical choices were documented during the project.

Examples include:

- Keeping the raw dataframe unchanged.
- Removing only constant columns from the analytical copy.
- Not using employee ID as an analytical feature.
- Reviewing outliers without automatically deleting them.
- Using both counts and within-group attrition rates.
- Using non-parametric testing for numeric group comparisons.
- Applying FDR correction because multiple statistical tests are performed.
- Reporting effect sizes alongside statistical significance.
- Using confidence intervals to communicate uncertainty.
- Checking group size before prioritizing high attrition rates.

Alternative approaches were considered where appropriate, and the selected methods were kept aligned with the scope of an EDA task.

---

## Responsible Use and Limitations

This analysis is based on a historical dataset and is intended for exploratory analysis.

Important limitations include:

- The dataset may not represent a current organization's workforce.
- Observed relationships do not establish causation.
- Statistical significance does not automatically mean practical importance.
- Small groups require careful interpretation.
- HR decisions should not be made from these results alone.
- Current organizational data and employee feedback should be used for real-world decisions.

The results should therefore be used to identify areas for further investigation rather than to make individual employee risk predictions.

---

## Final Validation

The notebook includes an automated final validation section.

The validation checks cover:

- Dataset shape
- Required fields
- Missing values
- Duplicate records
- Employee ID uniqueness
- Logical workforce consistency
- Statistical analysis completion
- FDR correction
- Effect-size calculations
- Multivariate analysis
- Priority evidence
- Chi-square assumptions
- Confidence intervals
- Final evidence tables

Before submission, the final notebook should display:

**PASS: All final validation checks passed.**

---

## How to Run in Google Colab

1. Open the notebook in Google Colab.
2. Start with a **fresh runtime**.
3. Select **Runtime → Run all**.
4. Wait for the Kaggle dataset download and all cells to finish.
5. Go to the final validation section.
6. Confirm:

`PASS: All final validation checks passed.`

7. Save the executed notebook with the important tables, charts and validation outputs visible.

The notebook downloads the dataset automatically, so manual CSV upload is not required.

---

## Repository Structure

```text
Arrowstack-Task-1-Employee-Attrition-EDA/
│
├── Arrowstack_Task_1_Comprehensive_EDA_Srishti_Pandey_FINAL_100_MARK_MASTER.ipynb
├── README.md
└── Arrowstack_Task_1_Employee_Attrition_EDA_Presentation_Srishti_Pandey.pptx# Arrowstack--Task-1-Employee-Attrition--EDA
Comprehensive Exploratory Data Analysis of IBM HR Employee Attrition dataset for Arrowstack Data Science Internship Task 1.
