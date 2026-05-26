# EICONO 💰⚡
### *AI-Powered Personal Finance Customer Care Bot*
### Flowzint AI Hackathon 2026 — Customer Care Bot Track

> Turning confused savers into confident investors — powered by Gemini AI.

**Built by Palash**

---

## 🎯 Problem Statement

**95% of Indians lack a proper financial plan.** Financial advisors charge ₹25,000+/year and only serve HNIs. Retail investors make decisions based on social media tips, fear, and gut instinct — leading to poor outcomes and eroded trust.

**EICONO** solves this by being an always-on, intelligent financial customer care bot that can be embedded in any fintech platform. It answers complex financial queries, generates personalized advice, analyzes portfolios, runs retirement simulations, and optimizes taxes — instantly and for free.

---

## ✨ Track: Customer Care Bot

| Metric | Our Approach |
|---|---|
| **Model Innovation (30%)** | Multi-modal AI: voice chat + PDF analysis + Monte Carlo simulations + step-up SIP modeling via Gemini 1.5 Flash |
| **Real-World Applicability (25%)** | Directly addresses India's ₹40 trillion retail investor market |
| **Technical Architecture (25%)** | FastAPI backend + React/Vite SPA, 12 REST endpoints, Vercel-deployable, zero heavy ML dependencies |
| **Documentation Clarity (20%)** | Comprehensive README, OpenAPI docs at `/docs`, architecture diagram |

---

## 🧠 12 AI-Powered Features

| # | Feature | Description |
|---|---|---|
| 1 | **💬 AI Money Mentor** | Voice-first WhatsApp-style chat with Gemini AI — instant, actionable financial advice |
| 2 | **📊 Money Health Score** | 6-dimension financial wellness score (Emergency Fund, Savings, Investments, Debt, Diversification, Goals) |
| 3 | **🔬 Portfolio X-Ray** | Upload CAMS/KFintech PDF → AI extracts fund overlap, sector exposure & asset allocation |
| 4 | **📈 Monte Carlo Simulator** | 1,000 probabilistic retirement simulations with Indian market volatility |
| 5 | **💰 Tax Wizard** | Old vs New regime comparison with exact ₹ savings and ELSS/NPS recommendations |
| 6 | **👫 Couple's Joint Planner** | India-first tool to optimize combined finances, tax splits & SIP allocation |
| 7 | **🎯 Goal Optimizer** | AI-powered goal tracking with actionable milestone planning |
| 8 | **⚠️ Risk Alerts** | Behavioral finance nudges with market-aware recommendations |
| 9 | **💳 Expense Tracker** | AI-categorized expense breakdown with 50/30/20 budget adherence scoring |
| 10 | **📈 SIP Growth Engine** | Step-up SIP modeling with inflation-adjusted returns — see how ₹5K/month becomes ₹2 Cr |
| 11 | **🛡️ Insurance Gap Finder** | HLV-method Life & Health cover analysis — identifies under-insurance risk instantly |
| 12 | **🔓 Debt Freedom Plan** | Avalanche vs Snowball comparison with exact payoff timeline & interest savings |

---

## 🛠️ Tech Stack

**Frontend**
- React 18 + Vite 6
- Tailwind CSS v4 + Radix UI
- Recharts + Framer Motion
- React Router v7
- Web Speech API (voice input/output)
- Vercel-deployable

**Backend**
- FastAPI + Python 3.10+
- Uvicorn (ASGI server)
- **Google Gemini 1.5 Flash** (AI engine)
- NumPy (Monte Carlo simulations)
- PyPDF2 (PDF parsing)

**Architecture**
- REST API with OpenAPI docs (`/docs`)
- CORS-enabled for frontend integration
- Stateless, serverless-ready design
- 12 API endpoints

---

## 🚀 Quick Start

### Prerequisites
- Python 3.10+
- Node.js 18+
- A free [Google AI Studio](https://aistudio.google.com/) API key

### 1. Clone & Setup Backend

```bash
cd backend
python -m venv venv
# Windows
venv\Scripts\activate
# Mac/Linux
source venv/bin/activate

pip install -r requirements.txt
cp .env.example .env
# Edit .env and add your GEMINI_API_KEY

uvicorn main:app --reload --port 8000
```

Backend → **http://localhost:8000** | API Docs → **http://localhost:8000/docs**

### 2. Setup Frontend

```bash
cd frontend
npm install
npm run dev
```

Frontend → **http://localhost:5173**

### 3. Deploy to Vercel (Frontend)

```bash
cd frontend
npx vercel
```

---

## 📁 Project Structure

```
EICONO/
├── backend/
│   ├── main.py              ← FastAPI app with 12 AI endpoints
│   ├── requirements.txt     ← Python dependencies (9 packages)
│   ├── .env.example         ← Environment template
│   └── .gitignore
├── frontend/
│   ├── src/
│   │   ├── app/
│   │   │   ├── components/  ← LandingPage, Dashboard, AIMentor, etc.
│   │   │   ├── context/     ← UserDataContext
│   │   │   ├── App.tsx      ← Landing → Onboarding → Dashboard flow
│   │   │   └── routes.ts
│   │   ├── services/
│   │   │   └── api.ts       ← Backend API client
│   │   └── main.tsx
│   ├── vercel.json          ← Vercel deployment config
│   ├── package.json
│   └── vite.config.ts
├── ARCHITECTURE.md
├── IMPACT.md
└── README.md
```

---

## 🌐 API Reference (12 Endpoints)

| Endpoint | Method | Description |
|---|---|---|
| `/` | GET | Health check + metadata |
| `/api/health` | GET | Service health status |
| `/chat` | POST | AI financial advice chat |
| `/health-score` | POST | 6-dimension Money Health Score |
| `/portfolio-xray` | POST | PDF portfolio analysis |
| `/monte-carlo` | POST | Retirement simulation |
| `/tax-wizard` | POST | Old vs New regime tax calculator |
| `/couple-planner` | POST | Joint finance optimizer |
| `/expense-tracker` | POST | 50/30/20 budget analysis |
| `/sip-growth` | POST | Step-up SIP projection |
| `/insurance-gap` | POST | Life & Health cover gap analysis |
| `/debt-freedom` | POST | Avalanche vs Snowball payoff |

Full interactive docs: **http://localhost:8000/docs**

---

## 👤 Author

**Palash** — Built with ❤️ for Flowzint AI Hackathon 2026

## 📄 License

MIT License — free to use and build upon.
