           
              INTERN TASK PHASE 2
                  
                     TASK 2

            AUTHOR : AHSAN MAJEED

     TITTLE :  End-to-End ML Pipeline with Scikit-learn Pipeline API

  * Objective of the Task

   The main goal is to build a Production-Ready Machine Learning Pipeline that predicts Customer Churn (whether a customer will leave a service or stay). By automating this, a business can identify "at-risk" customers and take action to keep them.

  * Methodology / Approach

   The code follows a structured, professional data science workflow:


 *Data Cleaning: 
                It handles missing values in "TotalCharges" and converts the "Churn" text (Yes/No) into numbers (1/0) that the computer can understand.

 *Automated Preprocessing: 
                Using a ColumnTransformer, the code automatically handles two different types of data at once:

  *Numerical Data:
                Scaled using StandardScaler so large numbers don't overwhelm small ones.

  *Categorical Data: 
                Converted into a mathematical format using OneHotEncoder.

  *Unified Pipeline: 
                It combines preprocessing and the Random Forest model into a single Pipeline. This ensures that any new data provided to the model is cleaned and formatted exactly like the training data.

  *Hyperparameter Tuning:
                It uses GridSearchCV to automatically test different settings (like the number of trees in the forest) to find the most accurate version of the model.

  *Model Export:
               Finally, it uses joblib to save the entire process into a single file (Ahsan Ch_pipeline_model.pkl). This file can be used later in a website or app without needing to rewrite the training code.

  * Key Results or Observations

    Scientific Optimization:
                Instead of picking a model and hoping for the best, the code scientifically finds the Best Parameters to ensure high performance.

    Error Prevention:
                By using a Pipeline, the code avoids "Data Leakage" and ensures that the preprocessing steps are applied consistently during both training and testing.

    Portability:
                 The saved .pkl file is a "reusable brain." It contains everything—from the scaling logic to the final decision-making patterns—making it very easy to deploy in a real-world environment.

      High Reliability: Using 5-fold cross-validation (cv=5) means the accuracy score is reliable and not just based on a lucky split of data.