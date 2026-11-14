# Medical Insurance Premium Prediction Using Machine Learning

## Project Overview

This project focuses on predicting annual medical insurance premiums using Machine Learning techniques, primarily Linear Regression.

The objective is to help understand how demographic, lifestyle, and health-related factors influence insurance premiums and develop an interpretable predictive model.

The project uses Python for data analysis, statistical testing, visualization, data preprocessing, and Machine Learning model development.

## Business Problem

Insurance providers need to estimate annual premiums based on customer characteristics such as age, BMI, smoking status, medical conditions, and lifestyle.

The goal is to build a predictive model that estimates insurance premiums while identifying the factors that contribute most to premium variations.

## Dataset Information

- **Dataset:** Medical Insurance Dataset (Synthetic)
- **Records:** 2,500
- **Features:** 11 independent variables
- **Target Variable:** `annual_premium`
- **Target Unit:** USD

### Features Used

| Feature | Description |
|---|---|
| age | Customer age |
| sex | Customer gender |
| bmi | Body Mass Index |
| children | Number of children |
| smoker | Smoking status |
| region | Customer region |
| exercise_freq | Exercise frequency |
| chronic_conditions | Number of chronic conditions |
| annual_income | Annual income |
| blood_pressure | Blood pressure |
| cholesterol | Cholesterol level |

## Technologies & Libraries

- **Programming Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Statistical Analysis:** SciPy, Statsmodels
- **Machine Learning:** Scikit-learn

## Project Workflow

1. **Data Loading & Understanding**
   - Imported the dataset using Pandas.
   - Examined dataset dimensions, data types, and statistical summaries.
   - Identified missing values and data-quality issues.

2. **Exploratory Data Analysis (EDA)**
   - Analyzed numerical and categorical variables.
   - Created histograms, box plots, and correlation heatmaps.
   - Studied relationships between customer characteristics and insurance premiums.

3. **Data Cleaning & Preprocessing**
   - Detected outliers using the IQR method.
   - Applied outlier capping (Winsorization).
   - Handled missing values using mean, median, mode, and KNN imputation.
   - Encoded categorical variables.
   - Applied feature scaling using StandardScaler.

4. **Statistical Analysis**
   - Conducted hypothesis testing using:
     - Independent T-test
     - ANOVA
     - Chi-Square test
   - Performed correlation analysis.
   - Checked multicollinearity using VIF.
   - Evaluated Linear Regression assumptions.

5. **Machine Learning Model Development**
   - Implemented Linear Regression using Scikit-learn.
   - Built an OLS model using Statsmodels.
   - Applied Ridge, Lasso, and Elastic Net regression.
   - Used train, validation, and test datasets.
   - Performed 5-fold cross-validation.

6. **Model Evaluation**
   - Evaluated models using:
     - R² Score
     - Adjusted R² Score
     - Mean Absolute Error (MAE)
     - Root Mean Squared Error (RMSE)
   - Analyzed residuals and checked model generalization.

## Model Performance

The following results were obtained on the test dataset:

| Model | R² Score | RMSE (USD) | MAE (USD) |
|---|---:|---:|---:|
| Linear Regression | 0.617 | 4,684.19 | 3,641.60 |
| Ridge Regression | 0.617 | 4,684.37 | 3,641.83 |
| Lasso Regression | 0.617 | 4,684.07 | 3,641.47 |
| Elastic Net | 0.535 | 5,160.09 | 4,069.76 |

**Best-performing approach:** Linear Regression and Lasso Regression achieved approximately 61.7% R² on the test dataset.

The mean 5-fold cross-validation R² score for Linear Regression was approximately 0.612.

## Key Insights

- Smoking status was the strongest predictor among the model's standardized coefficients.
- Age, BMI, and chronic conditions were also important premium-related factors.
- Linear Regression, Ridge, and Lasso produced similar predictive performance.
- Train, validation, and test R² scores were relatively close, indicating consistent model performance across the splits.
- The model achieved an MAE of approximately $3,642 on the test dataset.

## Project Structure

```text
medical-insurance-premium-prediction/
│
├── Insurance_Premium_Linear_Regression.ipynb
│
├── medical_insurance_2500_synthetic_1.csv
│
├── README.md
│
└── requirements.txt
```

## How to Run This Project

1. Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/medical-insurance-premium-prediction.git
```

2. Navigate to the project directory:

```bash
cd medical-insurance-premium-prediction
```

3. Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels scikit-learn jupyter
```

4. Open Jupyter Notebook:

```bash
jupyter notebook
```

5. Open `Insurance_Premium_Linear_Regression.ipynb` and run the notebook cells.

**Note:** Ensure the dataset CSV is placed in the project directory and update the dataset file path in the notebook if necessary.

## Future Improvements

- Perform hyperparameter tuning using GridSearchCV.
- Explore feature interactions such as BMI and smoking status.
- Apply target transformations to handle skewness.
- Compare performance with Random Forest and other non-linear regression algorithms.
- Improve predictive performance through feature engineering.

## Disclaimer

This project uses a synthetic dataset for educational and portfolio purposes. Predictions should not be used for actual insurance underwriting or medical decisions.

## Author

**Shaik Mahammad Saifulla**

Aspiring Data Analyst | Python | SQL | Power BI | Machine Learning

