# COVID-19 Data Analysis

## 📌 Project Overview

This project performs an **Exploratory Data Analysis (EDA)** on COVID-19 data to analyze the spread and impact of the pandemic across different regions.

Using **Python, Pandas, NumPy, and Matplotlib**, the project explores confirmed cases, deaths, and recovered cases and identifies the regions with the highest and lowest numbers of reported cases.

## 🎯 Objectives

The main objectives of this project are:

* Analyze COVID-19 data across different regions.
* Check the dataset for missing values and duplicate records.
* Calculate total confirmed cases by region.
* Calculate total deaths by region.
* Calculate total recovered cases by region.
* Identify regions with the highest number of confirmed cases.
* Identify regions with the lowest number of confirmed cases.
* Identify regions with the highest number of deaths.
* Analyze COVID-19 data specifically for India and Brazil.
* Sort regions based on confirmed and recovered cases.

## 📂 Dataset

The project uses the **COVID-19 dataset** stored in:

```text
4. Covid_19_data.csv
```

The analysis uses the following important columns:

| Column      | Description                                       |
| ----------- | ------------------------------------------------- |
| `Region`    | Region/country where COVID-19 cases were reported |
| `Confirmed` | Number of confirmed COVID-19 cases                |
| `Deaths`    | Number of reported deaths                         |
| `Recovered` | Number of recovered cases                         |

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Jupyter Notebook**

## 🔍 Data Analysis Performed

### 1. Data Loading

The dataset is loaded using Pandas:

```python
data = pd.read_csv("4. Covid_19_data.csv")
```

The complete dataset is then displayed and explored.

### 2. Dataset Columns

The project checks the available columns using:

```python
data.columns
```

This helps understand the structure of the dataset before performing analysis.

### 3. Missing Value Analysis

Missing values are checked using:

```python
data.isnull().sum()
```

This helps determine whether the dataset contains incomplete records.

### 4. Duplicate Analysis

Duplicate records are identified using:

```python
data.duplicated().sum()
```

This helps assess the quality and uniqueness of the dataset.

### 5. Confirmed Cases by Region

The total number of confirmed COVID-19 cases is calculated for each region:

```python
data.groupby('Region')['Confirmed'].sum()
```

This provides a region-wise view of the spread of COVID-19.

### 6. Deaths by Region

The total number of deaths is calculated for each region:

```python
data.groupby('Region')['Deaths'].sum()
```

### 7. Recovered Cases by Region

The total number of recovered cases is calculated using:

```python
data.groupby('Region')['Recovered'].sum()
```

### 8. Regions with Fewer Than 10 Confirmed Cases

The project filters the dataset to identify records where confirmed cases are below 10:

```python
data[data.Confirmed < 10]
```

### 9. Top 5 Regions by Confirmed Cases

The five regions with the highest number of confirmed cases are identified using:

```python
data.groupby('Region')['Confirmed'].sum() \
    .sort_values(ascending=False).head(5)
```

### 10. Bottom 5 Regions by Confirmed Cases

The five regions with the lowest number of confirmed cases are identified using:

```python
data.groupby('Region')['Confirmed'].sum() \
    .sort_values(ascending=True).head(5)
```

### 11. Top 10 Regions by Deaths

The project identifies the ten regions with the highest total number of deaths:

```python
data.groupby('Region')['Deaths'].sum() \
    .sort_values(ascending=False).head(10)
```

### 12. India Analysis

COVID-19 records for **India** are filtered separately:

```python
data[data.Region == 'India']
```

This allows the COVID-19 data for India to be examined independently.

### 13. Brazil Analysis

Similarly, records for **Brazil** are extracted:

```python
data[data.Region == 'Brazil']
```

### 14. Sorting by Confirmed Cases

The dataset is sorted in descending order based on confirmed cases:

```python
data.sort_values(by=['Confirmed'], ascending=False)
```

This makes it easier to identify records with the highest number of confirmed cases.

### 15. Sorting by Recovered Cases

The dataset is also sorted based on recovered cases:

```python
data.sort_values(by=['Recovered'], ascending=True)
```

## 📊 Key Analysis Areas

The project focuses on three major COVID-19 indicators:

**Confirmed Cases →** Measures the reported spread of COVID-19.

**Deaths →** Helps understand the impact of COVID-19 across regions.

**Recovered Cases →** Provides an overview of reported recoveries.

The region-wise grouping and sorting operations make it possible to compare these indicators across different regions.

## 📁 Project Structure

```text
COVID-19-Data-Analysis/
│
├── Covid19 Project.ipynb
├── 4. Covid_19_data.csv
└── README.md
```

## ▶️ How to Run the Project

### 1. Clone the Repository

```bash
git clone <your-github-repository-url>
```

### 2. Navigate to the Project Directory

```bash
cd COVID-19-Data-Analysis
```

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib jupyter
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open the Notebook

Open:

```text
Covid19 Project.ipynb
```

Make sure the dataset:

```text
4. Covid_19_data.csv
```

is available in the same directory as the notebook.

## 💡 Skills Demonstrated

This project demonstrates practical experience with:

* Python Programming
* Pandas
* NumPy
* Data Loading
* Data Cleaning
* Missing Value Checking
* Duplicate Detection
* Data Filtering
* Data Sorting
* GroupBy Operations
* Aggregation
* Exploratory Data Analysis
* Region-wise Data Analysis

## 👩‍💻 Author

**Ashwitha Gogikar**

Data Analytics | Python | Power BI | Machine Learning

* GitHub: https://github.com/gshwitha2000-wq
* LinkedIn: https://www.linkedin.com/in/ashwitha-gogikar-35839a1b5/
