# Radiology Imaging Slot No-Show Prediction
This project predicts patient no-shows for  Imaging appointments using machine learning.  
It combines the public Kaggle "No-show Appointments" dataset with **synthetic healthcare scheduling data** to simulate real hospital scheduling operations.

## Objectives
- Analyze appointment and patient patterns contributing to no-shows  
- Predict which appointments are at high risk of being missed  
- Provide actionable insights for schedulers and hospital administrators  
- Support integration with an Scheduling slot-management app

### Problem Addressed
Missed appointments cost hospitals both time and resources. By predicting potential no-shows, facilities can:
- Reallocate slots efficiently  
- Reduce idle machine time  
- Improve patient access and care coordination  
  
## Dataset
- **Source**: [Kaggle No-show Appointments Dataset](https://www.kaggle.com/datasets/joniarroba/noshowappointments)
- **Synthetic Features Added**:
  - `Medical_Transport` (Yes/No)
  - `Appointment_Day
  - `WaitingDays`
  - `Visit_Count`
  - `Past_Noshow_count`

## Exploratory Data Analysis (EDA)
- Distribution of no-shows by age, gender, waiting days, Medical_Transport, Appointment_Day and more
- Chi-square tests for feature significance
- Correlation heatmaps and feature selection

## Predictive Modelling
Models tested:
- Logistic Regression  
- Random Forest  
- XGBoost  

**Handling Class Imbalance**: SMOTE applied to balance show/no-show cases.

Confusion matrices and performance plots available in the `/images` folder.
## Model Comparison (No Show class @ Best thresholds)

| Model               | Recall | Precision | F1   |
|---------------------|--------|-----------|------|
|Logistic Regression | 0.65  | 0.31      | 0.42 | 
|Logistic Regression (Smote) | 0.60   | 0.26      | 0.37 | 
| Random Forest       | 0.74   | 0.28      | 0.41 | 
| XGBoost (final)     | 0.87   | 0.30      | 0.44 | 

![Confusion Matrix](Images/XGBoost_Smote_CM.png)

<p align="center">
  <b>Confusion Matrix from XGBoost Model</b>
</p>

## Business Impact
Predictive insights can help clinic/hospitals:
- Identify high-risk patients
- Send targeted reminders
- Improve machine utilization and reduce missed idle slots

## Future Scope
- Integrate model output into Power Apps Imaging Scheduling Tool
- Add real-time prediction dashboard in Power BI

## Credits and Acknowledgments
- Original dataset by Joni Arroba on Kaggle **(https://www.kaggle.com/datasets/joniarroba/noshowappointments)**
- Synthetic data creation, analysis, and modelling by **Prashasti Hajela**
- Tools used: Jupyter Notebook, Anaconda, Python, Pandas, NumPy,Matplotlib, Seaborn, Scikit-learn, XGBoost, Imbalanced-learn

## Contact Information
For questions, suggestions, or collaboration:
- Author: Prashasti Hajela
- Email: prashastihajela95@gmail.com
- LinkedIn: https://www.linkedin.com/in/prashasti-h-73bb4b137/
