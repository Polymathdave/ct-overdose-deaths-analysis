# Connecticut Accidental Drug-Related Deaths (2012–2024): Data Analysis

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

An end-to-end analysis of the public **Accidental Drug-Related Deaths 2012–2024** dataset for the State of Connecticut. It covers loading and cleaning the raw records, statistical testing and a regression model, and is structured using the **CRISP-DM** methodology.

## ❓ Research questions
| # | Question |
|---|----------|
| RQ1 | How have accidental drug-related deaths changed from 2012 to 2024? |
| RQ2 | Which substances are most commonly involved? |
| RQ3 | What is the demographic profile of victims? |
| RQ4 | Is fentanyl involvement associated with sex? |

## 🔄 Workflow
```
Raw CSV ──► Load & profile ──► Clean & engineer features ──► Descriptive analysis ──► Statistical tests ──► Logistic regression
```
1. **Data loading & profiling**: record counts, schema and column-level missingness.
2. **Pre-processing & feature engineering**: type coercion (e.g. Age to numeric), converting substance flags from `Y`/blank to `1`/`0`, and dropping records missing essential fields.
3. **Descriptive analysis**: trends, substance totals and demographics, with outlier detection using the IQR rule and z-scores.
4. **Inferential statistics**:
   - Shapiro-Wilk normality check
   - Welch's two-sample t-test with Cohen's *d* effect size
   - Pearson chi-square test of independence with Cramér's *V*
5. **Multivariate logistic regression**: `Fentanyl ~ Age + Sex + Race`, giving adjusted odds ratios.

## 📁 Repository structure
```
├── Accidental_Drug_Related_Deaths_2012-2024.csv   # Source dataset
├── LD7186_Section1_Practical .ipynb               # Notebook with outputs and charts
└── README.md
```

## ▶️ How to run
```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels jupyter
jupyter notebook "LD7186_Section1_Practical .ipynb"
```

## 🧰 Skills demonstrated
Data cleaning · Data quality checks · Feature engineering · Exploratory data analysis · Hypothesis testing · Regression modelling · Data visualisation
