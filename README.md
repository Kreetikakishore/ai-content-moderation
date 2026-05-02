# 🛡️ AI Content Moderation System

> A machine learning-powered web application that detects and filters toxic or harmful text in real time using NLP, Scikit-learn, and a FastAPI deployed backend.

---

## 📸 Demo

**Input — Text Entry:**

![Input](https://raw.githubusercontent.com/Kreetikakishore/ai-content-moderation/main/assets/input.png)

**Output — Moderation Result:**

![Output](https://raw.githubusercontent.com/Kreetikakishore/ai-content-moderation/main/assets/dashboard.png)

---

## 📌 Executive Summary

User-generated content on digital platforms carries significant risk of harassment, hate speech, and toxic behavior. Manual moderation at scale is neither efficient nor scalable.

This project builds an **end-to-end AI content moderation pipeline** that:

- Trains a machine learning model on real toxic comment data
- Deploys the model as a REST API using FastAPI
- Provides a simple frontend interface for real-time predictions
- Automates harmful content detection with high precision

---

## 🧠 How It Works

1. User enters text in the frontend interface
2. Request is sent to the FastAPI backend
3. Backend loads the trained model (`.pkl`)
4. Text is vectorized using TF-IDF
5. Model predicts whether content is **Toxic** or **Safe**
6. Result is instantly returned to the UI

---

## 📊 Model Details

| Property | Detail |
|----------|--------|
| Algorithm | Logistic Regression |
| Text Representation | TF-IDF Vectorizer |
| Classification Type | Binary (Safe / Toxic) |
| Evaluation Metrics | Precision, Recall, F1-Score |
| Model Format | Joblib `.pkl` |

---

## 🧰 Technology Stack

| Tool | Role |
|------|------|
| Python | Core programming |
| FastAPI | REST API backend |
| Uvicorn | ASGI server |
| Scikit-learn | ML model training |
| Pandas & NumPy | Data processing |
| TF-IDF Vectorizer | Text feature extraction |
| Joblib | Model saving & loading |
| HTML | Frontend interface |

---

## ⚙️ Model Training Approach

- Combined multiple toxicity labels into a unified severity score
- Converted into binary classification:
  - `0` → Safe
  - `1` → Toxic
- Applied TF-IDF vectorization for text representation
- Trained Logistic Regression with optimized hyperparameters
- Evaluated using full classification report

---

## 📂 Repository Structure

```
ai-content-moderation/
│
├── data/
│   └── train.csv
│
├── model/
│   ├── train.py
│   └── moderation_model.pkl
│
├── frontend/
│   └── index.html
│
├── assets/
│   ├── input.png
│   └── dashboard.png
│
├── app.py
├── requirements.txt
└── README.md
```

---

## 🚀 How to Run Locally

### 1. Clone Repository

```bash
git clone https://github.com/Kreetikakishore/ai-content-moderation.git
cd ai-content-moderation
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Train the Model (optional)

```bash
python model/train.py
```

### 4. Run FastAPI Server

```bash
uvicorn app:app --reload
```

### 5. Open in Browser

```
http://127.0.0.1:8000
```

---

## 🌍 Real-World Applications

- Social media comment moderation
- Online gaming chat filtering
- Community platform safety
- Customer review screening
- Forum and blog moderation

---

## 📈 Key Impact

- ✅ Automated detection of harmful content at scale
- ✅ Reduced manual moderation effort significantly
- ✅ Real-time prediction via REST API
- ✅ Easily integrable into any platform

---

## 💡 Future Improvements

- Integrate advanced transformer models like **BERT**
- Add multi-class classification for toxicity types
- Deploy on cloud platforms (AWS / Render / Railway)
- Add user authentication and API key management
- Build a monitoring dashboard for moderation logs

---

## ⚠️ Note

This project was developed as an AI and NLP portfolio case study to demonstrate end-to-end machine learning deployment, text classification, and API development skills.

---

## 👤 Author

**Kreetika Kishore**
Data Analytics & AI Portfolio Project | 2026
