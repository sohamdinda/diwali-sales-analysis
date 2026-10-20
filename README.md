# 🪔 Diwali Sales Analysis & Customer Segmentation

An exploratory data analysis and machine learning project focused on understanding festive-season purchasing patterns and identifying customer groups using Python.

## 📌 Project Overview

This project analyzes Diwali sales data to explore customer demographics, purchasing behavior, product categories, and regional sales patterns. It also applies **K-Means clustering** to group customers based on spending-related features.

The goal is to turn sales data into actionable business insights and demonstrate an end-to-end data analysis workflow.

## 🎯 Objectives

- Analyze sales patterns by gender and age group.
- Explore state-wise and occupation-wise purchasing behavior.
- Identify top-performing product categories.
- Perform customer-level feature engineering.
- Apply K-Means clustering for exploratory customer segmentation.
- Develop data-driven business recommendations.

## 🛠️ Tech Stack

- **Language:** Python
- **Data analysis:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine learning:** Scikit-learn (StandardScaler, K-Means)
- **Environment:** Jupyter Notebook, VS Code

## 📂 Project Structure

```text
Diwali-Sales-Analysis/
├── data/  # Local dataset; not included in Git
├── Diwali Sales Data Analysis and Customer Segmentation.ipynb
├── requirements.txt
├── .gitignore
└── README.md
```

## 🔍 Analysis Workflow

1. **Data cleaning:** Removed fully empty columns, handled missing `Amount` values, standardized column names, and removed exact duplicate rows.
2. **Exploratory data analysis:** Examined sales patterns across gender, age group, state, occupation, and product category.
3. **Feature engineering:** Aggregated transaction records into customer-level spending features.
4. **Feature scaling:** Standardized numerical features before clustering.
5. **Customer segmentation:** Evaluated candidate cluster counts using the elbow method and silhouette score.
6. **Interpretation:** Compared the resulting customer groups and considered potential business applications.

## 🤖 Customer Segmentation

K-Means clustering was applied using three customer-level features:

- Total spending
- Transaction-record count
- Average spending per transaction

The features were standardized using `StandardScaler`. Candidate cluster counts from **2 to 7** were evaluated.

| Metric | Result |
|---|---:|
| Selected cluster count | 2 |
| Silhouette score for K=2 | 0.517 |
| Customers in Cluster 0 | 580 |
| Customers in Cluster 1 | 3,172 |

The two clusters showed differences in spending and transaction-record counts. Cluster 0 contained fewer customers with a higher average number of transaction records, while Cluster 1 contained more customers with a lower average number of records.

These clusters are **exploratory segments**, not validated customer types. Further evaluation is needed to establish their stability and business usefulness.

## 💡 Potential Business Applications

- Explore targeted campaigns for customers with different purchasing patterns.
- Investigate opportunities to increase repeat purchases among lower-frequency customers.
- Compare product-category preferences across customer segments.
- Use regional and demographic patterns to guide further marketing analysis.

These are potential applications of the analysis; their effectiveness would need to be tested using additional data.

## ⚙️ Setup and Installation

### 1. Clone the repository

```bash
git clone https://github.com/sohamdinda/diwali-sales-analysis.git
cd diwali-sales-analysis
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

### 3. Activate the environment

**Windows PowerShell:**

```powershell
.\.venv\Scripts\Activate.ps1
```

### 4. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 5. Add the dataset

Place the authorized dataset file at:

```text
data/Diwali Sales Data.csv
```

The dataset is excluded from this repository. Obtain it from an authorized source before running the notebook.

### 6. Run the notebook

Open `Diwali Sales Data Analysis and Customer Segmentation.ipynb` in VS Code, select the `.venv` Python kernel, and run the cells in order.

## ⚠️ Limitations

- The dataset represents a specific festive-season sales period and may not generalize to other periods.
- Transaction-record count is a proxy for purchase frequency, not a confirmed count of distinct orders.
- Total spending, average spending, and transaction count may be correlated.
- The selected cluster count and resulting segments require further validation.
- Dataset access and redistribution permissions should be checked before sharing the data.

## 🚀 Future Improvements

- Validate cluster stability using alternative initializations and clustering methods.
- Compare alternative feature sets and evaluate the influence of correlated features.
- Create clearer customer-segment visualizations.
- Quantify business findings with additional validated metrics.
- Test whether the segments support useful marketing decisions.

## 👨‍💻 Author

**Soham Dinda**

GitHub: [@sohamdinda](https://github.com/sohamdinda)

---

*This project is for educational and analytical purposes.*
