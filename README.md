# GuardianSMS — SMS Spam Detection System

A machine learning-powered SMS spam detection system built with Python and Flask, achieving **97.58% accuracy** using Multinomial Naive Bayes.

> Semester Project — COMSATS University Islamabad, Wah Campus
> Eman Zahra & Uneeza Kamran | Supervisor: Dr. Sulma Rashid

---

## Features

- Real-time SMS spam detection with threat percentage scoring
- Bulk scanner for multiple messages at once
- Side-by-side message comparison
- URL, urgency, money, and phishing keyword detection
- Scan history saved in browser
- PDF report export
- Live threat intelligence feed
- Dark / Light theme toggle

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Python, Flask |
| ML Model | Scikit-learn — Multinomial Naive Bayes + TF-IDF |
| Dataset | UCI SMS Spam Collection (5,572 messages) |
| Frontend | HTML, CSS, JavaScript, Chart.js |

---

## Model Performance

| Metric | Result |
|--------|--------|
| Accuracy | 97.58% |
| Precision | 98.41% |
| Recall | 83.22% |
| F1-Score | 90.18% |

---

## Getting Started

**1. Clone the repository**
```bash
git clone https://github.com/your-username/guardiansms.git
cd guardiansms
```

**2. Install dependencies**
```bash
cd backend
python -m pip install -r requirements.txt
```

**3. Train the model**
```bash
python model_trainer.py
```

**4. Start the API server**
```bash
python app.py
```

**5. Open the frontend**

Open `frontend/index.html` in your browser. The API will be running at `http://localhost:5000`.

---

## API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/predict` | POST | Scan a single SMS message |
| `/bulk-predict` | POST | Scan multiple messages at once |
| `/health` | GET | Check API status |

---

## Example Results

| Message | Result | Threat Level |
|---------|--------|-------------|
| "Don't forget groceries" | ✅ SAFE | Low (5%) |
| "You won $1000 prize" | 🚨 SPAM | High (92%) |
| "Bank account suspended" | 🚨 SPAM | Critical (98%) |
| "Meeting at 3pm" | ✅ SAFE | Low (8%) |

---

## License

This project was developed for academic purposes at COMSATS University Islamabad, Wah Campus.

