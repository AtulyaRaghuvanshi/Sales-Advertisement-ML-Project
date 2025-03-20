# Sales-Advertisement-ML-Project
# Simple Linear Regression: Sales and Advertising Analysis

## Project Overview
This project implements a Simple Linear Regression model to explore and predict the linear relationship between **Sales** and **Advertising** expenditures for a dietary weight control product. Using a dataset spanning 36 months, the goal is to understand how sales influence advertising budgets and evaluate the model's performance using metrics like RMSE and R² score.

The project demonstrates fundamental machine learning concepts, including data preprocessing, model training, evaluation, and visualization, all implemented in Python using popular libraries such as Pandas, NumPy, Scikit-Learn, ව

## Dataset
The dataset is sourced from [http://www.econometrics.com/intro/sales.htm](http://www.econometrics.com/intro/sales.htm) and contains:
- **Sales**: Monthly sales data (independent variable, \(X\)).
- **Advertising**: Monthly advertising expenditure (dependent variable, \(y\)).
- **Format**: 36 rows, 2 columns, tab-separated, no headers.
- **File**: `sales.txt` (available in this repository).

Sample data (first 5 rows):
Sales  Advertising
12.0   15.0
20.5   16.0
21.0   18.0
15.5   27.0
15.3   21.0

## Prerequisites
To run this project, you’ll need:
- **Python**: Version 3.6 or higher (developed with 3.6.5).
- **Anaconda**: Recommended for managing dependencies (optional).
- **Libraries**:
  - `numpy` - Numerical computations.
  - `pandas` - Data manipulation.
  - `scikit-learn` - Machine learning tools.
  - `matplotlib` - Data visualization.
- **Jupyter Notebook**: For interactive execution (version 5.5.0 used).

Install dependencies via pip:
`pip install numpy pandas scikit-learn matplotlib jupyter`

Or use Anaconda:
`conda install numpy pandas scikit-learn matplotlib jupyter`

Sales-Advertising-Project/
│
├── SALES.txt              # Dataset file
├── regression_analysis.ipynb  # Jupyter Notebook with full code
└── README.md              # This file

## How to Run
1.Clone the Repository:
`git clone https://github.com/<your-username>/Sales-Advertising-Project.git
cd Sales-Advertising-Project`

2.Access the Dataset:
Locally: Ensure SALES.txt is in the project directory or adjust the path in the code.
Online: Use the raw GitHub URL:
`https://raw.githubusercontent.com/<your-username>/Sales-Advertising-Project/main/SALES.txt`

3. Open the Notebook
`jupyter notebook regression_analysis.ipynb`

4.Run the Code:
Execute all cells in the notebook to load the data, train the model, and visualize results.
Modify the url variable in the notebook to toggle between local and GitHub data sources:
`local_path = "SALES.txt"
github_url = "https://raw.githubusercontent.com/<your-username>/Sales-Advertising-Project/main/SALES.txt"
url = local_path if use_local else github_url`

## Key Steps in the Project
1 Data Loading: Import SALES.txt using Pandas.

2 Exploratory Data Analysis: Examine dataset structure, summary statistics, and visualize the Sales-Advertising relationship.

3 Model Building: Fit a Simple Linear Regression model using Scikit-Learn.


4 Evaluation: Compute RMSE (11.2273) and R² score (0.5789) to assess performance.

5 Visualization: Plot scatter points and the regression line, plus residual errors.

6 Conclusion: The model underfits (low training score: 0.2861) and isn’t suitable for deployment (R² < 0.7), suggesting a need for a more complex approach like polynomial regression.


## Results
- **Model Equation**: \( y = 1.6051 \cdot X - 11.1600 \)
- **Performance**:
  - **RMSE**: 11.2273 (high error indicates poor fit).
  - **R² Score**: 0.5789 (explains 57.89% of variance, below the 0.7 threshold).
- **Diagnosis**: Residual plots show non-random patterns, and low training/test scores indicate underfitting.

## Assumptions Tested
The model assumes:

1. Linear relationship (partially violated per scatter plot).
2. Multivariate normality.
3. No multicollinearity (not applicable with one feature).
4. No autocorrelation.
5. Homoscedasticity (violated per residual analysis).

## Future Improvements
1. Experiment with polynomial regression or other non-linear models.
2. Collect more data or additional features (e.g., marketing channels).
3. Address underfitting by increasing model complexity.

## References
- Machine Learning notes by Andrew Ng.
- Wikipedia: [Linear Regression](https://en.wikipedia.org/wiki/Linear_regression), [Simple Linear Regression](https://en.wikipedia.org/wiki/Simple_linear_regression), [OLS](https://en.wikipedia.org/wiki/Ordinary_least_squares).
