# WellnessWise

<div align="center">

**Intelligent Medical Decision Support System**

[![License: All Rights Reserved](https://img.shields.io/badge/License-Proprietary-blue.svg)](LICENSE)
[![Python 3.8+](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Flask](https://img.shields.io/badge/Flask-2.0+-green.svg)](https://flask.palletsprojects.com/)

[About](#about) • [Features](#features) • [Installation](#installation) • [Usage](#usage) • [Tech Stack](#tech-stack)

</div>

---

## About

WellnessWise is an intelligent, web-based medical decision support platform that leverages machine learning to assist users in identifying potential health conditions based on symptom analysis and demographic factors. The system provides structured disease insights, treatment guidance, comorbidity awareness, and personalized lifestyle recommendations.

> **⚠️ Disclaimer:** WellnessWise is intended strictly for **educational and informational purposes**. It does **not** provide medical diagnosis or replace professional healthcare advice, consultation, or treatment. Always consult a qualified healthcare professional for medical concerns.

---

## Features

### 🔍 Intelligent Symptom Analysis
- Natural language symptom input with machine learning classification
- TF-IDF vectorization for semantic symptom matching
- Multinomial Naive Bayes classifier for disease prediction
- Interpretable results with confidence scoring

### 👤 Personalized Health Insights
- Demographic-aware predictions (age, gender, pregnancy status)
- Tailored disease recommendations based on user context
- Improved accuracy and relevance compared to generic symptom checkers

### 📋 Comprehensive Disease Profiles
Each disease recommendation includes:
- Treatment protocols and medication guidance
- Comorbidity considerations and drug interactions
- Safety precautions and contraindications
- Educational summaries for patient awareness

### 🏥 Lifestyle & Wellness Guidance
- Disease-specific dietary recommendations
- Personalized exercise and wellness suggestions
- Preventive health measures

### 🗂️ Organized Disease Database
- Conditions grouped by medical system (respiratory, endocrine, cardiovascular, etc.)
- Easy browsing and exploration
- Structured medical knowledge repository

### 🔐 Secure User Management
- User registration and authentication
- Session-based security
- SQLite backend with SQLAlchemy ORM

### 📱 Responsive Design
- Clean, modern interface optimized for desktop and mobile
- Intuitive user experience
- Real-time result visualization

---

## Installation

### Prerequisites
- Python 3.8 or higher
- pip package manager
- Git

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd WellnessWise
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
   
   Or manually install core packages:
   ```bash
   pip install flask pandas scikit-learn numpy
   ```

4. **Verify dataset**
   Ensure `augmented_diseases_extended.csv` exists in the root directory

5. **Run the application**
   ```bash
   python app.py
   ```
   
   Open your browser and navigate to `http://localhost:5000`

---

## Usage

### Basic Workflow

1. **Register or Log In**
   - Create a new account or sign in with existing credentials

2. **Input Symptoms**
   - Select symptoms from dropdown menus
   - Provide demographic information (age, gender, pregnancy status)

3. **View Results**
   - Review predicted diseases with match scores
   - Examine comorbidities and precautions
   - Access treatment and lifestyle guidance

### Example

```
Input:
- Symptoms: fever, cough, fatigue
- Age: 35
- Gender: Female
- Pregnancy Status: Not pregnant

Output:
- Top predictions: Influenza, Common Cold, COVID-19
- Match scores, treatment options, and lifestyle recommendations
```

---

## Tech Stack

| Component | Technology |
|-----------|-----------|
| **Backend** | Python, Flask |
| **Machine Learning** | Scikit-learn, Pandas, NumPy |
| **NLP** | TF-IDF Vectorization, Cosine Similarity |
| **Algorithm** | Multinomial Naive Bayes Classifier |
| **Frontend** | HTML5, CSS3, Jinja2 Templates |
| **Database** | SQLite, SQLAlchemy ORM |
| **Dataset** | `augmented_diseases_extended.csv` |

---

## Project Structure

```
WellnessWise/
├── app.py                              # Flask application entry point
├── model.py                            # Machine learning model implementation
├── models.py                           # Database models (SQLAlchemy)
├── Models.ipynb                        # Jupyter notebook for model experimentation
├── augmented_diseases_extended.csv     # Disease and symptom dataset
├── requirements.txt                    # Python dependencies
├── templates/                          # HTML templates
│   ├── index.html
│   ├── login.html
│   ├── signup.html
│   ├── symptom_checker.html
│   └── results.html
├── static/                             # Static assets (CSS, JavaScript, images)
│   └── style.css
├── Model Details/                      # Model documentation and analysis
├── README.md                           # This file
└── LICENSE                             # License information
```

---

## Screenshots

### Signup/Login Page
<img width="1841" height="926" alt="Screenshot 2025-04-12 152228" src="https://github.com/user-attachments/assets/452c0b38-8821-450d-8b2a-b4b4f5aaf8e7" />
<img width="1840" height="920" alt="Screenshot 2025-04-12 152341" src="https://github.com/user-attachments/assets/33910020-6d45-4e51-b254-65f778e44ca0" />


### Home Page
<img width="1900" height="929" alt="wellness-wise" src="https://github.com/user-attachments/assets/70597c69-70ed-47d0-bd3a-ef2a0bcbe329" />

### Symptom Checker Interface
<img width="1412" height="832" alt="Screenshot 2025-04-19 103420" src="https://github.com/user-attachments/assets/c5aa6e90-b216-4d09-8840-73d273fedace" />

### Prediction Results
<img width="1449" height="917" alt="Screenshot 2025-04-19 103454" src="https://github.com/user-attachments/assets/d7e22558-05b6-4a95-9f07-bcc4f62ceb82" />

### Detailed Disease Insights
<img width="984" height="821" alt="Screenshot 2025-04-12 152915" src="https://github.com/user-attachments/assets/34434feb-e191-45ef-96fe-dbd8758b43aa" />

---

## System Architecture

### Symptom Processing Pipeline

```
User Input → Normalization → TF-IDF Vectorization → Similarity Matching
```

### Disease Prediction Pipeline

```
Symptom Vectors → Naive Bayes Classifier → Disease Scores → Ranking
```

### Personalization Layer

```
Demographics (Age/Gender/Pregnancy) → Context Filtering → Refined Results
```

### Knowledge Integration

```
Disease ID → Treatment Data → Comorbidities → Lifestyle Recommendations
```

---

## Dataset

The system uses an augmented, curated dataset containing:
- **Diseases:** Comprehensive disease profiles across medical specialties
- **Symptoms:** Associated symptoms with relevance weights
- **Treatments:** Evidence-based treatment protocols and medications
- **Comorbidities:** Drug interactions and disease correlations
- **Lifestyle Data:** Diet and exercise recommendations

---

## Model Details

### Algorithm: Multinomial Naive Bayes

- **Why:** Fast inference, interpretable results, suitable for multi-class disease classification
- **Input:** TF-IDF vectorized symptom features
- **Output:** Probability scores for each disease
- **Training:** Supervised learning on symptom-disease pairs

### Feature Engineering

- **TF-IDF Vectorization:** Semantic similarity between user input and known symptoms
- **Cosine Similarity:** Measures closeness of symptom vectors
- **Demographic Weighting:** Adjusts predictions based on age, gender, and pregnancy status

---

## How It Works

1. **User enters symptoms** via natural language or structured selection
2. **Symptoms are normalized** and converted to TF-IDF vectors
3. **Machine learning model** predicts probable diseases with confidence scores
4. **Demographic context** refines predictions for increased relevance
5. **System retrieves** comprehensive medical information for top results
6. **Educational summaries** are presented alongside treatment guidance

---

## Limitations & Disclaimers

- **Educational Purpose Only:** This system provides informational support, not medical diagnosis
- **Not a Substitute for Professional Care:** Always consult qualified healthcare providers
- **Limited by Data:** Predictions based on curated dataset; rare conditions may be underrepresented
- **Demographic Bias:** System trained on specific populations; results may vary across groups
- **No Emergency Support:** Do not use for acute medical emergencies

---

## Contributing

This project is proprietary software. For inquiries regarding contributions, modifications, or licensing, please contact the authors.

---

## Authors

**Mahipal Chauhan** | **Dhruv Jani**

B.Tech Computer Science Engineering  
Batch 2022–2026

---

## License

© 2025 Dhruv Jani and Mahipal Chauhan. All rights reserved.

Unauthorized use, reproduction, modification, or distribution is strictly prohibited without explicit written permission from the authors.

For licensing inquiries, please contact the authors directly.

---

## Support & Feedback

For bug reports, questions, or suggestions, please reach out to the authors.

---

<div align="center">

**Disclaimer:** This system is for educational purposes only and should never replace professional medical consultation.

</div>
