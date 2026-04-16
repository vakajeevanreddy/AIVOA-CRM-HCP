# AIVOA CRM HCP

AI-powered CRM application for documenting Healthcare Professional (HCP) interactions.  
This project includes a **React frontend** and a **Python backend**.

---

## 🚀 Features
- Frontend built with React + Vite
- Backend powered by Python (FastAPI/Flask)
- AI Assistant component for interaction logging
- Redux state management
- Clean project structure with `.gitignore` to exclude dependencies

---

## 📂 Project Structure
AIVOA/
│
├── Front_end/        # React frontend
│   ├── Components/   # UI components (AIAssistant, InteractionForm, Chatbox)
│   ├── pages/        # Page-level views
│   ├── Redux/        # State management
│   ├── app.jsx
│   ├── main.jsx
│   ├── package.json
│   └── vite.config.js
│
├── Back_end/         # Python backend
│   ├── main.py / server.py
│   └── requirements.txt
│
├── .gitignore
├── README.md
└── start_backend.bat


---

## ⚙️ Setup Instructions

### Frontend (React + Vite)
```bash
cd Front_end
npm install
npm run dev


cd Back_end
python -m venv .venv
.\.venv\Scripts\activate
pip install -r requirements.txt
python start_backend.bat
