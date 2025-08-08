# Loan Eligibility Prediction Web App

## 📌 Description
A full-stack web application that predicts a user's **loan eligibility** based on their financial and personal details.  
- **Frontend:** React.js (Vite or CRA) with Tailwind CSS  
- **Backend:** Flask API serving predictions from a trained ML model  
- **Model:** RandomForestClassifier trained on historical loan data  

---

## 📂 Project Structure
loan-eligibility-app/
│
├── backend/ # Flask server handling API requests and ML predictions
├── frontend/ # React.js application for user interaction
├── model/ # Trained machine learning model (.pkl file)
├── train.csv # Dataset used to train the model
├── README.md # Project documentation
└── TrainAndSaveModel.ipynb # Notebook to preprocess, train, and export the model


---

## 🔧 Backend
- **Framework:** Flask  
- **Endpoint:** `POST /predict` — accepts 11 user inputs  
- **Functionality:**
  - Preprocesses inputs to match the training pipeline  
  - Loads the trained ML model (`logistic_model.pkl`)  
  - Returns prediction: `"Approved"` or `"Rejected"`  
- **CORS:** Enabled via `flask-cors` to allow frontend communication  

**Dependencies:**

Flask
numpy
pickle
flask-cors
## 💻 Frontend
Framework: React.js (Vite or Create React App)

## Features:

Form inputs for user financial/personal data

Sends data to backend /predict route

Displays result with styled UI animations

Styling: Tailwind CSS with subtle animations

## 🧠 Model
Algorithm: RandomForestClassifier

Features: 11 engineered features (Gender, Income, Credit History, etc.)

Training: Implemented in TrainAndSaveModel.ipynb

Serialization: Saved as model/logistic_model.pkl via pickle

## 📈 Algorithms Used
1. RandomForestClassifier
Ensemble method that builds multiple decision trees and merges their predictions for better accuracy and reduced overfitting.

2. LogisticRegression (Optional)
A linear model for binary classification — can be used by modifying the training notebook.

##⚡ How to Run the Project
Prerequisites
Python 3.x

Node.js & npm

pip (Python package installer)

1. Clone the Repository
bash
Copy
Edit
git clone <your-repo-url>
cd loan-eligibility-app
2. Backend Setup
bash
Copy
Edit
cd backend
pip install -r requirements.txt
python app.py
3. Frontend Setup
bash
Copy
Edit
cd frontend
npm install
npm run dev
4. Train the Model (Optional if already trained)
Open TrainAndSaveModel.ipynb in Jupyter or VS Code

Run all cells to save model to /model/logistic_model.pkl

Note: Ensure Flask backend is running at http://localhost:5000 before testing the frontend.

## ✅ Result
Instant loan eligibility predictions

Fully responsive UI

Graceful handling of invalid inputs

## 📚 Learning Outcomes
Integrating ML models into full-stack applications

Preprocessing & encoding categorical data

Managing CORS and API communication

Local deployment of ML-powered web apps

## 🚀 Future Improvements
Deploy on Render / Vercel / Railway

Add authentication & user accounts

Store prediction history in a database (SQLite / MongoDB)

Hyperparameter tuning with GridSearchCV

Enhanced UI with charts and personalized feedback

Built with ❤️ using Python, React, and Machine Learning
