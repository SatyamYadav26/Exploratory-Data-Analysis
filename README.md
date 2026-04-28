📌 Overview

This project performs Exploratory Data Analysis (EDA) on a Kaggle dataset to uncover patterns, detect outliers, and understand feature distributions.

It focuses on data cleaning, preprocessing, and visualization to prepare the dataset for further machine learning tasks.

📂 Dataset
File: kaggle_datasets_all_merged.csv

Contains dataset-level metrics such as:

📥 Total Downloads

👁 Total Views

👍 Total Votes

⭐ Usability Rating

📦 Dataset Size (totalBytes)

⚙ Kernel Count

🛠 Tech Stack

Python

Pandas

NumPy

Matplotlib

Seaborn

Jupyter Notebook

🔍 Workflow

1️⃣ Data Loading
Loaded dataset using Pandas
Previewed using .head()

2️⃣ Data Understanding
Used .info() and .describe()
Checked data types and distributions

3️⃣ Data Cleaning
Removed unnecessary columns:
Unnamed: 0
id
datasetId

4️⃣ Handling Missing Values
Identified null values
Ensured dataset consistency

5️⃣ Outlier Removal
Applied IQR (Interquartile Range) method:
Removed extreme values
Improved data reliability

6️⃣ Data Visualization
Histograms for numerical features:
Downloads
Views
Votes
Ratings
Dataset size
📈 Key Insights
Dataset metrics are highly skewed
Presence of significant outliers in downloads & views
Data cleaning improves interpretability
