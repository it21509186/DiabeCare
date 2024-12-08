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

1. Data Dependencies
- Dataset  
  - Comprehensive health dataset (age, sex, glucose levels, BMI, etc.) for diabetic care.  
  - Annotated datasets for food recognition with features like food type, portion size, and nutritional content (e.g., calories, protein, carbohydrates).  
  - Health indicator ranges (e.g., BMI classifications, blood glucose thresholds).  
  - Historical meal data for dietary trend analysis and personalized recommendations.  

- Real-Time Data Sources
  - Fitness trackers, smartwatches, and glucose monitors for health tracking.  
  - User-uploaded meal photos or videos for real-time calorie estimation.  
  - APIs for barcode scanning of packaged foods for nutritional data retrieval.  



2. Software Dependencies
- Programming Languages
  - Python: For predictive analytics, backend logic, food recognition algorithms, and calorie estimation.  
  - Dart: For mobile frontend development using Flutter.  

- Libraries and Frameworks  
  - TensorFlow/Keras: For CNN-based food recognition and health data predictions.  
  - OpenCV: For image preprocessing and volume estimation.  
  - Pandas, NumPy: For data processing (health and nutritional data).  
  - Flask/Django: For building RESTful APIs to serve health and food calorie data.  

- APIs 
  - Health APIs (Google Fit, Apple HealthKit) for glucose and fitness tracking.  
  - FoodData Central or Edamam API for nutritional information retrieval.  



3. Hardware Dependencies
- Smart Devices
  - Wearables for real-time health monitoring (e.g., physical activity, glucose).  
  - Smartphones with high-resolution cameras for meal uploads.  
  - Barcode scanners for packaged food data integration.  

- Cloud Services
  - AWS: For scalable model deployment, data storage, and processing (health and food data).  



4. Machine Learning Dependencies
- Algorithms 
  - CNN: For food recognition and feature extraction from meal images.  
  - ARIMA/LSTM: For blood glucose trend predictions.  
  - Regression models: For calorie prediction based on meal composition and user activity.  

- Feature Engineering Tools
  - Libraries for normalizing data (e.g., glucose levels, meal portions).  

- Model Training Environment  
  - Jupyter Notebook/Google Colab: For developing and testing models.  



5. Integration and Security Dependencies
- Authentication Services 
  - OAuth: For secure user authentication.  
  - Two-factor authentication: For protecting sensitive user data.  

- Data Encryption  
  - AES/RSA: For encrypting sensitive health and food data.  
  - HTTPS: For secure app-backend communication.  

- Data Storage  
  - Firebase: For storing meal logs, calorie estimates, and health data in real-time.  
  - Relational databases (PostgreSQL): For structured data storage (user profiles, historical logs).  



6. User Engagement Dependencies
- Notification Services
  - Firebase Cloud Messaging (FCM): For meal reminders, dietary tips, and health alerts.  

- Visualization
  - Dashboards for tracking trends in calorie intake, glucose levels, and adherence to recommendations.  



7. Testing and Deployment Dependencies
- Testing Tools  
  - Selenium/Appium: For automated UI testing of mobile features.  
  - PyTest: For backend logic and API testing.  

- Deployment
  - CI/CD tools (Jenkins/GitHub Actions): For seamless deployments.  
  - Google Play Store and Apple App Store: For mobile app distribution.  



8. Health Monitoring
- Lab Report Analysis
  - Preprocess lab reports to analyze health metrics (HbA1c, fasting blood sugar).  
  - Detect risk levels and provide personalized recommendations.  

- Calorie Tracking
  - Monitor meal compositions and calorie consumption for dietary compliance.  



9. Future Blood Glucose Level Prediction
- Predictive Models
  - ARIMA/LSTM models for forecasting glucose trends.  
  - Incorporate meal details, physical activity, and medication history for personalized insights.  

- Notifications  
  - Real-time alerts for predicted high-risk glucose levels or unhealthy meal patterns.  



10. Trend Analysis and Reporting
- Blood Glucose Trends
  - Weekly, monthly, and yearly analysis of blood glucose levels and lab findings.  

- Calorie Intake Analysis
  - Generate personalized reports highlighting meal patterns, deviations, and nutritional gaps.  
  - Provide actionable insights for healthcare providers and users to optimize diets.
 
# Git Hub Repo Link
https://github.com/it21509186/DiabeCare.git



