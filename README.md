# Diwali Sales Analysis & Customer Segmentation

An exploratory data analysis project using Python to study festive-season sales patterns and segment customers based on purchasing behavior.

## Objectives

- Analyze sales by gender and age group.
- Explore state-wise and occupation-wise sales.
- Identify top-performing product categories.
- Apply K-Means clustering to customer-level features.
- Develop evidence-based business recommendations.

## Tech Stack

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Structure

```text
Diwali-Sales-Analysis/
├── data/
│   └── Diwali Sales Data.csv
├── Diwali Sales Data Analysis and Customer Segmentation.ipynb
├── requirements.txt
├── .gitignore
└── README.md
```

## Setup

Create and activate a virtual environment:

```bash
python -m venv .venv
```

Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
python -m pip install -r requirements.txt
```

Open the notebook in VS Code and select the `.venv` Python kernel.

## Customer Segmentation

K-Means clustering was applied to customer-level spending, transaction-record count, and average spending features. The number of clusters was evaluated using the elbow method and silhouette score.

The current exploratory analysis selected two clusters for further interpretation.

## Limitations

- The dataset represents festive-season sales.
- Transaction-record count is used as a proxy for purchase frequency.
- Clusters depend on the selected features and model configuration.
- The dataset's redistribution terms should be checked before publishing it.

## Future Improvements

- Validate cluster stability and business usefulness.
- Improve customer-segment visualizations.
- Add stronger, quantified business recommendations.