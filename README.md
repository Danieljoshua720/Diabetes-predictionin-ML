# 🩺 Diabetes Prediction Web App

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Flask](https://img.shields.io/badge/Flask-2.0+-green.svg)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0+-orange.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

A machine learning web application that predicts whether a person is **Diabetic or Non-Diabetic** based on medical inputs, using **Logistic Regression** and served via a **Flask** web interface.

---

## 🌐 Live Demo

> Enter patient details → Get instant diabetes prediction

---

## 📁 Project Structure
```
Diabetes-prediction/
│
├── Logistic_Regression.ipynb     # Model training, EDA & evaluation
├── modelForPrediction.pkl        # Saved trained Logistic Regression model
├── standardScalar.pkl            # Saved StandardScaler for input normalization
│
├── app.py                        # Flask backend – routes & prediction logic
├── home.html                     # Home / landing page
├── index.html                    # Patient input form
├── single_prediction.html        # Prediction result page
│
└── README.md
```

---

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/Danieljoshua720/Diabetes-prediction.git
cd Diabetes-prediction
```

### 2. Create a Virtual Environment
```bash
python -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install flask scikit-learn numpy pandas joblib
```

---

## 🚀 Run the App
```bash
python app.py
```

Then open your browser and go to:
```
http://127.0.0.1:5000
```

---

## 🔬 Machine Learning Model

| Detail | Info |
|--------|------|
| Algorithm | Logistic Regression |
| Dataset | Pima Indians Diabetes Dataset |
| Preprocessing | StandardScaler |
| Saved Model | `modelForPrediction.pkl` |
| Saved Scaler | `standardScalar.pkl` |

---

## 🌐 App Flow
```
🏠 home.html
     ↓
📋 index.html        ← User enters medical details
     ↓
⚙️  app.py           ← Flask loads model & scaler, runs prediction
     ↓
✅ single_prediction.html  ← Shows: Diabetic / Non-Diabetic
```

---

## 📊 Input Features

| Feature | Description |
|---------|-------------|
| Pregnancies | Number of times pregnant |
| Glucose | Plasma glucose concentration |
| BloodPressure | Diastolic blood pressure (mm Hg) |
| SkinThickness | Triceps skin fold thickness (mm) |
| Insulin | 2-Hour serum insulin (mu U/ml) |
| BMI | Body mass index |
| DiabetesPedigreeFunction | Genetic diabetes risk score |
| Age | Age in years |

---

## 📄 Key Files Explained

| File | Purpose |
|------|---------|
| `Logistic_Regression.ipynb` | Data cleaning, EDA, model training, saving `.pkl` files |
| `app.py` | Flask app – handles routing, loads model, returns prediction |
| `modelForPrediction.pkl` | Serialized Logistic Regression model |
| `standardScalar.pkl` | Fitted scaler to normalize user input before prediction |
| `index.html` | HTML form to collect patient data |
| `single_prediction.html` | Displays the final prediction result |

---

## 📸 Screenshots

> *(Add screenshots of your home page, input form, and result page here)*
```
home.html          index.html         single_prediction.html
[Home Page]  →→→  [Input Form]  →→→  [Result: Diabetic ✅]
```

---

## 🛠️ Tech Stack

- **Backend:** Python, Flask
- **ML:** Scikit-learn, Logistic Regression
- **Frontend:** HTML, CSS
- **Model Serialization:** Joblib / Pickle

---

## 🤝 Contributing

Contributions are welcome! Here's how:

1. Fork the repository
2. Create a new branch
```bash
git checkout -b feature/your-feature-name
```
3. Commit your changes
```bash
git commit -m "Add: your feature description"
```
4. Push to GitHub
```bash
git push origin feature/your-feature-name
```
5. Open a **Pull Request**

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 👨‍💻 Author

**Daniel Joshua**
🔗 [GitHub](https://github.com/Danieljoshua720)

---

> ⚠️ **Disclaimer:** This application is built for **educational purposes only**.
> It is **not** a substitute for professional medical diagnosis or advice.
