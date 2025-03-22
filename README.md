# README: Machine Learning for Room Occupancy Estimation

**Overview**

This project focuses on estimating room occupancy using data collected from non-intrusive sensors. The goal is to optimize resource utilization, improve energy efficiency, and enhance user experience in smart buildings. The project employs machine learning techniques to predict room occupancy based on sensor data, including temperature, light, sound, CO2 levels, and passive infrared (PIR) readings.

------
**Key Objectives**

-Predict Room Occupancy: Use sensor data to estimate the number of occupants in a room.

-Optimize Resource Utilization: Enable real-time adjustments to lighting, HVAC systems, and security protocols based on occupancy.

-Improve Energy Efficiency: Reduce energy consumption by ensuring resources are only used when needed.

-Enhance User Experience: Provide a comfortable and secure environment for occupants.

--------
**Dataset**

The dataset used in this project was collected from a controlled environment over four days. It includes 10,129 instances and 18 features, such as:

- Sensor Readings: Temperature, light, sound, CO2 levels, and PIR readings from multiple sensors.

- Target Variable: Room_Occupancy_Count, which indicates the exact number of occupants in the room.
-----------
**Dataset Features:**

Date and Time: Timestamps for each reading.

Temperature (S1-S4): Temperature readings from four sensors.

Light (S1-S4): Light intensity readings from four sensors.

Sound (S1-S4): Sound level readings from four sensors.

CO2 (S5): CO2 concentration readings.

CO2 Slope: Rate of change in CO2 levels.

PIR (S6-S7): Passive infrared sensor readings.

Room_Occupancy_Count: The target variable indicating the number of occupants.

----------------
**Methodology**

The project follows a structured approach to develop and evaluate machine learning models for occupancy estimation:

Exploratory Data Analysis (EDA): Analyze the dataset to understand the relationships between features and the target variable.

----------------------
**Data Preprocessing:**

- Handle missing data.

- Use Synthetic Minority Over-sampling Technique (SMOTE) to address class imbalance in the target variable.
  
------------------
**Model Selection:**

-Random Forest

-Support Vector Machine (SVM)

-Gradient Boosting

-XGBoost

--------------------
**Model Training and Evaluation:**

- Use k-fold cross-validation to ensure robust model evaluation.

- Optimize hyperparameters using GridSearchCV.
---------------------
**Performance Metrics:** Evaluate models using accuracy, precision, recall, and F1-score.
----------------------
**Machine Learning Models**
The following models were evaluated for occupancy estimation:

**1. Random Forest**

Strengths: Handles multiple features, reduces overfitting, and captures complex relationships.

**Performance:**

Before Balancing: Accuracy: 99.90%, Precision: 99.90%, Recall: 99.90%, F1 Score: 99.91%

After Balancing: Accuracy: 99.85%, Precision: 99.85%, Recall: 99.85%, F1 Score: 99.85%

Best Parameters: {'max_depth': 10, 'min_samples_split': 2, 'n_estimators': 200}

**2. Support Vector Machine (SVM)**
Strengths: Effective in high-dimensional spaces and captures complex relationships.

Performance:

Before Balancing: Accuracy: 99.26%, Precision: 99.27%, Recall: 99.26%, F1 Score: 99.26%

After Balancing: Accuracy: 99.26%, Precision: 99.27%, Recall: 99.26%, F1 Score: 99.26%

Best Parameters: {'C': 1, 'kernel': 'rbf'}

**3. Gradient Boosting**
Strengths: Combines weak learners to create a strong model, effective for imbalanced datasets.

Performance:

Before Balancing: Accuracy: 99.56%, Precision: 99.55%, Recall: 99.56%, F1 Score: 99.56%

After Balancing: Accuracy: 99.55%, Precision: 99.54%, Recall: 99.55%, F1 Score: 99.55%

Best Parameters: {'learning_rate': 0.2, 'n_estimators': 50}

**4. XGBoost**

Strengths: Efficient, handles missing data, and performs well on imbalanced datasets.

Performance:

Before Balancing: Accuracy: 99.70%, Precision: 99.70%, Recall: 99.70%, F1 Score: 99.70%

After Balancing: Accuracy: 99.70%, Precision: 99.70%, Recall: 99.70%, F1 Score: 99.70%

Best Parameters: {'learning_rate': 0.2, 'n_estimators': 200}
-------------------------------------------
**Results and Discussion**
- Model Performance: All models achieved high accuracy, precision, recall, and F1-scores, indicating strong performance in predicting room occupancy.

- Balancing Impact: SMOTE was used to address class imbalance, but the performance metrics remained stable, suggesting that the models were not significantly affected by class imbalance.

- Best Model: Random Forest performed the best, with the highest accuracy and stable performance across all metrics.
 
- Reliability: The models showed no signs of overfitting or underfitting, and the results were consistent across training and test datasets.
---------------------------------------------
**Limitations**
Hyperparameter Sensitivity: All models are sensitive to hyperparameter choices, requiring careful tuning.

Interpretability: Models like Random Forest, Gradient Boosting, and XGBoost are less interpretable compared to simpler models.

Computational Resources: SVM and ensemble methods can be computationally expensive, especially for large datasets.

Overfitting Risk: Gradient Boosting and XGBoost are prone to overfitting if not properly tuned.

**Conclusion**
This project successfully applied machine learning techniques to estimate room occupancy using sensor data. Random Forest emerged as the best-performing model, with high accuracy and reliability. The results demonstrate the potential of machine learning in optimizing resource utilization and improving energy efficiency in smart buildings. Future work will focus on advanced tuning techniques and real-time model monitoring to further enhance performance.
