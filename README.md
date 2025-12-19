Bank Customer Churn Prediction – Data Science Learning Project

Overview:
This repository contains my hands-on work on a bank customer churn dataset, carried out as part of my data science learning and lab practice. The project focuses on understanding the complete machine learning workflow, from data exploration and preprocessing to model building, evaluation, and interpretation of results.
While I have worked on multiple datasets during my learning phase (including standard practice datasets), this repository highlights the churn dataset as a focused example to demonstrate how ML techniques are applied end to end.

Problem Statement
Customer churn occurs when customers stop using a bank’s services or close their accounts. For banks, churn management is critical because retaining existing customers is significantly more cost-effective than acquiring new ones.

The objective of this project is:
To predict whether a customer is likely to churn
To identify the key factors contributing to churn
To draw meaningful insights that can support customer retention strategies

Dataset Overview
The dataset used in this project was obtained from Kaggle (Bank Customer Churn Dataset). It contains 10,000 customer records with demographic, financial, and behavioral attributes.

Key feature categories include:
Demographic: Age, Gender, Country
Financial: Credit Score, Balance, Estimated Salary
Behavioral: Tenure, Number of Products, Active Membership, Credit Card status
Target Variable: Churn (1 = left, 0 = stayed)

Data Preparation
Initial data inspection showed no missing or duplicate values.
Preprocessing steps included:
Encoding categorical variables using label encoding and one-hot encoding
Scaling numerical features using standardization
Splitting the dataset into 80% training and 20% testing sets using stratified sampling to preserve the churn ratio (approximately 20%)

Exploratory Data Analysis (EDA)
EDA was performed to understand patterns and relationships between customer attributes and churn behavior. Key observations include:
Approximately 20% of customers had churned, indicating moderate class imbalance
Churn increased significantly with age, showing older customers are more likely to leave
Customers with higher account balances showed a higher churn tendency, suggesting dissatisfaction among premium customers
Customers with fewer products and low engagement (inactive members) churned more frequently
Correlation analysis showed churn was positively related to age and balance, and negatively related to active membership and number of products

Model Development and Evaluation
Three supervised learning models were implemented and compared:
Logistic Regression
Decision Tree
Random Forest

Performance was evaluated using accuracy, ROC-AUC, recall, precision, and F1-score.
Among the models:
Logistic Regression provided a strong baseline
Decision Tree improved recall but showed signs of overfitting
Random Forest achieved the best overall performance, with the highest accuracy and ROC-AUC, along with balanced recall and precision
Based on these results, Random Forest was selected as the final model.

Feature Importance Analysis
Feature importance from the Random Forest model revealed the most influential factors driving churn:
Age emerged as the strongest predictor
NumBer of products used had a significant impact
Account balance played an important role, particularly among high-balance customers
Engagement-related features such as active membership were more influential than purely financial indicators
These findings suggest that churn is strongly linked to customer engagement and behavior rather than income alone.

Key Conclusions
The Random Forest model achieved the best performance with 81.8% accuracy and a ROC-AUC of 0.866
Churn is primarily driven by age, product usage, balance, and engagement levels
Older customers with high balances and fewer products are more likely to churn
Improving customer engagement and offering personalized retention strategies can help reduce churn

Learning Outcome
This project helped strengthen my understanding of:
The end-to-end machine learning pipeline
How EDA guides preprocessing and model choice
The importance of interpretability alongside performance
Translating model outputs into meaningful business insights

The work reflects my continued interest in data science and applied machine learning, with an emphasis on learning through practice rather than focusing only on model metrics.

Tools and Technologies Used
Python
Pandas, NumPy
Scikit-learn
Matplotlib, Seaborn
Jupyter Notebook
