# 📊 Kaggle Dataset EDA Project

## 📌 Overview

This project performs **Exploratory Data Analysis (EDA)** on a Kaggle dataset to uncover patterns, detect outliers, and understand feature distributions.

The project focuses on:

- 🧹 Data Cleaning
- 🔍 Missing Value Handling
- 📉 Outlier Detection & Removal
- 📊 Data Visualization
- 📚 Feature Understanding

The cleaned dataset can be further used for Machine Learning and Data Analysis tasks.

---

# 📂 Dataset

**Dataset File:** `kaggle_datasets_all_merged.csv`

The dataset contains important dataset-level metrics such as:

- 📥 Total Downloads
- 👁 Total Views
- 👍 Total Votes
- ⭐ Usability Rating
- 📦 Dataset Size (`totalBytes`)
- ⚙ Kernel Count

---

# 🛠 Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

# 🔍 Workflow

## 1️⃣ Data Loading

- Loaded dataset using Pandas
- Previewed dataset using `.head()`

```python
df = pd.read_csv("kaggle_datasets_all_merged.csv")
df.head()
```

---

## 2️⃣ Data Understanding

Used:

```python
df.info()
df.describe()
```

This helped in:

- Understanding data types
- Identifying numerical features
- Detecting missing values
- Observing feature distributions

---

## 3️⃣ Data Cleaning

Removed unnecessary columns:

- `Unnamed: 0`
- `id`
- `datasetId`

```python
df.drop(columns=['Unnamed: 0', 'id', 'datasetId'], inplace=True)
```

---

## 4️⃣ Handling Missing Values

Checked null values using:

```python
df.isnull().sum()
```

Ensured dataset consistency before analysis.

---

## 5️⃣ Outlier Removal

Applied the **IQR (Interquartile Range)** method to remove extreme values.

### Formula

\[
IQR = Q3 - Q1
\]

```python
Q1 = df[column].quantile(0.25)
Q3 = df[column].quantile(0.75)

IQR = Q3 - Q1

lower = Q1 - 1.5 * IQR
upper = Q3 + 1.5 * IQR

df = df[(df[column] >= lower) & (df[column] <= upper)]
```

### Benefits

- Reduced impact of extreme values
- Improved visualization clarity
- Increased data reliability

---

# 📊 Data Visualization

Visualized numerical features using:

- Histograms
- Distribution Plots
- Boxplots

### Features Visualized

- Downloads
- Views
- Votes
- Ratings
- Dataset Size

Example:

```python
sns.histplot(df['totalDownloads'], kde=True)
plt.show()
```

---

# 📈 Key Insights

- Dataset metrics are highly skewed
- Significant outliers exist in:
  - Downloads
  - Views
  - Votes
- Data cleaning improved interpretability
- Visualization helped identify distribution trends

---

# 🚀 Future Improvements

- Feature Engineering
- Correlation Analysis
- Machine Learning Model Building
- Dashboard Creation using Power BI/Tableau

---

# ▶️ How to Run

## 1️⃣ Clone the Repository

```bash
git clone <your-repository-link>
```

## 2️⃣ Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn
```

## 3️⃣ Run the Notebook

```bash
jupyter notebook
```

---

# 📁 Project Structure

```bash
├── kaggle_datasets_all_merged.csv
├── EDA_Project.ipynb
├── README.md
└── requirements.txt
```

---

# 🤝 Contributing

Contributions are welcome!

Feel free to fork this repository and improve the project.

---

# 📜 License

This project is for educational and learning purposes.
