# MRI Slot No-Show Prediction
This project predicts patient no-shows for MRI appointments using machine learning.  
It combines the public Kaggle "No-show Appointments" dataset with **synthetic healthcare scheduling data** to simulate real hospital scheduling operations.

## Objectives
- Analyze appointment and patient patterns contributing to no-shows  
- Predict which appointments are at high risk of being missed  
- Provide actionable insights for schedulers and hospital administrators  
- Support integration with an MRI slot-management app

### Problem Addressed
Missed appointments cost hospitals both time and resources. By predicting potential no-shows, facilities can:
- Reallocate MRI slots efficiently  
- Reduce idle machine time  
- Improve patient access and care coordination  
  
## Dataset
- **Source**: [Kaggle No-show Appointments Dataset](https://www.kaggle.com/datasets/joniarroba/noshowappointments)
- **Synthetic Features Added**:
  - `Medical_Transport` (Yes/No)
  - `Reminder_Channel` (SMS, Phone,Email, None)
  - `Pt_confirmed` (Yes/No)
  - `First_Visit` (Yes/No)
  - `Appointment_Day` and `WaitingDays`

## Exploratory Data Analysis (EDA)
- Distribution of no-shows by age, gender, reminder channel, waiting days, Medical_Transport, Appointment_Day, Pt_confirmed
- Chi-square tests for feature significance
- Correlation heatmaps and feature selection

## Predictive Modelling
Models tested:
- Logistic Regression  
- Random Forest  
- XGBoost  

**Handling Class Imbalance**: SMOTE applied to balance show/no-show cases.

Confusion matrices and performance plots available in the `/images` folder.

## Business Impact
Predictive insights can help clinic/hospitals:
- Identify high-risk patients
- Send targeted reminders
- Improve machine utilization and reduce missed MRI slots

## Future Scope
- Integrate model output into Power Apps MRI Scheduling Tool
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
