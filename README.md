# Intelligent-Intrusion-Detection-System
## Overview

This project focuses on detecting cyber threats using machine learning techniques. By analyzing network traffic data, the model aims to identify and classify different types of cyber-attacks such as DDoS, Ransomware, and Normal traffic. The dataset contains various network attributes such as packet length, protocol type, and traffic flow metrics to help the model distinguish between normal and malicious activities.

## Problem Statement

In today’s digital landscape, cyber-attacks are a significant concern for businesses and organizations. The goal of this project is to build a machine learning model that can analyze network traffic and identify potential cyber threats. By automating threat detection, this project helps to reduce the time and effort required for manual monitoring and improves network security.

Dataset Description The dataset consists of network traffic logs with various features such as:

Timestamp: Time of packet capture 
Source_IP: The source IP address of the traffic 
Destination_IP: The destination IP address 
Protocol: Protocol used in the network communication (e.g., ICMP, UDP) 
Packet_Length: Length of the packet 
Bytes_Sent/Bytes_Received: The amount of data sent or received 
Flow_Packets/s
Flow_Bytes/s: 
Flow metrics Attack_Type: The type of attack (DDoS, Ransomware, or Normal) 
Each row is labeled with a Label that indicates whether the traffic is malicious or normal.

Dataset name : cyberfeddefender_dataset.csv (located under 'data' subfolder inside backend project folder)

## Steps Involved 

1️⃣ Data Preprocessing Clean and process raw network traffic data. Handle missing values, duplicate entries, and outliers. Encode categorical variables like Protocol and Attack_Type. Normalize or scale continuous features.

2️⃣ Exploratory Data Analysis (EDA) Analyze the distribution of features. Visualize patterns to understand relationships between different network metrics and attack types. Identify correlations between features and the target variable (Label).

3️⃣ Model Development Train multiple machine learning models (e.g., Random Forest, XGBoost, SVM) to detect anomalies. Fine-tune the hyperparameters of the best-performing models. Evaluate models using metrics such as accuracy, precision, recall, and F1-score.

4️⃣ Model Deployment Once the best model is selected, it will be deployed as a web service. The model will be containerized using Docker for easy deployment and scaling.

The project consists of two major components:

  1️⃣ Front end project
  2️⃣ Back end project

Frontend Project :

Functionality: User interface to input Cyber Threat Detection features, submit the form, and get the predicted label for cyber attacks with probabilities from the backend.
Technologies Used:
HTML5
React.js (useState hook, Axios for API calls)
Backend Project

Functionality: API for predicting cyber attack labels using a trained machine learning model.

Technologies Used:

Python
Flask (API to serve the model)
Python Libraries: Flask, scikit-learn, pandas, numpy, matplotlib, pickle-mixin
Other Tools: Pipenv for virtual environment management, Docker for containerization
Scripts: notebook.ipynb, model.py, predict.py
