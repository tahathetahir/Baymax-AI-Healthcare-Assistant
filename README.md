# Baymax: Your Personal Health Assistant

Baymax is an AI-powered medical assistant that bridges underprivileged patients to credible medical advice. From symptom description to personalized treatment, all within a single session.

---

## Group Members

| Name | Roll Number |
|---|---|
| Muhammad Taha Tahir | 24L-0677 |
| Rehan Farooq But | 24L-0674 |
| Sheikh Ahsan Omer | 24L-3062 |

---

## Motivation

Healthcare has become a luxury. Austerity cuts, remote living, and overwhelmed appointment systems prevent millions from accessing quality medical advice. Baymax bridges this gap by delivering credible, personalized medical guidance powered by AI.

---

## Objectives

Baymax is designed to diagnose across **41+ diseases** from the Kaggle symptom-disease dataset with probabilistic confidence scores. It predicts a **dynamic severity score (0 to 10)** that varies based on patient vitals, age, and medical history. It generates **personalized treatment plans** optimized per patient profile rather than retrieved from a fixed lookup, and maintains a **medical log** for returning patients across sessions.

---

## Modules

### 1. Conversation Module
Engages the patient in a friendly, guided conversation to learn about their condition. It collects symptoms, age, name, and medical history on the first visit. For returning users, only the name is needed and the history is retrieved automatically.

### 2. Diagnosis Module
Uses a trained **Artificial Neural Network (ANN)** to map symptoms to diseases. It returns the top 3 most likely diseases along with a confidence score for each, giving a probabilistic picture rather than a rigid single answer.

### 3. Severity Assessment Module
Employs **Simple Linear Regression** to predict a severity index from 0 to 10. The score shifts dynamically based on symptoms, age, vitals, and medical history. A 70-year-old and a 22-year-old presenting the same symptoms will receive measurably different scores.

### 4. Treatment Recommendation Module
Uses **Genetic Algorithms** to produce an optimized, personalized treatment plan covering medication, remedial workout, and diet. The plan is evaluated across compatibility, effectiveness, workout suitability, diet efficacy, and alignment with the patient's severity level.

### 5. Health Report Module
Generates a comprehensive end-of-session health report. Baymax explains the diagnosed condition in plain, accessible language and interacts with the user in a consoling and comforting tone throughout.

### 6. User Interface Module
Built with **React**, the interface lets users interact with all Baymax modules visually and displays diagnosis results, severity scores, and treatment plans in a clean, readable layout.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React |
| Diagnosis Model | Artificial Neural Network (ANN) |
| Severity Prediction | Simple Linear Regression |
| Treatment Optimization | Genetic Algorithm |
| Dataset | Kaggle Symptom-Disease Dataset (41+ diseases) |

---

## Getting Started

### Prerequisites
- Node.js and npm
- Python 3.x
- Required Python packages (see `requirements.txt`)

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/baymax.git
cd baymax

# Install frontend dependencies
cd client
npm install

# Install backend dependencies
cd ../server
pip install -r requirements.txt
```

### Running the App

```bash
# Start the backend
python app.py

# Start the frontend
cd client
npm start
```

---

## Project Structure

```
baymax/
├── client/                  # React frontend
│   └── src/
│       ├── components/      # UI components
│       └── pages/           # App pages
├── server/                  # Backend logic
│   ├── conversation/        # Conversation module
│   ├── diagnosis/           # ANN diagnosis model
│   ├── severity/            # Linear regression model
│   ├── treatment/           # Genetic algorithm module
│   └── report/              # Health report generator
├── datasets/                # Kaggle symptom-disease dataset
└── README.md
```

---

## Disclaimer

Baymax is an academic project and is **not a substitute for professional medical advice**. Always consult a licensed healthcare provider for medical decisions.
