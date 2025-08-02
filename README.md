# 🧠 Predicting Alzheimer's Disease with Supervised Machine Learning

This project demonstrates an end-to-end machine learning workflow to predict the diagnosis of Alzheimer's disease based on a comprehensive clinical dataset. The notebook covers everything from data exploration and preprocessing to training and evaluating 10 different supervised classification models.

## 📌 Project Overview
The primary goal of this project is to identify the most effective supervised learning model for classifying Alzheimer's disease. By analyzing various patient attributes—including demographic, lifestyle, and clinical data—we aim to build a robust predictive tool that can aid in early and accurate diagnosis.

## 💾 Dataset
The dataset used is `alzheimers_disease_data.csv`, which contains:

- 2,149 patient records  
- 34 predictive features, such as Age, BMI, Blood Pressure, and MMSE score  
- Target Variable: `Diagnosis` (0 for Cognitively Normal, 1 for Alzheimer's)  
- No missing values or duplicates

## ⚙️ Project Workflow
The project follows a structured machine learning pipeline:

1. **Data Loading & Inspection**: Initial examination of the dataset's structure and quality  
2. **Exploratory Data Analysis (EDA)**: In-depth analysis of feature distributions, correlations, and class balance  
3. **Data Preprocessing**:  
   - Dropping non-predictive columns (`PatientID`, `DoctorInCharge`)  
   - Splitting the data into 80% training and 20% testing sets  
   - Scaling numerical features using `StandardScaler`  
4. **Model Training & Evaluation**: Iteratively training and evaluating 10 different classification models  
5. **Model Comparison**: Compiling performance metrics (F1-Score, Accuracy) to identify the best-performing model  

## 📊 Key Findings from EDA
- The dataset is balanced (near 50/50 class split)  
- MMSE score and Age are the strongest individual predictors  
- Family history is also strongly correlated with diagnosis  

## 🤖 Models Trained
10 supervised models were trained and compared:

- Logistic Regression  
- Support Vector Machine (SVM)  
- K-Nearest Neighbors (KNN)  
- Decision Tree  
- Random Forest  
- AdaBoost  
- Gaussian Naive Bayes  
- XGBoost  
- Bagging Classifier  
- Stacking Classifier  

## 🏆 Performance Results

| Model              | F1-Score (%) | Accuracy (%) |
|--------------------|--------------|--------------|
| XGBoost            | 92.62        | 94.88        |
| Random Forest      | 92.26        | 94.65        |
| Stacking Classifier| 91.75        | 94.19        |
| Bagging Classifier | 90.34        | 93.49        |

**XGBoost** emerged as the top-performing model, showcasing the effectiveness of ensemble methods.

## 🏁 Conclusion and Future Work
This project confirms that machine learning models—particularly XGBoost—can effectively predict Alzheimer's disease from structured clinical data.

### Next Steps:
- **Hyperparameter Tuning**: Use `GridSearchCV` to improve model performance  
- **Feature Importance**: Analyze top contributing features for clinical insight  
- **Deployment**: Develop a simple web app for real-time predictions
