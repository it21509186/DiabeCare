# DiabeCare
Integrated Healthcare Management System for Enhanced Diabetic Patient Care

# Research Question
Diabetes is a growing public health concern worldwide, with significant implications for individuals' 
health and quality of life. In Sri Lanka, the prevalence of diabetes has been rising steadily, posing 
a major public health challenge. Effective management of diabetes requires continuous 
monitoring and regulation of various health parameters. Many diabetic patients face challenges 
in maintaining consistent and accurate records of these parameters, leading to suboptimal disease 
management and increased risk of complications. However, existing mobile applications often fall 
short of providing comprehensive, integrated solutions that address all aspects of diabetes 
management. Below, we outline five key research problems related to diabetes management 
applications, demonstrating how our proposed system offers superior.
Most existing applications focus on a single aspect of diabetes management, such as blood glucose 
monitoring or dietary tracking, but fail to provide a holistic view of a patient’s health. For instance, 
apps like MySugr focus primarily on blood sugar logging, while lose it, (Seto et al., 2016) centers 
on dietary tracking. Our system integrates multiple health parameters including calorie intake, 
medication adherence, physical activity, and vital signs, offering a comprehensive overview of the 
patient’s health status.
Many applications do not support seamless integration with various health monitoring devices, 
leading to inconsistent and inaccurate data entry. Apps like Glucose Buddy (Wu et al., 2019) 
require manual entry of blood glucose levels, which can be error prone. Our system’s use of Scan
integration for automatic data transfer from blood glucose monitors ensures accuracy and reduces 
the burden on patients.
While some apps provide basic recommendations, they often lack the sophistication to offer 
personalized advice based on comprehensive data analysis. For example, the Diabetes app (Brzan 
et al., 2016) offers general dietary advice but does not tailor recommendations based on individual 
health data. Our system employs machine learning to analyze integrated health data and deliver 
personalized insights and recommendations, making it more effective in guiding patients’ daily 
management.
Few applications utilize advanced predictive analytics to foresee potential health issues and 
provide proactive recommendations. The Glooko app (Foster et al., 2016) offers trend analysis also 
excellent tracking. But it is not available in our region. Our system is available to all the Sri Lankan 
diabetic patients along with the more excellent tracking. Also, algorithms predict future health 
risks and outcomes, allowing for early intervention and better long-term management of 
diabetes.
Maintaining user engagement and adherence to diabetes management plans is a significant 
challenge. Apps like BlueLoop (Moore et al., 2014) provide excellent tracking features but struggle 
with keeping users consistently engaged. Our system addresses this by offering a user-friendly 
interface combined with comprehensive, actionable insights, thus encouraging sustained use and 
adherence to management plans.


# Project Overview
The Integrated Healthcare Management System for Enhanced Diabetic Patient Care offers an 
easy-to-use solution for managing diabetes. It uses advanced technologies like image recognition, 
Scan, and machine learning. The system includes four components: Food Calories Estimation, 
Medication and Blood Glucose Monitoring, Activity Management and Suggestion, and Overall, 
Health Care Management, providing a complete view of the patient's health and personalized 
recommendations.
Food Calories Estimation System:
• Patient using video input and upload photos of their meals.
• The system identifies the meal, calculates its calorie content including the levels such as 
protein, carbohydrate etc. and estimates its volume.
• It tracks total daily calories and, after accounting for exercise, calculates net remaining 
calories.
• Machine learning provides personalized dietary advice based on calorie intake and 
exercise.
• Gradually recommending changes to reduce portions and maintain a consistent calorie 
count, while helping patient control and manage their diet without sudden restrictions.
Medication and Blood Glucose Monitoring System:
• Record types and amounts of medications, ensuring adherence to schedules.
• Patients specify medication type (tablets or insulin) before entry.
• Monitor glucose levels: tablets monthly after an 8-hour fast; insulin daily before meals.
• Automatically log blood glucose levels from scan-enabled devices and maintain history 
charts for trend analysis.
• Continuously track sugar levels, suggesting weekly doctor visits if levels fluctuate.
• Notify a family member if levels drop significantly and alert ambulance services for 
severe drops.
• Allow real-time data access for doctors, with weekly reports sent to them that include 
medication history and glucose analysis.
Activity Management and Suggestion System:
• Record types, durations, and frequencies of exercises performed by the patient, either 
manually or using built-in sensor APIs and smart devices.
• Maintain a detailed log of physical activity over time.
• Provide personalized exercise recommendations based on patient data, health status, 
preferences, and activity history.
• Suggest specific types of exercises, along with their duration and frequency, tailored for 
diabetic patients.
Overall, Health Care Management System:
• Monitors key health metrics such as blood pressure, heart rate, blood oxygen levels, 
height, and weight also provide an alert whether the diabetic level will increase, decrease

# Architectural Diagram 
![sytem_overview_diagram](https://github.com/user-attachments/assets/90271e88-d54f-45d7-ba57-90827f57c32c)


# Dependencies
Dependencies for the Comprehensive Integrated Healthcare Management System

1. Data Dependencies

Dataset:

Comprehensive dataset with features like age, sex, exercise type, glucose levels, BMI, diabetes type, blood pressure, heart rate, blood oxygen level, height, and weight.

Annotated datasets for food recognition with features like food type, portion size, and nutritional content (e.g., calories, protein, carbohydrates).

Health indicator ranges (e.g., BMI classifications with normal weight ranges, blood glucose thresholds).

Historical health data for trend analysis and model training.

Historical meal data for dietary trend analysis and personalized recommendations.

Real-Time Data Sources:

Fitness trackers, smartwatches, glucose monitors for real-time data collection.

User-uploaded meal photos or videos for real-time calorie estimation.

APIs for barcode scanning of packaged foods for nutritional data retrieval.

Integration with health APIs like Google Fit, Apple HealthKit, or device SDKs.

2. Software Dependencies

Programming Languages:

Python: For machine learning, predictive analytics, backend logic, food recognition algorithms, and calorie estimation.

JavaScript: For frontend and interactive dashboard development.

Dart: For mobile frontend development using Flutter.

Libraries and Frameworks:

Machine Learning:

TensorFlow, Keras, Scikit-learn, or PyTorch for model training and predictive analytics.

Optuna or GridSearchCV for hyperparameter tuning.

Data Analysis and Visualization:

Pandas, NumPy for data manipulation and analysis.

Matplotlib, Seaborn, D3.js, or Chart.js for dashboards and trend visualizations.

Mobile and Web Development:

Flutter or React Native for mobile app development.

Flask/Django for building RESTful APIs to serve health and food calorie data.

APIs:

Google Fit API, Apple HealthKit API, or Open mHealth APIs for health data integration.

FoodData Central or Edamam API for nutritional information retrieval.

Notification APIs (e.g., Firebase Cloud Messaging, APNS).

3. Hardware Dependencies

Smart Devices:

Wearables for real-time health monitoring (e.g., physical activity, glucose).

Smartphones with high-resolution cameras for meal uploads and sensors for step count, activity duration, etc.

Barcode scanners for packaged food data integration.

Cloud Services:

Cloud platforms like AWS, Google Cloud, or Microsoft Azure for hosting the backend, running predictive models, storing health and food data securely, and providing scalable model deployment.

4. Machine Learning Dependencies

Algorithms:

CNN: For food recognition and feature extraction from meal images.

ARIMA/LSTM: For blood glucose trend predictions.

Regression models: For calorie prediction based on meal composition and user activity.

Decision Tree, Random Forest for classification and prediction.

Clustering algorithms for grouping patients by trends.

Feature Engineering Tools:

Libraries for preprocessing data (e.g., handling missing data, normalizing glucose levels, scaling meal portions).

Image preprocessing tools for diabetic foot image analysis.

Model Training Environment:

Jupyter Notebook/Google Colab for developing and testing models.

Deployment-ready environments for real-time analytics.

5. Integration and Security Dependencies

Authentication Services:

OAuth for secure user login and integration with health platforms.

Two-factor authentication (2FA) for added security.

Data Encryption:

AES or RSA for encrypting sensitive health and food data.

HTTPS for secure app-backend communication.

Data Storage:

Firebase for storing meal logs, calorie estimates, and health data in real-time.

Relational databases (PostgreSQL, MySQL) for structured data storage (user profiles, historical logs).

NoSQL databases (e.g., MongoDB) for flexible data storage.

6. User Engagement Dependencies

Gamification Frameworks:

Dependencies for creating badges, progress tracking, and challenges for user motivation.

Notification Services:

Firebase Cloud Messaging (FCM), Apple Push Notification Service (APNS) for meal reminders, dietary tips, and health alerts.

Visualization Tools:

Dashboards for tracking trends in calorie intake, glucose levels, adherence to recommendations, and overall health insights.

Libraries like D3.js or Chart.js for interactive visualizations.

7. Testing and Deployment Dependencies

Testing Tools:

Selenium or Appium for automated UI testing of mobile features.

PyTest or Mocha for backend logic and API testing.

Deployment Platforms:

Google Play Store and Apple App Store for mobile app distribution.

CI/CD tools (Jenkins, GitHub Actions) for seamless deployments.

8. Health Monitoring

Record key indicators like blood pressure, heart rate, blood oxygen levels using smart devices.

Calculate BMI values and classify patients using a tabular display of world-recognized normal BMI ranges (e.g., healthy, unhealthy).

Preprocess lab reports to analyze health metrics (HbA1c, fasting blood sugar) and detect risk levels for personalized recommendations.

9. Trend Analysis and Reporting

Blood Glucose Trends:

Weekly, monthly, and yearly analysis of blood glucose levels and lab findings.

Calorie Intake Analysis:

Generate personalized reports highlighting meal patterns, deviations, and nutritional gaps.

Provide actionable insights for healthcare providers and users to optimize diets.

Health Insights and Reporting:

Generate reports with detailed progression of health indicators.

Include actionable suggestions and highlight abnormal data points with red markers for better visibility.

10. Predictive Analytics for Diabetic Foot Health

Predictive Models:

Train machine learning models for risk assessment using uploaded images of patient feet.

Preprocess, analyze, and provide risk evaluations and recommendations for patient care.

Notifications:

Automated alerts for healthcare providers when critical health parameters exceed safe ranges.

11. Alert System

Notifications:

Real-time alerts for predicted high-risk glucose levels, unhealthy meal patterns, or deviations from health norms.

 
# Git Hub Repo Link
https://github.com/it21509186/DiabeCare.git



