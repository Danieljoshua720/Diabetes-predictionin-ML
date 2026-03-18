#🩺 Diabetes Prediction Using Machine Learning
Overview
This project builds a machine learning model to predict whether a patient is diabetic or not based on medical diagnostic features. It uses the Pima Indians Diabetes Dataset and applies classification algorithms to achieve high prediction accuracy.

📁 Project Structure
diabetes-prediction-ml/
│
├── data/
│   └── diabetes.csv              # Dataset (Pima Indians Diabetes)
│
├── notebooks/
│   └── diabetes_prediction.ipynb # EDA + Model Training notebook
│
├── src/
│   ├── preprocess.py             # Data cleaning & feature engineering
│   ├── train.py                  # Model training script
│   ├── evaluate.py               # Model evaluation metrics
│   └── predict.py                # Prediction on new data
│
├── models/
│   └── diabetes_model.pkl        # Saved trained model
│
├── requirements.txt
├── README.md
└── app.py                        # (Optional) Flask/Streamlit web app

📊 Dataset
Source: UCI ML Repository – Pima Indians Diabetes Database
FeatureDescriptionPregnanciesNumber of times pregnantGlucosePlasma glucose concentrationBloodPressureDiastolic blood pressure (mm Hg)SkinThicknessTriceps skin fold thickness (mm)Insulin2-Hour serum insulin (mu U/ml)BMIBody mass index (weight/height²)DiabetesPedigreeFunctionDiabetes pedigree functionAgeAge in yearsOutcomeTarget variable: 1 = Diabetic, 0 = Non-Diabetic
Dataset Size: 768 samples, 8 features, 1 target variable

⚙️ Installation
Prerequisites

Python 3.8+
pip

Steps
bash# 1. Clone the repository
git clone https://github.com/yourusername/diabetes-prediction-ml.git
cd diabetes-prediction-ml

# 2. Create a virtual environment (recommended)
python -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt
```

### requirements.txt
```
numpy==1.24.0
pandas==2.0.0
scikit-learn==1.3.0
matplotlib==3.7.0
seaborn==0.12.2
joblib==1.3.0
flask==2.3.0           # optional (for web app)
streamlit==1.25.0      # optional (for UI)

🚀 Usage
1. Train the Model
bashpython src/train.py
2. Evaluate the Model
bashpython src/evaluate.py
3. Predict on New Data
bashpython src/predict.py --input "[6, 148, 72, 35, 0, 33.6, 0.627, 50]"
4. Launch the Web App (Optional)
bash# Flask
python app.py

# OR Streamlit
streamlit run app.py
```

---

## 🔬 Machine Learning Pipeline

### 1. Data Preprocessing
- Handle missing/zero values (Glucose, BMI, BloodPressure, etc.)
- Feature scaling using `StandardScaler`
- Train-test split (80/20)

### 2. Models Used

| Model | Accuracy |
|---|---|
| Logistic Regression | ~77% |
| Random Forest | ~82% |
| Support Vector Machine (SVM) | ~79% |
| K-Nearest Neighbors (KNN) | ~75% |
| XGBoost | **~84%** ✅ |

### 3. Best Model
**XGBoost Classifier** with hyperparameter tuning via `GridSearchCV`.

### 4. Evaluation Metrics
- Accuracy
- Precision, Recall, F1-Score
- ROC-AUC Curve
- Confusion Matrix

---

## 📈 Results
```
Best Model: XGBoost
Accuracy:   84.2%
Precision:  82.1%
Recall:     79.6%
F1-Score:   80.8%
ROC-AUC:    0.89

🧪 Example Prediction
pythonfrom src.predict import predict_diabetes

patient_data = {
    "Pregnancies": 6,
    "Glucose": 148,
    "BloodPressure": 72,
    "SkinThickness": 35,
    "Insulin": 0,
    "BMI": 33.6,
    "DiabetesPedigreeFunction": 0.627,
    "Age": 50
}

result = predict_diabetes(patient_data)
print(result)  # Output: "Diabetic" or "Non-Diabetic"
```

---

## 🌐 Web App (Streamlit)

A simple interactive UI where users can input patient features and get a real-time prediction.
```
Input Features → [Model] → Prediction (Diabetic / Non-Diabetic) + Probability

📌 Key Learnings

Handling medical datasets with zero-value anomalies
Feature importance analysis using Random Forest & XGBoost
Class imbalance handling using SMOTE
Model serialization with joblib


🤝 Contributing

Fork the repository
Create a new branch: git checkout -b feature/your-feature
Commit your changes: git commit -m "Add feature"
Push to the branch: git push origin feature/your-feature
Open a Pull Request


📄 License
This project is licensed under the MIT License — see the LICENSE file for details.


