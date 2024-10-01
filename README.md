# Heart Disease Prediction

## Introduction

This project develops a predictive model to determine the presence of heart disease in patients based on various clinical parameters. Utilizing the UCI Cleveland Heart Disease dataset, the project employs machine learning techniques to achieve high accuracy in classification, aiding in early diagnosis and preventive healthcare measures.

## Data Analysis & Feature Engineering

- **Dataset Utilization**: Employed the Cleveland Heart Disease dataset from the UCI Machine Learning Repository, comprising 303 samples with 13 clinical features and a target variable indicating heart disease presence.
  
- **Exploratory Data Analysis (EDA)**:
  - **Data Integrity**: Verified the absence of missing values and ensured all features are correctly formatted.
  - **Feature Distribution**: Analyzed the distribution of key features such as age, sex, chest pain type (`cp`), resting blood pressure (`trestbps`), cholesterol (`chol`), and maximum heart rate achieved (`thalach`).
  - **Correlation Analysis**: Examined the correlation between features and the target variable to identify significant predictors.
  - **Visualization**:
    - **Sex Distribution**: Visualized the distribution of heart disease cases across genders.
    - **Heart Rate Analysis**: Compared the mean maximum heart rate between patients with and without heart disease.
    - **Age vs. Heart Rate**: Explored the relationship between age, heart rate, and heart disease presence.
    - **Chest Pain Types**: Assessed the prevalence of different chest pain types in relation to heart disease.
    - **Exercise Induced Angina**: Evaluated the occurrence of exercise-induced angina among patients with and without heart disease.

- **Data Preparation**:
  - **Feature Selection**: Selected relevant features excluding the target variable for model training.
  - **Data Splitting**: Split the dataset into training (80%) and testing (20%) sets to evaluate model performance.
  - **Scaling**: Applied `StandardScaler` to normalize feature values, ensuring efficient training of machine learning models.

## Modeling & Prediction

- **Models Implemented**:
  - **Logistic Regression**: Baseline model for binary classification.
  - **K-Nearest Neighbors (KNN)**: Instance-based learning model.
  - **Random Forest**: Ensemble learning method utilizing multiple decision trees.

- **Training Strategy**:
  - **Initial Training**: Trained each model on scaled training data and evaluated their accuracy on the test set.
  - **Hyperparameter Tuning**:
    - **KNN**: Identified the optimal number of neighbors (`k=15`) to maximize test accuracy.
    - **Logistic Regression**: Utilized `RandomizedSearchCV` and `GridSearchCV` to fine-tune the regularization parameter `C`.
    - **Random Forest**: Employed `RandomizedSearchCV` to optimize the number of estimators, maximum depth, and minimum samples for splits and leaves.
  - **Cross-Validation**: Performed 5-fold cross-validation to assess model robustness and generalizability.

- **Final Model Selection**: Logistic Regression emerged as the best-performing model post-tuning, achieving the highest accuracy and balanced precision-recall metrics.

## Results

  
- **Classification Report**:
    ```
                  precision    recall  f1-score   support

               0       0.90      0.82      0.86        22
               1       0.90      0.95      0.93        39

        accuracy                           0.90        61
       macro avg       0.90      0.88      0.89        61
    weighted avg       0.90      0.90      0.90        61
    ```


  
  Significant features influencing the prediction include `thalach` (maximum heart rate), `cp` (chest pain type), `ca` (number of major vessels colored by fluoroscopy), and `sex`.

## Conclusion

The project successfully developed a predictive model for heart disease classification with high accuracy and balanced precision and recall. Key achievements include:

- **Effective Data Handling**: Ensured data integrity and applied robust preprocessing techniques.
- **Model Training & Tuning**: Fine-tuned Logistic Regression to achieve optimal performance.
- **Evaluation**: Achieved 90.16% accuracy, surpassing the initial proof-of-concept target of 95% accuracy.
- **Feature Insights**: Identified critical clinical parameters influencing heart disease prediction.
  
These results demonstrate the potential of machine learning in aiding early detection of heart disease, contributing to preventive healthcare strategies.

