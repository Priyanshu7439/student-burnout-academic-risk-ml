#Student Burnout & Academic Risk Prediction System

A Machine Learning based system designed to predict student burnout levels and academic performance risks using behavioral and academic indicators.

This project applies machine learning techniques to analyze student lifestyle factors such as study hours, sleep patterns, screen time, attendance, and physical activity in order to identify early signs of burnout and academic risk.

The system also includes a Streamlit-based interactive web application that allows users to input student information and receive predictions in real time.


#Project Motivation

In modern academic environments, students frequently experience stress due to high academic pressure, irregular sleep cycles, excessive screen exposure, and reduced physical activity.

These factors can lead to:
	•	Academic burnout
	•	Reduced productivity
	•	Poor academic performance

Traditional monitoring systems detect these problems after they occur.
This project aims to create a predictive system that identifies potential risks early using machine learning.



#Key Features
	•	Predicts student burnout level
	•	Predicts academic risk based on behavioral indicators
	•	Uses multiple machine learning algorithms for comparison
	•	Performs data preprocessing and feature scaling
	•	Provides evaluation metrics such as accuracy and F1 score
	•	Includes an interactive Streamlit web interface



#Dataset

The dataset used in this project is synthetic (self-created).

Dataset Information

Total Records: 350

Features:
	•	student_id
	•	age
	•	gender
	•	study_hours_per_day
	•	sleep_hours_per_day
	•	attendance_percentage
	•	assignment_delay_days
	•	screen_time_hours
	•	physical_activity_hours
	•	cgpa
	•	burnout_score
	•	burnout_level (target)

Class Distribution: Slightly Imbalanced



#Machine Learning Models Used

Several machine learning algorithms were tested:
	•	Logistic Regression
	•	Random Forest
	•	Support Vector Machine (SVM)
	•	K-Nearest Neighbors
	•	Naive Bayes

After comparison, Logistic Regression produced the best performance for the burnout prediction model.



#Model Performance

#Burnout Prediction Model

Algorithm: Logistic Regression

Train Accuracy: 97.14%

Test Accuracy: 91.42%

Macro F1 Score: 0.878



#Academic Risk Model

Algorithm: Logistic Regression

Train Accuracy: 42.85%

Test Accuracy: 37.14%

Macro F1 Score: 0.37

The lower accuracy of the academic model indicates that academic performance prediction requires additional factors such as psychological and socio-economic variables.



#Data Preprocessing

The following preprocessing techniques were applied:
	•	Missing value handling (rows dropped)
	•	Label Encoding for categorical variables
	•	Feature scaling using StandardScaler
	•	Train-Test Split (80:20)
	•	Random State: 42



#Exploratory Data Analysis

Several visualizations were used to understand the dataset:
	•	Feature correlation heatmap
	•	Class distribution plots
	•	Feature importance analysis

These analyses helped identify key predictors such as:
	•	Assignment delay days
	•	Sleep hours
	•	Study hours
	•	CGPA
Project Structure
```
Student-Burnout-Academic-Risk-Prediction
│
├── data
│   └── raw
│       └── student_burnout_dataset.csv
│
├── models
│   └── trained_models.pkl
│
├── notebooks
│   ├── eda.ipynb
│   ├── burnout_model_comparison.ipynb
│   └── academic_performance_comparison.ipynb
│
├── src
│   ├── academic
│   │   ├── preprocessing.py
│   │   ├── train_model.py
│   │   ├── evaluate.py
│   │   ├── predict.py
│   │   └── main.py
│   │
│   └── burnout
│       ├── data_preprocessing.py
│       ├── train_model.py
│       ├── evaluate.py
│       ├── predict.py
│       └── main.py
│
└── z_app
    └── app.py
```
#Installation

#Clone the repository
git clone https://github.com/yourusername/student-burnout-risk-prediction.git

#Move into the project directory:
cd student-burnout-risk-prediction

#Install dependencies
pip install -r requirements.txt

#Running the Application

Start the Streamlit application:
streamlit run z_app/app.py

Then open your browser and go to:
http://localhost:8501

#Streamlit Application

The web application allows users to input student parameters including:
	•	Age
	•	Study Hours
	•	Sleep Hours
	•	Attendance
	•	Screen Time
	•	Physical Activity
	•	CGPA
	•	Assignment Delay

The model then predicts the burnout level of the student.


#Future Improvements
	•	Use real educational datasets
	•	Include psychological and socio-economic variables
	•	Apply ensemble learning techniques
	•	Improve academic performance prediction accuracy
	•	Deploy the system on cloud platforms

#Technologies Used
	•	Python
	•	Scikit-learn
	•	Pandas
	•	NumPy
	•	Matplotlib
	•	Seaborn
	•	Streamlit


#Author
Priyanshu Kumar
