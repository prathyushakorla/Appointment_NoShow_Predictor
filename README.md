**Appointment No-Show Predictor**

Predicting patient no-shows to optimize appointment scheduling and interventions using machine learning.

**Project Overview**

This project predicts the likelihood of patients missing their scheduled appointments using historical appointment data, patient demographics, and weather information. The goal is to enable healthcare providers to reduce missed appointments through targeted reminders and optimized scheduling.

Key features:

Predicts No-Show Risk Probability for each appointment.

Classifies patients into Low, Medium, High, or Critical risk categories.

Recommends intervention strategies (SMS, phone reminders, follow-ups) based on risk factors.

Identifies optimal scheduling characteristics for high attendance.

Generates a summary dashboard for decision support.



**Dataset**

Appointments Data: KaggleV2-May-2016.csv (patient appointments, demographics, no-show status)

Weather Data: DailyClimateTrain.csv & DailyClimateTest.csv (temperature, humidity, wind, pressure)



**Methodology**

Data Loading & Exploration: Load datasets, check distributions, visualize No-Show patterns.

Data Preprocessing: Clean column names, handle missing values, clip ages, convert target to numeric.

**Feature Engineering:**

Temporal features (days until appointment, day of week, month, season, weekend indicator)

Demographics & comorbidity index

Weather merge for appointment day

Appointment type and age group

Feature Encoding: Label encoding for categorical features, encoding gender and neighborhood.

**Modeling:**

Random Forest

Gradient Boosting

Logistic Regression

Evaluation Metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC, feature importance.

Risk Stratification: Assign Low, Medium, High, Critical risk categories.

Intervention Recommendations: SMS reminders, phone calls, follow-ups, special care for high-risk patients.

Scheduling Optimization: Identify best days, months, and scheduling windows for maximum attendance.

Dashboard & Summary: Save predictions with risk probabilities and recommended interventions.




**Usage**

Open Appointment_NoShow_Predictor.py in Jupyter/Colab.

Run cells sequentially.

Output includes:

Feature importance plots

ROC curves

Risk stratification visualizations

Top 10 high-risk appointments for intervention

Final summary saved as Final_NoShow_Summary.csv.


<img width="1173" height="320" alt="image" src="https://github.com/user-attachments/assets/0d4af0f1-b3fa-4258-a87a-1f2dc847c709" />





**Key Insights**

Random Forest and Gradient Boosting performed best for this dataset.

Age, days until appointment, comorbidity index, and prior SMS reminders are significant predictors.

Targeted interventions can potentially reduce no-show rates significantly.




