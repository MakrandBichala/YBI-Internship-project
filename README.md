# YBI-Internship-project
NBA ML Model (Linear Regression)

** NBA Salary Prediction using Multiple Linear Regression
Project Overview**
This project builds a Multiple Linear Regression model using Python to predict the salaries of NBA players based on their age, height, and weight. The dataset is processed and used to train a regression model capable of estimating player salary from user inputs or batch data.

**Problem Statement**
Predict the salary of an NBA player using simple measurable features:
Age
Height (converted from feet-inches to inches)
Weight

**Dataset**
Source: YBI Foundation - NBA Dataset
Features Used:
Age — Player's age in years
Height — Player's height in feet-inches (converted to inches)
Weight — Player's weight in pounds
Salary — Player's annual salary in USD (target)

**Tools & Libraries**
Python (via Google Colab)
pandas, numpy
scikit-learn — for model training and evaluation
matplotlib, seaborn — for optional visualizations

**Workflow**
1. Data Cleaning
Dropped missing values
Converted height from '6-5' format to inches using a custom function

2. Feature Selection
X = df[['Age', 'Height', 'Weight']]
y = df['Salary']

4. Model Training
Used LinearRegression() from scikit-learn:
model = LinearRegression()
model.fit(X_train, y_train)

6. Evaluation Metrics
R² Score
Mean Squared Error (MSE):
print("R² Score:", r2_score(y_test, y_pred))
print("MSE:", mean_squared_error(y_test, y_pred))

🧪 Prediction Example
Manual input simulation in Colab:
age = 25
feet = 6
inches = 5
weight = 210
height = feet * 12 + inches
input_df = pd.DataFrame([[age, height, weight]], columns=['Age', 'Height', 'Weight'])
salary_pred = model.predict(input_df)[0]

print(f"Predicted Salary: ${salary_pred:,.2f}")
✅ Output
The model returns a salary estimate (in USD) based on the player’s input features:
Predicted Salary: $4,358,201.84
