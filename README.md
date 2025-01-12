##  Traffic Severity Prediction
This project leverages a machine learning approach to predict the severity of traffic incidents based on environmental, temporal, and geographical features. The model is built using a Random Forest classifier and achieves 84.5% accuracy.

# Table of Contents
Features  
Dataset  
Approach  
Results  
Future Improvements  

# Features
Predicts traffic incident severity (1 to 4).  
Processes large datasets with efficient feature selection and encoding.  
Handles class imbalance and outliers for better model performance.  
Implements Random Forest for robust and interpretable results.  

# Dataset
The dataset includes various features related to traffic incidents:  

Spatial Data: Start_Lat, Start_Lng  
Environmental Data: Wind_Speed, Pressure, Weather_Group  
Temporal Data: Hour, Day_of_Week, Month  
Other Features: Distance(mi), Sunrise_Sunset, Duration, Temp_Bin  
Why Latitude and Longitude Instead of Street and Zipcode?  
Latitude and Longitude provide precise spatial information.  
Street and Zipcode have high cardinality (200,000+ unique values for Street, 400,000+ for Zipcode), which increases computational complexity without significant predictive value.  

# Approach
Feature Engineering:  

Extracted time-based features (Hour, Day_of_Week, Month) from timestamps.  
Binned temperature into discrete categories (Temp_Bin).  
Simplified weather conditions into grouped categories (Weather_Group).  
Outlier Detection and Removal:  

Removed 920,514 outliers using Z-score and IQR methods.  
Categorical Encoding:  

Used one-hot encoding for features like Source, Timezone, and Weather_Group.  
Model Training:  

# Algorithm: Random Forest Classifier.  
Achieved an accuracy of 84.5%.  

![image](https://github.com/user-attachments/assets/aa493865-f057-4b87-9fff-6b79e4845a9e)
