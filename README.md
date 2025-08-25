# Employee Attrition Prediction

## 📌 Project Description

This project focuses on analyzing and predicting **employee attrition** using machine learning techniques. Employee attrition is a critical issue in human resources management, as high turnover leads to increased costs, knowledge loss, and reduced organizational performance.

The repository provides **end-to-end workflows** from data cleaning and exploratory data analysis (EDA) to model building, evaluation, and explainability to identify the key factors driving attrition and to predict employees most at risk of leaving.

---

## 🎯 Goals

* Understand the **key drivers of employee attrition**.
* Build predictive models to identify at-risk employees.
* Provide **actionable insights** to HR teams for retention strategies.

---

## 📂 Project Structure

```
employee-attrition/
├─ data/             # Raw, interim, and processed data
├─ notebooks/        # Jupyter notebooks for EDA and modeling
├─ src/              # Source code for preprocessing, training, evaluation
├─ models/           # Trained model artifacts
├─ reports/          # Visualizations, figures, and summary tables
├─ config/           # Config files (e.g., feature definitions, params)
├─ requirements.txt  # Python dependencies
└─ README.md         # Project documentation
```

---

## 📊 Dataset

* **Target variable**: `Attrition` (Yes/No).
* **Features**: Mix of categorical (JobRole, Department, MaritalStatus, etc.) and numerical (Age, MonthlyIncome, YearsAtCompany, etc.).
* Source: Synthetic HR dataset (commonly used IBM HR dataset) or internal HR data.

---

## ⚙️ Setup & Installation

```bash
# Clone repository
git clone https://github.com/mrsugamrijal/employee-attrition.git
cd employee-attrition

# Create virtual environment
python -m venv .venv
source .venv/bin/activate   # On Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

---

## ▶️ How to Run

1. Place raw data in the `data/raw/` folder.
2. Run the EDA notebooks in `notebooks/`.
3. Train models:

   ```bash
   python -m src.train --config config/config.yaml
   ```
4. Evaluate model:

   ```bash
   python -m src.evaluate --config config/config.yaml
   ```
5. Outputs (trained models, evaluation figures) are stored in `models/` and `reports/`.

---

## 🔎 Exploratory Data Analysis (EDA)

* Checked for missing values and outliers.
* Analyzed distributions of numerical features.
* Examined attrition rates across categorical features (e.g., JobRole, OverTime, MaritalStatus).
* Visualized correlations using heatmaps and pair plots.

---

## 🤖 Modeling

* **Baseline**: Logistic Regression (with class weights).
* **Alternative models**: Decision Tree, Random Forest, Gradient Boosting.
* Feature engineering: one-hot encoding for categorical variables, scaling for numeric features.
* Class imbalance handled via **SMOTE** and `class_weight=balanced`.

---

## 📈 Evaluation Metrics

* Accuracy, Precision, Recall, F1-score.
* ROC AUC and PR AUC.
* Confusion matrix for class-level performance.

---

## ✨ Results & Insights

* **Key attrition drivers**: Overtime, Job Role (Sales/Tech), being Single, and lack of promotions.
* **Retention factors**: Higher Monthly Income, Senior Job Levels, Years with Current Manager, Job Satisfaction.
* Logistic regression odds ratios and tree-based feature importance highlighted actionable HR levers.

---

## 📊 Visualizations

* Bar charts (Attrition by department, overtime, job role).
* Scatter plots (Salary vs Attrition, YearsAtCompany vs Attrition).
* Box plots (Attrition by MonthlyIncome, WorkLifeBalance).
* Confusion matrix, ROC/PR curves.
* SHAP plots for explainability.

---

## 🔍 Explainability

* Logistic Regression coefficients → Odds ratios for interpretability.
* Tree-based models → Feature importance ranking.
* SHAP → Local and global explanations for HR decision-making.

---

## ⚠️ Limitations & Ethics

* Dataset may not capture real-world biases (synthetic).
* Predictions should **support, not replace** HR judgment.
* Fairness audits and ethical considerations are recommended before deployment.

---

## 🚀 Future Work

* Deploy as a dashboard or API for HR teams.
* Explore advanced models (XGBoost, LightGBM).
* Real-time attrition monitoring.
* Fairness and bias mitigation techniques.

---

## 📜 License

This project is licensed under the **MIT License** — feel free to use and adapt.

---
