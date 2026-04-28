📌 Project Overview

This project performs Explatory Data Analysis (EDA) on a merged Kaggle dataset containing information about datasets such as downloads, views, votes, usability ratings, and more.

The goal is to:

Understand dataset structure
Clean and preprocess data
Handle missing values and outliers
Visualize key patterns and distributions
📂 Dataset

The dataset used:

kaggle_datasets_all_merged.csv

It contains features like:

totalBytes
kernelCount
usabilityRating
totalDownloads
totalViews
totalVotes
⚙️ Technologies Used
Python 🐍
Pandas
NumPy
Matplotlib
Seaborn
🔍 Steps Performed
1. Data Loading
Imported dataset using Pandas
Displayed first few rows for initial understanding
2. Data Inspection
Checked dataset structure using .info()
Generated statistical summary using .describe()
3. Missing Values Handling

Identified missing values using:

df.isnull().sum()
4. Data Cleaning
Dropped unnecessary columns:
Unnamed: 0
id
datasetId
5. Outlier Detection & Removal
Used IQR (Interquartile Range) method:
Calculated Q1, Q3, and IQR
Removed extreme values beyond threshold
6. Data Visualization
Generated histograms for numerical features:
totalBytes
kernelCount
usabilityRating
totalDownloads
totalViews
totalVotes
📈 Key Insights
Distribution of dataset metrics varies significantly
Some features show skewness due to high-value outliers
Cleaning improves data quality and reliability for further analysis
▶️ How to Run
Clone this repository:
git clone <your-repo-link>
Install dependencies:
pip install pandas numpy matplotlib seaborn
Run the notebook:
jupyter notebook eda.ipynb
📌 Future Improvements
Add correlation heatmaps
Perform feature engineering
Build predictive models (ML)
Interactive dashboards (Plotly / Power BI)
