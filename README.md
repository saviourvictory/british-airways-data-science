
# British Airways Data Science Projects

A collection of two data science projects completed as part of the British Airways Data Science job simulation on Forage.

These projects demonstrate practical applications of Python, data analysis, exploratory data analysis, data processing, predictive modelling and machine learning evaluation in an airline business context.

## Projects Overview

### Task 1: Flight Schedule and Lounge Eligibility Analysis

**Objective:** Analyse British Airways summer flight schedule data and develop a structured lookup of flight capacity and tier-based lounge eligibility.

**Dataset:** 10,000 flight records with 17 original columns.

**Work performed:**
- Loaded and inspected flight schedule data using Pandas.
- Calculated total seat capacity across First Class, Business Class and Economy.
- Grouped flights by time of day and haul type (short-haul and long-haul).
- Aggregated flight counts, total seats and eligible passenger counts across three tiers.
- Calculated tier eligibility percentages relative to total seat capacity.
- Exported the aggregated results into an Excel lookup file.

**Output:** `BA_Lounge_Eligibility_Lookup.xlsx`

**Technologies:** Python, Pandas, NumPy, Excel.

### Task 2: Customer Booking Completion Prediction

**Objective:** Explore customer booking behaviour and develop a machine learning classification model to predict whether a customer completes an airline booking.

**Dataset:** 50,000 customer booking records containing 13 input features and one target variable.

**Exploratory Data Analysis:**
- Analysed booking completion rates across sales channels.
- Investigated differences between round trips, one-way trips and circle trips.
- Examined booking completion patterns by flight day.
- Compared booking origins and flight routes.
- Investigated numerical features including purchase lead time, length of stay and flight duration.
- Identified class imbalance in the target variable.

**Data Preparation:**
- Checked missing values and duplicate records.
- Separated numerical, binary and categorical features.
- Applied One-Hot Encoding to categorical variables.
- Used a stratified 80/20 train-test split.
- Maintained consistent target proportions across training and testing datasets.

**Machine Learning:**

Developed a Random Forest classification pipeline using Scikit-learn.

Two approaches were evaluated:

1. Standard Random Forest.
2. Class-weighted Random Forest using `balanced_subsample` to address class imbalance.

**Model Evaluation:**

The balanced Random Forest achieved the following five-fold cross-validation results:

| Metric | Mean Score |
|---|---:|
| Accuracy | 80.20% |
| Precision | 36.97% |
| Recall | 45.84% |
| F1-score | 40.92% |
| ROC-AUC | 77.94% |

Class balancing improved the model's ability to identify completed bookings. Recall increased from approximately 4% to 46%, although precision decreased.

**Feature Importance:**

Permutation importance identified the most influential features:

1. Booking origin
2. Flight route
3. Length of stay
4. Sales channel
5. Flight duration

**Technologies:** Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn.

## Skills Demonstrated

- Data Cleaning and Preprocessing
- Exploratory Data Analysis (EDA)
- Data Aggregation and Statistical Analysis
- Feature Engineering
- Data Visualisation
- Classification
- Random Forest
- One-Hot Encoding
- Imbalanced Classification
- Model Evaluation
- Stratified Cross-Validation
- Permutation Feature Importance
- Python and SQL-oriented analytical thinking

## Repository Structure

```text
british-airways-data-science/
│
├── task1.ipynb
├── task2.ipynb
└── README.md
```

## Getting Started

Clone the repository:

```bash
git clone https://github.com/saviourvictory/british-airways-data-science.git

cd british-airways-data-science
```

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl jupyter
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open `task1.ipynb` or `task2.ipynb` to explore the analysis and modelling workflow.

**Note:** The original datasets are not included in this repository. You will need the relevant input files to execute the notebooks from the beginning.

## Author

**Saviour Victory**

MSc Artificial Intelligence and Machine Learning  
University of Essex

GitHub: https://github.com/saviourvictory

---

*This repository demonstrates practical data science and machine learning workflows applied to airline operations and customer booking behaviour.*