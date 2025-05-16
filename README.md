# Render_Employee_Wellness_programm
Health risk prediction model for Rende Technical Solutions Company's employee whether any employee need treatment 

Problem Statement:
Rende Technical Solutions has lost a key employee, raising serious concerns about employee health 🏥. The company wants to identify those who may need medical treatment by analyzing various attributes stored in their database 📊. By predicting health risks, organizations can take proactive steps to improve well-being and productivity 💡. Your task is to develop a model that helps detect employees in need of treatment, ensuring a healthier workforce 💼✨.

Objective: 
The goal is to help organizations understand factors affecting employee health and well-being 🏥. By building accurate predictive models 📊, companies can identify areas needing intervention and design targeted wellness programs 🏋️‍♂️. This will improve employee health and productivity 💼. The objective is to predict if an employee needs treatment based on test data 🔍.


🔍 Project Overview
This project aims to predict whether an employee is likely to seek treatment for mental health based on various demographic, workplace, and support-related attributes. The approach combines data preprocessing, exploratory data analysis, feature engineering, and the application of several classification algorithms to build a robust predictive model.

🧹 Data Preparation
The dataset was loaded and initially explored to understand its structure and missing values.
Irrelevant columns like S.No, state, comments, and leave were dropped to reduce noise.
Missing values in critical features like work_interfere, self_employed, benefits, and wellness_program were imputed using the mode of each column.
Outliers in the Age column were addressed by filtering out unrealistic values (outside the 18–60 range).
The Gender column was cleaned and standardized into three categories: Male, Female, and Transgender.
The no_employees column was ordinally encoded into no_employees_encoded to preserve hierarchy.

🛠️ Feature Engineering
The Timestamp column was processed to extract the year of the response for potential trend analysis.
Categorical variables were label-encoded for model compatibility.
New engineered features like support_score, flexibility_flag, and risk_score were tested but ultimately not retained due to limited contribution to model performance.

📊 Exploratory Data Analysis (EDA)
Distributions of numerical variables such as Age and no_employees_encoded were visualized using histograms.

![Image](https://github.com/user-attachments/assets/7f310f07-95ed-421a-921f-d244bfe6734c)

Count plots were used to explore categorical variables and their relationships with the target.

![Image](https://github.com/user-attachments/assets/a2699eff-680b-4189-9b24-2efe777e27dc)

Heatmaps and cross-tabulations helped identify associations between key variables like wellness_program, obs_consequence, and treatment.

![Image](https://github.com/user-attachments/assets/5a5bb4ae-0891-4ba5-aac8-60dc80f9a0b0)

🤖 Model Building and Evaluation
Multiple classification models were trained including:
Decision Tree
Logistic Regression
Random Forest
Gradient Boosting
K-Nearest Neighbors
Model performance was evaluated using accuracy, precision, F1-score, and detailed classification reports.

Among these, the Random Forest classifier emerged as one of the best-performing models, especially in terms of precision and overall balance.

🧠 Key Insights

Feature importance analysis revealed that Age, Family History, Care Options, Country, Number of Employees, Mental Health Consequences, and Physical Health Indicators play a significant role in predicting treatment needs.

Decision Tree:

![Image](https://github.com/user-attachments/assets/fd6e5831-f8ac-464e-ade3-5a194d17e7e7)

Random Forest:

![Image](https://github.com/user-attachments/assets/22922ec2-b69a-43ea-96d6-45f69c7154a2)

A single tree from the Random Forest was visualized to enhance model interpretability.
![Image](https://github.com/user-attachments/assets/a0e2d5ef-e4c9-48de-bcc0-81f876799304)

Predictions were saved to a CSV file for downstream business applications.
