# netflix-data-cleaning-task
Data cleaning and preprocessing task for internship using the Netflix Movies and TV Shows dataset. Includes handling missing values, standardizing formats, fixing column names, and converting date formats using Python and Pandas.
# Netflix Data Cleaning – Internship Task

This repository contains the solution to **Task 1: Data Cleaning and Preprocessing** for a data analyst internship. The dataset used is the **Netflix Movies and TV Shows dataset**, originally sourced from Kaggle.

## 📂 Dataset Overview

- **File**: `netflix_titles.csv`
- **Rows**: 8807
- **Columns**: 12
- **Fields include**: `title`, `type`, `country`, `cast`, `date_added`, `rating`, `duration`, etc.

## 🧼 Cleaning Steps Performed

### ✅ 1. Handled Missing Values
- Checked null values using `.isnull().sum()`
- Kept critical rows with missing `director`, `cast`, and `country` — flagged them for potential analysis impact
- 10 missing `date_added` entries were preserved as `NaT`

### ✅ 2. Removed Duplicates
- Used `.drop_duplicates()` — found **0 duplicate rows**

### ✅ 3. Standardized Column Names
- All column names were converted to lowercase with underscores for consistency  
  Example: `Date Added` → `date_added`

### ✅ 4. Converted Date Formats
- Parsed `date_added` using `pd.to_datetime()`
- Reformatted to `dd/mm/yyyy` using `.dt.strftime('%d/%m/%Y')`

### ✅ 5. Verified Data Types
- `release_year` is `int`
- `date_added` is stored as a formatted string
- Other columns are of type `object` (text)

## 📦 Files Included

- `netflix_cleaning_code.py` or `.ipynb`: Python script or notebook used for cleaning
- `cleaned_netflix_data.csv`: Final cleaned dataset
- `README.md`: This file

## 🛠 Tools Used

- Python 3.x
- Pandas
- Jupyter Notebook or VS Code

## 🎯 Learning Outcome

Through this task, I gained hands-on experience in:
- Identifying and handling missing values
- Fixing formatting issues in real-world data
- Using Pandas effectively for data wrangling and transformation
- Preparing data for analysis or machine learning



