# Traffic Severity Prediction
This project aims to predict the severity of traffic incidents based on environmental, temporal, and geographical features using a Random Forest classifier. The dataset has been preprocessed to optimize model performance and includes a carefully selected set of features.

How to Run the Python Script
Prerequisites
Ensure you have Python 3.7 or later installed along with the following libraries:

pandas
numpy
scikit-learn
matplotlib
seaborn

Project Approach
1. Dataset Overview
The dataset contains details about traffic incidents, such as location, environmental factors, and time-based features.

2. Data Preprocessing
Feature Selection:
Final features used include:

Source
Severity (target variable)
Start_Lat, Start_Lng (latitude and longitude)
Distance(mi)
Timezone
Pressure(in), Wind_Speed(mph)
Sunrise_Sunset (day or night)
Temp_Bin (binned temperature values)
Hour, Day_of_Week, Month
Duration
Weather_Group
Reason for Using Latitude and Longitude:
Latitude and longitude provide precise spatial patterns without the high cardinality issues associated with street and zipcode, which have over 200,000 and 400,000 unique values, respectively.

Outlier Removal:
Detected and removed 920,514 outliers using the Z-score and IQR methods to reduce noise and improve model performance.

Encoding Categorical Variables:
Used one-hot encoding for categorical features like Source, Timezone, and Weather_Group.

3. Model Training
Algorithm: Random Forest classifier.
Performance Metrics:
Accuracy: 84.5%
Macro F1-Score: 0.25 (struggles with minority classes).
# 4. Results
High accuracy for the majority class (Severity 2).
Lower precision and recall for minority classes (Severities 1, 3, and 4).
# Future Work
Handle Class Imbalance:
Apply SMOTE or oversampling to balance the dataset.
Hyperparameter Tuning:
Fine-tune Random Forest parameters using Grid Search or Random Search.
Explore Advanced Models:
Test XGBoost, LightGBM, or CatBoost for improved performance.
Feature Engineering:
Incorporate spatial clustering (e.g., DBSCAN) on latitude and longitude.
Improved Metrics:
Evaluate with ROC-AUC for better insights into imbalanced data performance.
