# AIVOA CRM — AI-Powered HCP Interaction Dashboard

A modern CRM application for managing Healthcare Professional (HCP) interactions using AI-powered natural language extraction.

## ✨ Features

- **AI Assistant** — Describe a medical interaction in natural language and the AI extracts structured fields automatically
- **Smart Field Mapping** — Handles LLM variations (e.g., "doctor" → `hcp_name`, "hospital" → `organization`)
- **16 Interaction Fields** — HCP name, specialty, organization, product focus, interaction type, date, time, attendees, topics discussed, voice summary, sentiment, follow-up actions, materials shared, samples distributed, suggested references, observation
- **Modern Dark UI** — Premium glassmorphism design with smooth animations
- **Interaction History** — View all saved interactions with sentiment badges

## 🛠 Tech Stack

| Layer    | Technology |
|----------|-----------|
| Frontend | React 18 + Vite |
| Backend  | FastAPI + SQLAlchemy |
| Database | SQLite (default) / MySQL (optional) |
| AI/LLM   | Groq (Llama 3.3 70B) with regex fallback |

## 🚀 Quick Start

### Prerequisites
- Python 3.10+
- Node.js 18+
- Groq API key ([get one free](https://console.groq.com))

### Backend Setup
```bash
cd Back_end
pip install -r requirements.txt

# Create .env file
echo GROQ_API_KEY=your_groq_api_key_here > .env

# Start the server
python -m uvicorn main:app --reload --port 8000
```

### Frontend Setup
```bash
cd Front_end
npm install
npm run dev
```

Open http://localhost:5173 in your browser.

## 📁 Project Structure

```
Pyndatic/
├── Back_end/
│   ├── main.py              # FastAPI app entry point
│   ├── db/
│   │   ├── database.py      # SQLAlchemy engine + session
│   │   └── schemas.py       # Pydantic schemas
│   ├── models/
│   │   └── interaction.py   # SQLAlchemy Interaction model
│   ├── routes/
│   │   ├── ai_routes.py     # /ai-assistant endpoint
│   │   └── interaction_routes.py  # CRUD endpoints
│   ├── services/
│   │   ├── langgraph_agent.py  # Intent routing + agent
│   │   ├── llm_service.py     # Groq LLM wrapper
│   │   └── log_tool.py        # NLP extraction tool
│   └── requirements.txt
├── Front_end/
│   ├── index.html
│   ├── main.jsx
│   ├── app.jsx              # Dashboard layout + key mapping
│   ├── styles.css           # Modern dark theme
│   ├── Components/
│   │   ├── AIAssistant.jsx  # Chat interface
│   │   ├── InteractionForm.jsx  # Form with glassmorphism cards
│   │   └── interactionhistory.jsx  # History list
│   └── package.json
└── .gitignore
```

## 📝 License

MIT
