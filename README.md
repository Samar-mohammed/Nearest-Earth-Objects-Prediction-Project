# Nearest-Earth-Objects-Prediction-Project


## Overview  
This project leverages machine learning to analyze and predict hazardous near-Earth objects (NEOs) based on their characteristics. The dataset spans over a century (1910–2024) and includes features such as absolute magnitude, estimated diameter, relative velocity, and miss distance.

---

## Dataset: Nearest Earth Objects (1910-2024)  
The dataset contains information about asteroids and other objects near Earth for over 100 years. It includes **338,199 rows × 9 columns** and is available at the following link:  
[Kaggle: NASA Nearest Earth Objects (1910-2024)](https://www.kaggle.com/datasets/ivansher/nasa-nearest-earth-objects-1910-2024/data)  

---

## Objective  
To classify near-Earth objects as **hazardous** or **non-hazardous** using machine learning models.

---

## Data Preprocessing  

### 1. Outlier Handling  
- Removed outliers using the **Interquartile Range (IQR)** method.  
- Applied **log transformations** to normalize `estimated_diameter_min`, `estimated_diameter_max`, and `relative_velocity`.  
- Used **Winsorization** and **robust Z-score capping** to handle extreme outliers.  

### 2. Data Cleaning  
- Removed missing values and duplicate rows to ensure data quality.  

### 3. Class Balancing  
- Used **SMOTE (Synthetic Minority Oversampling Technique)** to balance the target variable (`is_hazardous`), ensuring equal representation of hazardous and non-hazardous classes.

---

## Model Evaluation  
The following machine learning classifiers were compared:  
- **Logistic Regression**  
- **Decision Tree**  
- **Random Forest**  
- **Gradient Boosting**  

### Performance Metrics  
The models were evaluated using the following metrics:  
- Accuracy  
- Precision  
- Recall  
- F1-Score  
- AUC-ROC  

---

## Results  

### Best Model: Gradient Boosting  
Gradient Boosting achieved the best balance between training and testing metrics, avoiding overfitting.  

#### Performance Metrics:
| Metric              | Train Value | Test Value |  
|---------------------|-------------|------------|  
| **Accuracy**        | 0.8866      | 0.8866     |  
| **Precision**       | 0.8235      | 0.8239     |  
| **Recall**          | 0.9841      | 0.9836     |  
| **F1-Score**        | 0.8967      | 0.8967     |  
| **AUC-ROC**         | 0.9494      | 0.9489     |  

---

## Predictions  
The project includes a clear mechanism to test the model on new data and classify whether a NEO is hazardous or not.  

---

