# Exploratory Data Analysis on Haberman's Cancer Survival Dataset

## About the Dataset
The dataset contains cases from a study conducted between 1958 and 1970 at the University of Chicago's Billings Hospital on the survival of patients who had undergone surgery for breast cancer. 

**Dataset Link**: [Haberman's Survival Data Set on Kaggle](https://www.kaggle.com/datasets/gilsousa/habermans-survival-data-set)

**File Details**:
- Data: `haberman.csv`
- Code: `HabermanDatasetEDA.ipynb`

### Dataset Information
- **Number of Attributes**: 4
- **Attribute Details**:
  1. **Age**: Age of the patient at the time of operation (numerical).
  2. **Year**: Patient's year of operation (year - 1900, numerical).
  3. **Nodes**: Number of positive axillary nodes detected (numerical).
  4. **Survival Status** (class attribute):
     - `1`: The patient survived 5 years or longer.
     - `2`: The patient died within 5 years.

---

## 1. Objective
The primary goal of this analysis is to perform Exploratory Data Analysis (EDA) on the given dataset for a **classification problem**, which aims to:
- Predict whether patients who underwent cancer surgery survived for 5 years or longer.
- Understand relationships between features and their importance.

---

## 2. High-Level Statistics
- **Number of Points**: 306
- **Number of Features**: 3 (excluding the target variable)
- **Number of Classes**: 2 (`1` and `2`)
- **Data Points per Class**:
  - `Class 1 (Survived)`: 225 (74%)
  - `Class 2 (Died)`: 81 (26%)

---

## 3. Univariate Analysis
### Statistical Insights:
- **Mean, Variance, and Standard Deviation** for each feature.
- **Median, Percentiles, Quantiles, Interquartile Range (IQR)**, and **Median Absolute Deviation (MAD)**.

### Visualization Techniques:
- **Probability Density Function (PDF)** and **Cumulative Density Function (CDF)**.
- **Boxplots** and **Violin Plots**.

**Key Findings**:
1. **Age**:
   - Patients under 36 survived; patients above 76 died.
   - Increasing age is associated with a higher probability of death.
2. **Year**:
   - Patients operated on before 1958 did not survive.
   - Over time, the probability of survival has reduced.
3. **Nodes**:
   - Patients with 0–3 positive nodes mostly survived.
   - 90% of patients who died had fewer than 20 positive nodes.
   - Patients with more than 3 positive nodes had a higher likelihood of death.

---

## 4. Bivariate Analysis
### Techniques:
- **2D Scatter Plots**.
- **Pair Plots**.
- **Correlation Matrix**.

**Key Findings**:
- Patients with age < 33 and nodes in the range [0, 5] survived.
- The **nodes feature** is the most critical predictor of survival.
- No significant correlation exists between the features.
- Higher nodes (>45) and higher age (>75) drastically reduce survival chances.
- None of the visualizations distinctly separate the classes (died vs. survived).

---

## 5. Conclusions
- The dataset is **imbalanced**, with 74% belonging to `status = 1` (survived) and 26% to `status = 2` (died).
- **Nodes** is the most important feature:
  - Patients with fewer positive axillary nodes are more likely to survive.
- **Age** and **Year** show weaker relationships with survival.
- Despite analysis, the dataset does not allow for a clear distinction between the two classes based on visualizations.

---

## Repository Contents
- **Data File**: `haberman.csv`
- **Notebook**: `HabermanDatasetEDA.ipynb`


