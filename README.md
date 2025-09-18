# 📺 Context-Aware Amazon Fire TV Recommendation System

A **context-aware movie recommendation engine** for Fire TV that combines:
- **AWS Comprehend** for mood detection  
- **Contextual Multi-Armed Bandit algorithms** for personalized learning  
- **Real-time feedback loops** for continuous improvement  

---

## 🚀 Features
- 🎭 Context understanding (mood, intent, sub-intent, weather, time of day)  
- 🧠 Bandit algorithm with exploration vs exploitation  
- 🔄 Real-time feedback learning  
- 🎙️ Voice and text-based interaction  
- 📊 JSON/Firebase data storage  

---

## 🏗️ System Architecture
```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │    Backend      │    │   Data Layer    │
│   (React)       │◄──►│   (Flask)       │◄──►│   (JSON/Firebase)│
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         ▼                       ▼                       ▼
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│ • User Interface│    │ • Context Gen   │    │ • movies.json   │
│ • Voice Input   │    │ • Bandit Logic  │    │ • bandit_stats  │
│ • Search        │    │ • AWS Comprehend│    │ • training_data │
│ • Navigation    │    │ • Firebase Log  │    │ • feedback.json │
└─────────────────┘    └─────────────────┘    └─────────────────┘


```
---
## 📂 Project Structure


```text
project-root/
├── backend/
│   ├── api.py               # Flask backend
│   ├── utils/               # Context generation & bandit logic
│   ├── movies.json          # Movie catalog
│   ├── bandit_stats.json    # Bandit algorithm state
│   └── feedback.json        # User feedback logs
│
├── frontend/
│   ├── src/
│   │   ├── App.js           # React app
│   │   ├── components/      # UI components
│   │   └── services/        # API calls
│
└── README.md

```

---

## ⚙️ Installation & Setup

### 1. Clone Repository
```bash
git clone https://github.com/SaiSiriChandana/context-aware-firetv-recommender.git
cd context-aware-firetv-recommender
```

### 2. Backend Setup (Flask + Python)
```bash
cd backend
pip install -r requirements.txt
python api.py
```
Backend runs on [http://localhost:5000](http://localhost:5000)  

### 3. Frontend Setup (React)
```bash
cd frontend
npm install
npm start
```
Frontend runs on [http://localhost:3000](http://localhost:3000) 

---
## 🧠 How It Works

- User provides input (mood, intent, optional sub-intent, voice/text).
- Backend generates context key: Mood|Intent|SubIntent|Weather|Time.
- Bandit algorithm decides:
  - Exploitation → best past-performing movie
  - Exploration → random pick for learning
- User feedback updates bandit_stats.json in real-time.

---

## 🏆 Conclusion
This system goes **beyond basic filtering** by combining **context-awareness, adaptive exploration, and real-time learning** to deliver a **personalized entertainment experience** on Fire TV.

> 📌 Built during **Amazon HackOn Season 5**

---
