# 🎓 Student Performance Analysis  
### Exploratory Data Analysis — Mini Project  

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter&logoColor=white"/>
  <img src="https://img.shields.io/badge/Pandas-EDA-green?style=for-the-badge&logo=pandas&logoColor=white"/>
  <img src="https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge"/>
</p>

---

## 📽️ Project Info

| Field | Details |
|---|---|
| **Subject** | Exploratory Data Analysis |
| **Semester** | Sem 2 – B.Tech |
| **Project Type** | Mini Project |
| **Dataset** | Students Performance Dataset |
| **Author** | Ansh Yadav |

---

## 📌 Project Overview

This project analyzes student performance based on various factors such as gender, race/ethnicity, parental education, lunch type, and test preparation course.

Using **Python-based Exploratory Data Analysis (EDA)** techniques, we uncover patterns in student scores across **Math, Reading, and Writing**, and identify key factors affecting academic performance.

---

## 📂 Repository Structure

```
📦 Student-Performance-EDA
 ┣ 📓 Student_Performance_EDA.ipynb
 ┣ 📄 StudentsPerformance.csv
 ┣ 📄 README.md
 ┗ 📁 visuals/
```

---

## 📊 Dataset Description

| Column | Description |
|---|---|
| `gender` | Student gender |
| `race_ethnicity` | Ethnic group |
| `parent_education` | Parent's education level |
| `lunch` | Type of lunch |
| `test_prep` | Test preparation course |
| `math_score` | Math marks |
| `reading_score` | Reading marks |
| `writing_score` | Writing marks |
| `average_score` | Average score |
| `total` | Total |

---

## 🔬 EDA Techniques Applied

### 1️⃣ Dataset Loading & Cleaning
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_csv('StudentsPerformance.csv')

df.rename(columns={
    'race/ethnicity': 'race_ethnicity',
    'parental level of education': 'parent_education',
    'test preparation course': 'test_prep',
    'math score': 'math_score',
    'reading score': 'reading_score',
    'writing score': 'writing_score',
    'Average Score': 'average_score'
}, inplace=True)
```

### 2️⃣ Dataset Inspection
```python
df.head()
df.tail()
df.info()
df.dtypes
df.shape
```

### 3️⃣ Descriptive Statistics
```python
df.describe()
df['math_score'].mean()
df['reading_score'].median()
df['writing_score'].std()
```

### 4️⃣ Missing Values
```python
df.isnull().sum()
(df.isnull().sum()/len(df))*100
```

### 5️⃣ Frequency Count
```python
df['gender'].value_counts()
df['race_ethnicity'].value_counts()
```

### 6️⃣ Unique Values
```python
df.nunique()
df['gender'].unique()
```

### 7️⃣ Percentage Distribution
```python
df['gender'].value_counts(normalize=True)*100
```

### 8️⃣ Filtering Data
```python
df[df['average_score']>=90]
df[df['math_score']<40]
```

### 9️⃣ Crosstab
```python
pd.crosstab(df['gender'], df['test_prep'])
```

### 🔟 Groupby
```python
df.groupby('gender')[['math_score','reading_score','writing_score']].mean()
```

### 1️⃣1️⃣ Sorting
```python
df.sort_values(by='average_score', ascending=False)
```

### 1️⃣2️⃣ Derived Columns
```python
def assign_grade(score):
    if score >= 80: return 'Distinction'
    elif score >= 60: return 'First Class'
    elif score >= 40: return 'Pass'
    else: return 'Fail'

df['grade_category'] = df['average_score'].apply(assign_grade)
df['score_gap'] = df['reading_score'] - df['math_score']
```

### 1️⃣3️⃣ Visualizations
```python
sns.countplot(data=df, x='race_ethnicity')
sns.histplot(df['math_score'])
```

---

## 📈 Key Insights

- Students completing test preparation score higher  
- Parental education impacts performance  
- Some students are at risk (low math scores)  
- Gender-based performance differences exist  

---

## 🛠️ Tech Stack

```
Python
Pandas
NumPy
Matplotlib
Seaborn
```

---

## 🚀 How to Run

```bash
git clone https://github.com/<your-username>/student-performance-eda.git
cd student-performance-eda
jupyter notebook
```

Make sure `StudentsPerformance.csv` is in the same folder.

---

## 📝 Acknowledgements

- Dataset: Student Performance Dataset  
- Libraries: Pandas, Matplotlib, Seaborn  

---

<p align="center">
  Made by <strong>Ansh Yadav</strong>
</p>
