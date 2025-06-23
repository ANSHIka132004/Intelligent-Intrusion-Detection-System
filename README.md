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

Frontend Setup:

Steps to Set Up and Run the Frontend in local:

Open the project folder in Visual Studio Code.
Click on Terminal->New Terminal from the menu on the top.

1. Install Required Software:

Install Node.js.

Verify installation:

  node -v
  npm -v

2. Initialize the Project:

  Navigate to the frontend project directory

  cd frontend

3. Install dependencies:

   npm install

4. Run the Development Server:

  Start the React development server

  npm run dev

  The frontend application should now be accessible at http://localhost:5173

  UI will look as follows:

  ![Screenshot 2025-06-05 054450](https://github.com/user-attachments/assets/2b1fbf4b-c7ba-433d-b611-5d2dbbb3eed0)


5. Key Dependencies:

   React.js: User interface components
   Axios: Library for making HTTP requests (for communicating with the Flask backend)

   (Note: If any error related to axios library being not accessible, kindly run this command in the terminal:  npm install axios. Then run frontend app by providing npm run dev)

Backend Setup:

Follow below steps to run backend app.

Click on Terminal->New Terminal from the menu on the top.

Please proceed the following steps in the terminal (Navigate to the path of the project)
Prerequesite : Install Required Software:

  Install Python (3.11 or later).

  Install pipenv using below command:

  pip install pipenv
       
1. Navigate to backend project folder

  cd backend

2. Steps to Create Pipfile and Pipfile.lock

  pip install -r requirements.txt

3. Verify the Pipenv Environment:

  Activate the virtual environment:

  pipenv shell

4. Confirm installation of dependencies:

  pip list

5. Deactivate the environment when done

  exit

6. Export Dependencies to Pipfile.lock:

The Pipfile.lock will be automatically generated when you run pipenv install.
Verify that it exists in the backend directory.

7. Steps to Dockerize the Backend

   Run the following command to build the Docker image: (from Dockerfile)

   docker build -t flask-predict-app .
   ![Screenshot 2025-06-23 182128](https://github.com/user-attachments/assets/2b9e80d6-556c-4853-b5d6-2125714d89fc)


9. Run the Docker Container:
   
  Start the Flask app inside the container:

  docker run -p 5002:5002 flask-predict-app
  ![Screenshot 2025-06-23 205628](https://github.com/user-attachments/assets/c4f36ce7-8fa9-4f3f-9e17-d1d2b75e37ce)
![Screenshot 2025-06-23 205638](https://github.com/user-attachments/assets/d8716c6b-12d1-49ae-a426-00a5fa2f4e35)



9. Test the backend API : Ensure the backend is running at

    http://localhost:5002

   Use tools like Postman or the frontend React app to test the /predict endpoint.
![Screenshot 2025-06-05 052945](https://github.com/user-attachments/assets/62aa97a7-ed3e-4a53-b42d-98663a615883)



