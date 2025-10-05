OVERVIEW

This project demonstrates the use of Logistic Regression for classification tasks using the popular Seaborn “Tips” dataset.
The goal is to predict whether the meal was Lunch (0) or Dinner (1) based on various customer and order-related features.

🎯 OBJECTIVE

The main objective is to:

Understand how categorical and numerical data can be preprocessed for machine learning models.

Apply Logistic Regression to a real-world dataset.

Use GridSearchCV to optimize hyperparameters for the best model performance.

🧩 DATASET DESCRIPTION

The Tips dataset contains data about restaurant bills and tips, including:

Feature	Description
total_bill	Total bill amount (in dollars)
tip	Tip given by the customer
sex	Gender of the customer
smoker	Whether the customer is a smoker or not
day	Day of the week
time	Time of meal — Lunch or Dinner (our target variable)
size	Number of people at the table
🧮 Steps Performed
1️⃣ Data Loading and Exploration

Loaded the tips dataset from Seaborn.

Checked for null values and unique values in each column.

Ensured data cleanliness.

2️⃣ Encoding Categorical Data

The target column ‘time’ was converted into binary form:

Lunch → 0

Dinner → 1

Other categorical features (sex, smoker, day) were transformed using OneHotEncoding to make them suitable for the model.

3️⃣ Splitting the Data

The data was split into training (75%) and testing (25%) sets using train_test_split.

4️⃣ Model Building

Implemented Logistic Regression, which predicts binary outcomes (0 or 1) using a sigmoid activation over a linear equation.

5️⃣ Hyperparameter Tuning (GridSearchCV)

Performed a parameter search to find the best combination of:

penalty → ['l1', 'l2', 'elasticnet']

C → Regularization strength (1, 2, 3, 4, 5, 10, etc.)

max_iter → Iterations (100, 200, 300)

The best model used L2 regularization, C = 2, and max_iter = 100.

6️⃣ Model Evaluation

Evaluated the model using:

Accuracy Score

Classification Report (Precision, Recall, F1-Score)

Confusion Matrix Visualization

Achieved around 98% accuracy, indicating excellent classification performance.

7️⃣ Data Visualization

Heatmap: Showed correlations among numerical features.

Pairplot: Displayed feature distributions based on meal time (Lunch/Dinner).

📈 Key Learnings

Logistic Regression is ideal for binary classification problems.

OneHotEncoding is essential to handle categorical variables before training.

GridSearchCV helps in selecting the most optimal parameters.

The Tips dataset effectively demonstrates data preprocessing, model fitting, and performance evaluation in a single workflow.

🧠 Conclusion

This project showcases how a simple yet powerful algorithm like Logistic Regression can effectively classify real-world data after proper preprocessing and hyperparameter tuning.
With 98% accuracy, the model successfully predicts whether a meal was Lunch or Dinner based on customer and bill details.
