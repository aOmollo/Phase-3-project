# Phase-3-project  
SyriaTel Customer Churn Project   
# Business Understanding  

#### Background and Overview  
The project involves the development of a predictive model for customer churn using the available dataset, aiming to identify customers at risk of leaving the service. This project directly concerns stakeholders such as the marketing and sales teams, customer service departments, and upper management, with the potential to significantly impact customer retention and overall profitability. While the primary data source is the provided customer dataset, the project's scope encompasses the development and validation of the predictive model, along with the identification of key features influencing churn. Stakeholders' understanding and alignment regarding the project's objectives, scope, and expected outcomes are crucial, as clear communication is vital to ensure a unified understanding across different parts of the organization.  

**Business problem**   
SyriaTel, a leading telecommunications company, is facing challenges with customer churn, where customers discontinue their services with the company. Customer churn not only results in revenue loss but also impacts the company's reputation and market competitiveness. To mitigate this issue, SyriaTel aims to identify predictive patterns and develop a robust classifier to forecast whether a customer is likely to churn in the near future.  

**Objectives**    
This project aims:  
1.	To develop a binary classification, model that forecasts if a client will "soon" terminate their relationship with SyriaTel.    
2.	To determine what factors influence customer churn  
3.	To determine the best model for predicting customer churn  
4.	To evaluate how insights from feature importance can help improve customer churn
   
**Significance**   
By accurately identifying customers at risk of churn, the company can proactively implement retention strategies to mitigate churn and enhance customer loyalty.    

**Research Questions**   
The project aims at answering the following questions:   
•	What were the factors influencing customer churn?   
•	What is the best model for predicting customer churn?   
•	How can the insights from feature importance help improve customer churn? 

**Data Understanding**  
The data is from Syrian Tel Communication company retrieved from Kaggle (link: https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset/data). The structure of the data included 21 columns and 3333 rows. The columns detail the different kinds of attributes (refer to the summary section below) while the rows represent customers recorded in the dataset. The dataset contains continuous and categorical variables. The target variable used is churn and the rest of the variables served as predictors except for state and phone number.   

Here's a brief summary of each column:    
**State**: Customer's state.   
**Account Length**: Duration of the customer's account.   
**Area Code**: Telephone area code.   
**Phone Number**: Unique phone number.   
**International Plan**: Whether the customer has an international calling plan.   
**Voice Mail Plan**: Whether the customer has a voicemail plan.   
**Number Vmail Messages**: Number of voicemail messages.   
**Total Day Minutes/Calls/Charge**: Total daytime call duration, count, and charges.   
**Total Eve Minutes/Calls/Charge**: Total evening  

**Data Preparation**  
During this stage:   
i.	The data is observed to have no missing values and duplicates.  
ii.	Categorical data was transformed to numerical data with label encoder.  
iii.	Normalizing numeric data using Min-Max Scaler.  

**Modelling**   
**Modelling considerations:**   
1. Task Type: This project involves classification to predict customer churn.     
2. Models: We'll experiment with logistic regression, decision trees, random forests, and gradient boosting.   
3.Class Imbalance Management: We'll address overfitting using SMOTE and hyper parameter tuning.   
4. Regularization: We'll use regularization techniques like L1 or L2 regularization to prevent overfitting.   
5. Validation: We'll employ k-fold cross-validation to ensure our models generalize well.   
6. Loss Functions: We'll use entropy loss and gini for model training.   
7. Performance Threshold: Success will be determined by achieving predefined performance metrics thresholds. These considerations guide our model selection, training, and evaluation process, ensuring effective churn prediction.  

**Evaluation**  
The metrics used to evaluate models:    
a.	Accuracy score  
b.	Area under curve (auc)
Best model is selected best on high performance .   

**Findings of EDA**  
**Feature Importance**  
Feature importance analysis helps identify which features have the most influence on predicting churn. By knowing which factors contribute the most to churn, the company can prioritize them in its retention strategies and focus resources on addressing those factors effectively.   

![image](https://github.com/aOmollo/Phase-3-project/assets/146751854/130fe68f-3cc3-4a44-ba3b-0a678475a1f0)

The top five most important features that determine customer churn include:  
a.	Customer service charge  
b.	Total day minutes   
c.	Total day charge   
d.	Voice mail plan  
e.	Area code   

**Graph of Churn against Area code**  
![image](https://github.com/aOmollo/Phase-3-project/assets/146751854/7bece882-a63b-4f86-be2a-b8837222b4a0)  

**Graph of Churn against Customer Service Calls**   
![image](https://github.com/aOmollo/Phase-3-project/assets/146751854/3c5da096-addc-4c54-82d7-4b46404567b1)  

**Graph of Churn against Voice Mail Plan**   
**Models’ Results**   
<img width="278" alt="Capture" src="https://github.com/aOmollo/Phase-3-project/assets/146751854/5094130f-0fac-4dc0-bd73-1ece94070ec2">   
![image](https://github.com/aOmollo/Phase-3-project/assets/146751854/248fef04-8c23-4946-b08a-78b1e2675208)    

The best model is gradient boosting classifier with an accuracy score of 0.9100 for test and 0.9098 for training. This model tends to be more robust to overfitting compared to other models. This model demonstrates good generalization ability.    

**Visualization of ROC Curve of Gradient Boosting Classifier.**  









