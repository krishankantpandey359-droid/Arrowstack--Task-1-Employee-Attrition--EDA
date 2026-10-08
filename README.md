# Arrowstack Data Science Internship — Task 1

## Comprehensive Exploratory Data Analysis (EDA)

**Project:** Employee Attrition Analysis  
**Dataset:** IBM HR Analytics Employee Attrition & Performance  
**Source:** Kaggle  
**Prepared by:** Srishti Pandey  
**Level:** Intermediate Data Science

## Project objective

This notebook studies employee attrition using the IBM HR Analytics dataset. I first check the data quality, then clean the data where required and use tables, charts and statistical checks to study the main patterns.

The analysis is descriptive. A higher observed attrition rate is treated as a place to investigate next, not as proof that a factor causes employees to leave.

## Main coverage

- Exact Kaggle dataset loading with expected file and shape checks
- Complete data dictionary for all loaded source columns
- Missing-value, duplicate and employee-identifier checks
- Constant-column and basic numeric range checks
- Logical workforce consistency checks
- Traceable cleaning decisions with raw data preserved
- IQR outlier review without blind deletion
- Overall attrition count and percentage
- Eight business questions plus additional employee-profile analysis
- Group-wise attrition counts and within-group rates
- Small-group safeguard
- Direct attrition-linked multivariate analysis
- Pearson correlation review
- Chi-square tests with expected-count diagnostics, Cramer's V and FDR adjustment
- Mann-Whitney U tests with rank-biserial effect size and FDR adjustment
- Wilson 95% intervals for key observed rates
- Evidence summary and transparent investigation-priority rule
- Business KPI definition and executive decision summary
- Responsible-use and privacy note
- Findings, recommendations, non-causal interpretation and limitations
- Final automated validation and reproducibility check
- Rubric coverage map and viva/demo explanation
- Final submission checklist

## How to run in Google Colab

1. Open `Arrowstack_Task_1_Comprehensive_EDA_Srishti_Pandey_FINAL_100_MARK_MASTER.ipynb` in Google Colab.
2. Use a **fresh runtime**.
3. Select **Runtime -> Run all**.
4. Wait for the Kaggle dataset and all cells to finish.
5. Go to the final validation section.
6. Confirm the exact message:

**PASS: All final validation checks passed.**

7. Save the executed notebook with important outputs visible.

The notebook downloads the CSV automatically, so the CSV does not need to be uploaded manually before the first run.

## Dataset and reproducibility

Kaggle dataset identifier:
`pavansubhasht/ibm-hr-analytics-attrition-dataset`

Expected source file:
`WA_Fn-UseC_-HR-Employee-Attrition.csv`

Expected source shape:
`1470 rows × 35 columns`

## Statistical interpretation

P-values are used only as exploratory evidence. Multiple-test p-values are adjusted with the Benjamini-Hochberg false discovery rate procedure. Effect sizes are reported alongside p-values. Chi-square expected-count diagnostics are also checked. Wilson intervals are included to show uncertainty around observed group rates.

These checks do not prove causality. The notebook uses group size, rate difference, effect size and business context together before calling a group a higher investigation priority.

## Business priority rule

A group is marked **Higher priority** only when:

- it is not flagged as a small group under the 30-record check, and
- its observed attrition rate is at least 5 percentage points above the overall observed attrition rate.

This is a transparent project rule for prioritizing further investigation. It is not a universal HR threshold.

## GitHub package

Recommended folder:

```text
OIBSIP/Arrowstack-DataScience-Task1-EmployeeAttritionEDA/
├── Arrowstack_Task_1_Comprehensive_EDA_Srishti_Pandey_FINAL_100_MARK_MASTER.ipynb
├── README_Arrowstack_Task_1_Srishti_Pandey_FINAL_100_MARK_MASTER.md
└── Arrowstack_Task_1_Employee_Attrition_EDA_Presentation_Srishti_Pandey.pptx
