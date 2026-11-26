# Employee Attrition Analysis

## Comprehensive Exploratory Data Analysis (EDA)

**Project:** Employee Attrition Analysis  
**Dataset:** IBM HR Analytics Employee Attrition & Performance  
**Source:** Kaggle  
**Prepared by:** Srishti Pandey  
**Level:** Intermediate Data Science

## Project objective

This notebook studies employee attrition using the IBM HR Analytics dataset. It checks data quality, documents cleaning decisions, and uses tables, charts, and statistical checks to examine observed patterns.

The analysis is descriptive. A higher observed attrition rate is treated as a signal for further investigation, not as proof that a factor causes employees to leave.

## Files in this repository

- `Arrowstack_Task_1_Comprehensive_EDA_Srishti_Pandey_FINAL_100_MARK_MASTER_(2).ipynb`: main EDA notebook.
- `Task_1_Employee_Attrition_EDA_Presentation_ By_Srishti_Pandey.pptx`: project presentation.

The filenames above match the files currently stored in this repository. The supplied Kaggle dataset is downloaded at runtime; the original dataset is not modified or replaced by synthetic records.

## Main analysis coverage

- Loads the Kaggle dataset and checks the expected source file and shape.
- Builds a data dictionary for all loaded source columns.
- Checks missing values, duplicate rows, employee identifiers, constant columns, numeric ranges, and logical workforce relationships.
- Preserves the raw dataframe and records cleaning decisions.
- Reviews IQR outliers without deleting them automatically.
- Calculates overall attrition counts and rates.
- Answers eight business questions and adds employee-profile analysis.
- Compares group counts and within-group attrition rates, with a small-group safeguard.
- Reviews Pearson correlations and multivariate patterns.
- Runs Chi-square and Mann-Whitney U tests, reports effect sizes, and applies Benjamini-Hochberg false discovery rate adjustment within test families and across the combined comparison set.
- Checks Chi-square expected counts and flags tests where the asymptotic p-value assumptions are not adequately supported; calculates Wilson 95% intervals for selected observed rates.
- Summarizes findings, investigation priorities, business recommendations, responsible-use considerations, and limitations.
- Includes automated validation, reproducibility notes, rubric coverage, and a viva/demo explanation.

## How to run in Google Colab

1. Upload or open the notebook file listed above in Google Colab.
2. Use a fresh runtime.
3. Select **Runtime → Run all**.
4. Wait for the Kaggle dataset download and all cells to finish.
5. Review the final validation section.
6. Confirm the notebook prints:

   `PASS: All final validation checks passed.`

The notebook downloads the CSV automatically using KaggleHub. The CSV does not need to be uploaded manually before the first run. Internet access is required for the package installation and dataset download.

## Dataset and reproducibility

**Kaggle dataset identifier:** `pavansubhasht/ibm-hr-analytics-attrition-dataset`  
**Expected source file:** `WA_Fn-UseC_-HR-Employee-Attrition.csv`  
**Expected source shape:** 1,470 rows × 35 columns

The notebook checks the loaded shape against this expected shape in its final validation section.

## Statistical interpretation

P-values are used as exploratory evidence. Multiple-test p-values are adjusted with the Benjamini-Hochberg false discovery rate procedure. Effect sizes are reported alongside p-values. Chi-square expected-count diagnostics are checked, and Wilson intervals show uncertainty around selected observed group rates.

These checks do not establish causality. Group size, observed rate differences, effect sizes, and business context are considered together before identifying an investigation priority.

## Business priority rule

A group is marked **Higher priority** only when:

- it is not flagged as a small group under the 30-record check, and
- its observed attrition rate is at least 5 percentage points above the overall observed attrition rate.

This is a transparent project-specific rule for prioritizing further investigation. It is not a universal HR threshold.

## Limitations

- The analysis is based on the supplied IBM HR Analytics dataset and its available fields.
- Observed associations do not establish cause and effect.
- Priority labels are exploratory and should not be used alone for employee-level decisions.
- The notebook requires internet access to install dependencies and download the Kaggle dataset. Install the pinned project dependency ranges with `python -m pip install -r requirements.txt` before running locally. GitHub Actions validates the notebook format and executes all cells on pushes and pull requests.

## Latest GitHub Actions validation

Latest verified successful main-branch workflow run checked on 26 November 2026: [GitHub Actions run #45798096231](https://github.com/krishankantpandey359-droid/Arrowstack--Task-1-Employee-Attrition--EDA/actions/runs/45798096231). This run verifies the checks configured in this repository's workflow; it does not replace manual testing of features outside CI.
