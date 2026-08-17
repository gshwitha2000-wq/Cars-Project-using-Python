# 🚗 Cars Data Analysis

## 📌 Project Overview

This project performs a basic **Exploratory Data Analysis (EDA)** on a cars dataset using Python.

The analysis focuses on understanding the structure of the dataset, examining car manufacturers, identifying heavy vehicles, and comparing the **minimum and maximum Manufacturer's Suggested Retail Price (MSRP)** across different regions of origin.

The project uses **Pandas, NumPy, and Matplotlib** for data loading, exploration, filtering, and analysis.

## 🎯 Objectives

The main objectives of this project are:

* Load and explore the cars dataset.
* Understand the columns and data types.
* Generate descriptive statistics.
* Check for duplicate records.
* Identify different car manufacturers.
* Count the number of cars for each manufacturer.
* Find cars weighing more than 4,000 units.
* Find the costliest car in each region.
* Find the cheapest car in each region.

## 📂 Dataset

The project uses the following dataset:

```text
2. Cars Data1.csv
```

The dataset contains information about different cars, including their manufacturer, origin, weight, and MSRP.

### Important Columns Used

| Column   | Description                           |
| -------- | ------------------------------------- |
| `Make`   | Car manufacturer/brand                |
| `Origin` | Region or country of origin           |
| `Weight` | Weight of the car                     |
| `MSRP`   | Manufacturer's Suggested Retail Price |

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Jupyter Notebook**

## 🔍 Analysis Performed

### 1. Importing the Dataset

The CSV dataset is loaded using Pandas:

```python
data = pd.read_csv("2. Cars Data1.csv")
```

The complete dataset is then displayed for initial inspection.

### 2. Checking Dataset Columns

The project examines the available columns using:

```python
data.columns
```

This helps understand the structure and attributes available in the dataset.

### 3. Dataset Information

The `info()` function is used to inspect:

* Number of records
* Number of columns
* Data types
* Non-null values

```python
data.info()
```

### 4. Descriptive Statistics

The project uses:

```python
data.describe()
```

to generate descriptive statistics for the numerical columns.

This provides information such as:

* Count
* Mean
* Standard deviation
* Minimum
* Maximum
* Quartiles

### 5. Duplicate Records

Duplicate records are checked using:

```python
data.duplicated().sum()
```

This helps identify whether duplicate rows exist in the dataset.

### 6. Different Car Manufacturers

The project identifies all unique car manufacturers using:

```python
data.Make.unique()
```

This provides an overview of the different brands represented in the dataset.

### 7. Number of Cars by Manufacturer

The number of cars belonging to each manufacturer is calculated using:

```python
data.Make.value_counts()
```

This helps determine which manufacturers have the highest representation in the dataset.

### 8. Cars Weighing More Than 4,000

The project filters the dataset to find cars with a weight greater than 4,000:

```python
data[data['Weight'] > 4000]
```

This allows heavy vehicles in the dataset to be identified.

### 9. Costliest Car in Each Region

The maximum MSRP for each region of origin is calculated using:

```python
data.groupby('Origin')['MSRP'].max()
```

This identifies the highest-priced car available in each region represented in the dataset.

### 10. Cheapest Car in Each Region

The minimum MSRP for each region is calculated using:

```python
data.groupby('Origin')['MSRP'].min()
```

This provides the lowest car price for each region.

## 📊 Key Analysis Areas

The project explores the following areas:

**Manufacturer Analysis**
Identifies different car brands and the number of cars associated with each manufacturer.

**Weight Analysis**
Filters vehicles based on their weight to identify cars weighing more than 4,000.

**Regional Price Analysis**
Uses `groupby()` to compare the highest and lowest MSRP across different regions.

**Data Quality Analysis**
Uses dataset information, descriptive statistics, and duplicate checks to understand the quality and structure of the data.

## 💡 Skills Demonstrated

This project demonstrates practical knowledge of:

* Python
* Pandas
* NumPy
* Matplotlib
* Data Loading
* Data Inspection
* Descriptive Statistics
* Duplicate Detection
* Unique Value Analysis
* Value Counts
* Data Filtering
* GroupBy Operations
* Aggregation
* Exploratory Data Analysis

## 📁 Project Structure

```text
Cars-Data-Analysis/
│
├── Cars Data Project.ipynb
├── 2. Cars Data1.csv
└── README.md
```

## ▶️ How to Run the Project

### 1. Clone the Repository

```bash
git clone <your-github-repository-url>
```

### 2. Navigate to the Project Folder

```bash
cd Cars-Data-Analysis
```

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib jupyter
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open the Notebook

Open:

```text
Cars Data Project.ipynb
```

Make sure the dataset:

```text
2. Cars Data1.csv
```

is present in the same folder as the notebook.

## 👩‍💻 Author

**Ashwitha Gogikar**

Data Analytics | Python | Power BI | Machine Learning

* GitHub: https://github.com/gshwitha2000-wq
* LinkedIn: https://www.linkedin.com/in/ashwitha-gogikar-35839a1b5/
