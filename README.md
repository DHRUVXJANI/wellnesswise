# 🩺 WellnessWise — Intelligent Medical Decision Support System

**WellnessWise** is a smart, web-based medical decision support platform designed to assist users in identifying possible health conditions based on symptoms and personal health factors such as age, gender, and pregnancy status. Powered by machine learning, the system delivers structured disease insights, treatment guidance, comorbidity awareness, and lifestyle recommendations — making it valuable for learning, early self-assessment, and health awareness.

> ⚠️ **Disclaimer:** WellnessWise is intended strictly for *educational and informational purposes*. It does **not** provide medical diagnosis or replace professional healthcare advice, consultation, or treatment.

---

## ✨ Key Features

### 🔎 Symptom Intelligence

* Predict potential diseases using natural-language symptom input or structured selections.
* Machine-learning powered symptom similarity and classification pipeline.

### 📊 Personalized Health Filtering

* Results tailored using demographic context:

  * Age
  * Gender
  * Pregnancy status

### 📈 Comprehensive Disease Profiles

Each disease prediction includes:

* Treatment protocols
* Medication insights
* Comorbidity considerations
* Safety precautions
* Educational summaries

### 🏃 Lifestyle Guidance

* Disease-specific diet recommendations
* Workout and wellness suggestions.

### 🏷 Organized Disease Categories

* Browse conditions grouped by medical system (respiratory, endocrine, psychiatry, etc.).

### 🔐 Secure User Authentication

* Signup/login system using Flask + SQLite.
* Session-based authentication.

### 🎨 Responsive Interface

* Clean UI optimized for both desktop and mobile.

---

## 🖼️ Application Screenshots

### 🏠 Home & Disease Categories

![Home Page]<img width="1851" height="924" alt="Screenshot 2025-04-12 152508" src="https://github.com/user-attachments/assets/e10f74a5-e164-4335-abcb-7c2c3c21876c" />


### 🧾 Symptom Checker Interface

![Symptom Checker]<img width="1840" height="923" alt="Screenshot 2025-04-12 152642" src="https://github.com/user-attachments/assets/6b0c750b-a41f-46ea-8cdd-76b744bb3ba6" />
420.png)

### 📊 Prediction Results & Disease Insights

![Search Results]<img width="1839" height="920" alt="Screenshot 2025-04-12 152805" src="https://github.com/user-attachments/assets/83d59ece-3c89-44e5-bce1-8bd58eceaba8" />


### 🩺 Detailed Disease Recommendation View

![Detailed Result]<img width="984" height="821" alt="Screenshot 2025-04-12 152915" src="https://github.com/user-attachments/assets/447578f2-63d8-450f-b81e-998ca9c16c83" />
<img width="981" height="822" alt="Screenshot 2025-04-12 152931" src="https://github.com/user-attachments/assets/457a2054-800d-4e89-a219-3e884c8c7623" />


---

## 🛠️ Tech Stack

**Backend**

* Python
* Flask

**Machine Learning**

* Scikit-learn
* Pandas
* NumPy
* TF-IDF + Cosine Similarity for symptom mapping
* Multinomial Naive Bayes for disease prediction

**Frontend**

* HTML
* CSS
* Jinja2 Templates

**Database**

* SQLite
* SQLAlchemy ORM

**Dataset**

* `augmented_diseases_extended.csv`
  Curated dataset containing symptoms, diseases, treatments, comorbidities, and lifestyle data.

---

## 📁 Project Structure

```
WellnessWise/
├── app.py
├── model.py
├── models.py
├── Models.ipynb
├── augmented_diseases_extended.csv
├── templates/
├── static/
├── Model Details/
├── requirements.txt
└── README.md
```

---

## 🚀 Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone <repo-url>
cd WellnessWise
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

If missing:

```bash
pip install flask pandas scikit-learn numpy
```

### 3️⃣ Verify Dataset

Ensure:

```
augmented_diseases_extended.csv
```

exists in the root directory.

### 4️⃣ Run the App

```bash
python app.py
```

Open:

```
http://localhost:5000
```

(Optional) Use `Models.ipynb` for model experimentation.

---

## 🧪 How to Use

1. Launch the web application.
2. Select symptoms from dropdown menus.
3. Provide age, gender, and pregnancy status.
4. View:

   * Predicted diseases with match scores
   * Comorbidities & precautions
   * Treatment and lifestyle guidance

---

## 👨‍💻 Authors

**Mahipal Chauhan**
**Dhruv Jani**
B.Tech CSE — Batch 2022–2026

---

## 📜 License

© 2025 Dhruv Jani and Mahipal Chauhan.
All rights reserved.

Unauthorized use, reproduction, modification, or distribution is strictly prohibited without explicit permission from the authors.
