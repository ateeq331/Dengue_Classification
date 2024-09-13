Dengue Fever Prediction Android App
Overview
The Dengue Fever Prediction App allows users to predict the likelihood of dengue fever based on various medical and environmental factors. It is powered by a machine learning model trained to analyze input features such as blood test results, patient condition, and weather conditions. The app provides an easy-to-use interface for doctors and healthcare professionals to assess the risk of dengue fever in patients.

Features
User-friendly Interface: Simple, clean, and intuitive design for entering medical and environmental data.
Real-time Prediction: Provides instant predictions based on the input data using a trained Random Forest model.
Secure Data Handling: Ensures all medical data entered is processed securely within the app.
Machine Learning Model Integration: Uses a pre-trained Random Forest model to predict dengue fever outcomes.
Responsive and Mobile-friendly Design: Optimized for both mobile and tablet devices.
Screenshots
Include screenshots of the splash screen, prediction form, and results screen to showcase the app's interface.

Installation
To run this app on your Android device, follow these steps:

Prerequisites
Android Studio: You will need to install Android Studio to build and run the app.
Minimum SDK: 21 (Android 5.0 Lollipop)
Target SDK: 30 (Android 11)
Setup Instructions
Clone the Repository:

bash
Copy code
git clone https://github.com/yourusername/dengue-fever-prediction-app.git
Open the Project in Android Studio:

Launch Android Studio.
Select "Open an Existing Project" and navigate to the cloned repository folder.
Install Dependencies:

The necessary libraries and dependencies will automatically be installed via Gradle.
Run the App:

Connect an Android device or launch an emulator.
Click the green "Run" button in Android Studio to install and run the app.
Usage
Launch the App: Once installed, open the app from your Android device.
Input Features: Enter the required patient information, including:
Age
Gender
NS1, IGG, IGM test results
WBC, HCT, Platelet counts
Patient Condition & Outcome
Environmental data: temperature, humidity, wind speed
Prediction: Press the "Predict" button to get the likelihood of dengue fever.
Result: The app will display the prediction result immediately, either as "Dengue Fever" or "No Dengue Fever."
Backend Model
The app integrates with a machine learning backend via Flask, which processes the input data and returns predictions based on the trained model. The model uses Random Forest classification to predict dengue fever based on the following input features:

NS1, IGG, IGM: Blood test results related to dengue fever detection.
WBC, HCT, Platelet: Key medical indicators for dengue fever.
Environmental factors: Temperature, humidity, and wind speed influence the prediction.
API Integration
This app connects to a Flask API deployed on a Hugging Face Space. The API accepts POST requests containing medical and environmental data, processes them through the machine learning model, and returns a prediction.

API Endpoint
POST /predict:
Input: Medical and environmental data as form inputs.
Output: String response with the prediction.
Example Request:
bash
Copy code
curl -X POST https://adeveloper-dengue.hf.space/predict \
  -F 'age=35' \
  -F 'gender=1' \
  -F 'ns1=1' \
  -F 'igg=0' \
  -F 'igm=0' \
  -F 'wbc=4.5' \
  -F 'hct=0.40' \
  -F 'platelets=150000' \
  -F 'condition=1' \
  -F 'outcome=1' \
  -F 'temperature=32.5' \
  -F 'humidity=80' \
  -F 'wind=12'
Example Response:
makefile
Copy code
Prediction: Dengue Fever
Contributions
If you’d like to contribute to this project, feel free to fork the repository and submit a pull request. We welcome improvements related to UI/UX, machine learning models, and app performance.

License
This project is licensed under the MIT License - see the LICENSE file for details.

Contact
For any questions or feedback, please contact:

Developer: Muhammad Ateeq Haider
Email: andrddvlpr.2208@gmail.com
