# stock-analysis-machine-learning-stock-prediction
This project uses machine learning to predict stock prices using Apple Stock data (1980-2024). It includes EDA, multicollinearity assessment, data visualization, model training, and evaluation. Models like Linear Regression, Random Forest, KNN, and SVM were trained, with Linear Regression performing best and tested for overfitting.
# Machine Learning Stock Prediction

## Overview
This project demonstrates the application of machine learning models to predict Apple stock prices using historical data. The dataset consists of daily stock prices (Open, High, Low, Close) from 1980 to 2024. It covers 11,094 days of stock price history. The project includes data preprocessing, exploratory data analysis (EDA), visualization, model training, and performance evaluation.

## Data
The dataset used is the Kaggle **Apple Stock Market Historical Data (1980-2024)**, which contains the following columns:
- **Open**: Opening stock price
- **High**: Highest stock price during the day
- **Low**: Lowest stock price during the day
- **Close**: Closing stock price

### Data Preprocessing
- Checked for missing, duplicated, and null values (none were found).
- Performed **descriptive statistics** and **exploratory data analysis (EDA)** to understand the dataset better.
- Assessed **multicollinearity** using Variance Inflation Factor (VIF), revealing that the **High** column had the highest correlation with the target variable (Closing stock price).

## Visualizations
Several visualizations were created to analyze stock price behavior:
- Line plot of **Closing Price** over time.
- High vs Low stock prices per day.
- 30-day and 90-day **Moving Averages**.
- Bar plot of **Daily Price Range**.
- Daily **Percentage Change** in Closing Price.
- 30-day **Rolling Volatility** and **Drawdowns**.
- Visualizations for years of **high volatility** (1999) and **big drawdowns** (2000-2003) caused by the dot-com bubble burst.

### Insights
- In **1999**, the stock price rose significantly due to Apple's introduction of the iMac.
- Between **2000-2003**, the stock price faced a major drop due to the dot-com bubble burst, especially in **September 2000** and **October 2000**.

## Model Training & Evaluation
The following models were trained using the dataset:

### With Scaled Data:
- **Linear Regression**: Best performance with a correlation of **0.99996**.
- **Random Forest**: Correlation of **0.99991**.
- **KNN**: Correlation of **0.99991**.
- **SVM**: Correlation of **0.99253**.

### Without Scaled Data:
- **Linear Regression**: Correlation of **0.99996**.
- **KNN**: Correlation of **0.99993**.
- **SVM**: Correlation of **0.99521**.
- **Random Forest**: Correlation of **0.99993**.

### Hyperparameter Tuning:
- Used **Grid Search** for Random Forest to fine-tune the model and found a slight improvement in performance with a correlation of **0.99992**.

### Overfitting Test:
- The trained models were tested on a **new dataset** to check for overfitting. The **Linear Regression** model performed best with a correlation of **0.99968** on the new data.

## Conclusion
The project demonstrates the process of preparing financial data, analyzing patterns, and training machine learning models to predict stock prices. The models were evaluated, and it was observed that Linear Regression performed the best overall. The project also emphasizes the importance of assessing overfitting and testing models on new datasets.

## Future Work
-Experiment with other machine learning algorithms (e.g., LSTM, ARIMA) for better stock prediction.
-Explore feature engineering to improve model performance.
## Acknowledgments
Datasets: Kaggle Apple Stock Market Historical Data (1980-2024) and Kaggle Tesla Stock Price With Indicators (10 Years)
Libraries: scikit-learn, pandas, matplotlib, seaborn, numpy
