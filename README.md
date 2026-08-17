# MLOps & Feast – CSE Skill Gap Analysis

**Project Overview**

This project focuses on analyzing the alignment between **Computer Science Engineering (CSE) graduate skills, academic curriculum, industry requirements, decision frameworks, and training outcomes**.

The project uses Python, Pandas, NumPy, and Excel datasets to perform initial **data exploration and data-quality analysis** as part of an MLOps/skill-gap analysis workflow.

The analysis works with four datasets:

* **Graduate Skills**
* **Curriculum Industry**
* **Decision Framework**
* **Training Outcomes**

The datasets are stored as separate sheets in an Excel workbook named:

`CSE_Curriculum_Industry_Skill_Alignment_4_Datasets_500_Each.xlsx`

---

## Objectives

The main objectives of this project are:

1. Analyze graduate skill information.
2. Examine the relationship between academic curriculum and industry requirements.
3. Explore decision-making framework data.
4. Analyze training outcomes.
5. Identify missing values in the datasets.
6. Identify duplicate records.
7. Inspect dataset structure, columns, and statistical information.
8. Prepare the datasets for further skill-gap analysis and MLOps workflows.

---

## Technologies Used

* **Python**
* **Google Colab**
* **Pandas**
* **NumPy**
* **Microsoft Excel / XLSX**
* **Google Drive**

---

## Project Structure

```text
MLOps-Feast-SkillGap/
│
├── MLops_Feast_SkillGap.py
├── CSE_Curriculum_Industry_Skill_Alignment_4_Datasets_500_Each.xlsx
└── README.md
```

---

## 📊 Datasets

The Excel workbook contains four sheets:

### 1. Graduate_Skills

Contains information related to the skills possessed or expected among CSE graduates.

### 2. Curriculum_Industry

Contains data related to the relationship between academic curriculum and industry skill requirements.

### 3. Decision_Framework

Contains information related to the decision framework used in the skill-alignment analysis.

### 4. Training_Outcomes

Contains information related to training and resulting outcomes.

The Python script loads each sheet independently using Pandas.

---

## Data Analysis Performed

### Dataset Shape

The script checks the number of rows and columns in each dataset:

```python
print("Graduate Skills:", graduate_skills.shape)
print("Curriculum Industry:", curriculum_industry.shape)
print("Decision Framework:", decision_framework.shape)
print("Training Outcomes:", training_outcomes.shape)
```

### Column Analysis

The columns of every dataset are displayed to understand the available attributes.

### Data Inspection

The project uses:

* `head()`
* `info()`
* `describe()`

to inspect the datasets and understand their structure and statistical properties.

### Missing Value Analysis

Missing values are checked for all four datasets:

```python
graduate_skills.isnull().sum()
curriculum_industry.isnull().sum()
decision_framework.isnull().sum()
training_outcomes.isnull().sum()
```

This helps identify incomplete records that may require preprocessing.

### Duplicate Detection

The project also checks for duplicate records in each dataset:

```python
graduate_skills.duplicated().sum()
curriculum_industry.duplicated().sum()
decision_framework.duplicated().sum()
training_outcomes.duplicated().sum()
```

This helps improve data quality before further analysis or machine-learning workflows.

---

##  How to Run the Project

### Option 1: Google Colab

1. Open the Python notebook/script in Google Colab.
2. Upload the Excel dataset.
3. Run the cells sequentially.
4. The script loads the four Excel sheets.
5. Dataset information, missing values, and duplicate counts are displayed.

The original notebook was created using Google Colab.

### Option 2: Local Python Environment

Install the required libraries:

```bash
pip install pandas numpy openpyxl
```

Place the Excel dataset in the same project directory as the Python script.

Then run:

```bash
python MLops_Feast_SkillGap.py
```

---

## Workflow

```text
Excel Dataset
      ↓
Load Excel Workbook
      ↓
Read Four Dataset Sheets
      ↓
Inspect Dataset Shape
      ↓
Inspect Columns
      ↓
Explore Dataset Information
      ↓
Statistical Analysis
      ↓
Missing Value Detection
      ↓
Duplicate Detection
      ↓
Data Quality Assessment
      ↓
Further Skill-Gap / MLOps Analysis
```

---

## Current Status

### Completed

* Excel workbook loading
* Loading four datasets
* Dataset shape inspection
* Column inspection
* Basic dataset exploration
* Statistical description
* Missing-value detection
* Duplicate detection
* Google Drive integration

### Future Enhancements

The project can be extended with:

* Data preprocessing
* Feature engineering
* Skill-gap identification
* Curriculum vs. industry comparison
* Visualization using Matplotlib/Seaborn
* Machine-learning-based skill prediction
* Feature Store integration using **Feast**
* Model training and evaluation
* Model versioning
* MLOps pipeline automation
* Model deployment
* Monitoring and performance tracking

> **Note:** These are potential future extensions; the current uploaded script does not yet implement the ML model, Feast feature store, or deployment pipeline.

---

Input File

The project expects the following Excel file:

```text
CSE_Curriculum_Industry_Skill_Alignment_4_Datasets_500_Each.xlsx
```

The script reads the workbook using:

```python
pd.ExcelFile(file_name)
```

and accesses the four named sheets.

**Project Purpose**

This project serves as a foundation for understanding **CSE skill gaps between academic education and industry expectations**, while providing a starting point for incorporating **MLOps and feature-store technologies such as Feast** into the workflow.
