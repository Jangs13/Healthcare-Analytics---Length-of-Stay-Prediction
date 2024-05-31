# Healthcare Analytics - Length of Stay Prediction

## Introduction
Healthcare organizations are under increasing pressure to improve patient care outcomes and achieve better care. This project leverages healthcare analytics to predict the Length of Stay (LOS) for patients. By analyzing data using quantitative and qualitative techniques, we aim to provide insights that can help hospitals optimize treatment plans and reduce infection rates, thereby improving overall patient care.

## Project Goal
The primary goal of this project is to accurately predict the Length of Stay for each patient to help hospitals optimize their resources and improve operational efficiency.

## Hypothesis Generation
We assume that various factors impact the Length of Stay (LOS). These factors are categorized into two levels:

## Patient-Level Factors
- Type of Admission: Urgent, Emergency, and Trauma levels, where Trauma patients tend to stay longer.
- Severity of Illness: Classified as Minor, Moderate, and Extreme, with more severe illnesses resulting in longer stays.
- Visitors with Patient: More visitors can lead to longer stays.
- Age: Infants and older patients typically have longer recovery times.
- Admission Deposit: Higher deposits may indicate more severe conditions and longer stays.
- Hospital-Level Factors
- Ward Type: ICU patients usually stay longer than those in general wards.
- Department: Patients in surgery departments often have longer recovery times compared to other departments like gynecology.
- Data Exploration
- The dataset comprises 318,438 observations and 17 variables, with the target variable "Stay" divided into 11 classes ranging from 0 to over 100 days. Key variables include case_id, Hospital_code, Type of Admission, Severity of Illness, Visitors with Patient, Age, and Admission_Deposit.

## Data Cleaning and Preparation
Missing values in the "City_code_patient" and "Bed Grade" variables were imputed using the mode. Ordinal data was transformed using label encoding for further analysis.

## Feature Engineering
We created new features such as "count_id_patient," "count_id_patient_hospitalCode," and "count_id_patient_wardfacilityCode" to capture the count of multiple admissions for patients in different contexts.

## Modelling Strategy
Model 1: Naïve Bayes
A Gaussian Naïve Bayes classifier was used, achieving an accuracy of 34.55%.
![Naive bayes](https://github.com/Jangs13/Healthcare-Analytics---Length-of-Stay-Prediction/blob/master/images/naive%20bayes.png)

## Model 2: XGBoost
An XGBoost classifier with tuned parameters was employed, achieving an accuracy of 43.04%.
![XGBoost](https://github.com/Jangs13/Healthcare-Analytics---Length-of-Stay-Prediction/blob/master/images/XGboost.png)

## Model 3: Neural Networks
A neural network with six dense layers and a SoftMax output layer was used. Despite being theoretically better, it achieved an accuracy of 42.19% due to the smaller dataset.
![Neural Network](https://github.com/Jangs13/Healthcare-Analytics---Length-of-Stay-Prediction/blob/master/images/Neural%20Network.png)

## Prediction and Results
The XGBoost model performed best, with predictions closely aligning with actual LOS. The distribution of predictions indicates most patients stay between 21-30 days, with fewer staying beyond 60 days.

## Future Insights
- Smart Staffing & Personnel Management: Efficient resource allocation based on data analysis.
- Advanced Risk & Disease Management: Accurate preventive care through insights into patient conditions and treatment outcomes.
- Real-time Alerting (Clinical Decision Support): Providing recommendations to health professionals for prescriptive choices.
- Enhancing Patient Engagement: Tracking patient activities and health metrics to identify potential risks.

## Conclusion
Predicting patient LOS at the time of admission helps hospitals allocate resources efficiently and manage patients better. This project demonstrates the potential of using healthcare analytics to improve hospital management and patient care.
