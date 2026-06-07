# ARGUS - Prompt-to-Simulation Lunar Mission Intelligence

<div align="center">
  <img src="Argus/images/argus_logo.png" alt="ARGUS Logo" width="200" onerror="this.style.display='none'"/>
  <br/>
  <h3>FAR AWAY · 2026 INDIA'S BIGGEST INTERNATIONAL HACKATHON</h3>
  <p><b>Theme 4: Space & Aerospace - "Push the boundaries of space technology and aerospace innovation."</b></p>
</div>

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Next.js 16](https://img.shields.io/badge/Next.js-16-black)](https://nextjs.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.110+-green.svg)](https://fastapi.tiangolo.com/)

**ARGUS** transforms natural language mission descriptions into validated, simulation-verified lunar mission plans. Built for **Theme 4: Space & Aerospace**, ARGUS democratizes and accelerates aerospace engineering by bridging the gap between mission intent and physical execution. 

---

## 🚀 The Vision: Theme 4 (Space & Aerospace)

The aerospace sector is historically slow, siloed, and opaque. Mission intent is formulated in documents, translated manually by engineers, and validated in disconnected tools. 
**ARGUS pushes the boundaries of space technology** by creating a unified **"prompt-to-simulation" pipeline**.

By integrating **Agentic LLMs**, **Computer Vision**, **Physics Validation**, and **3D Digital Twins**, we've built a system where a single operator can design, validate, and simulate a safe lunar rover mission in seconds, rather than weeks.

## 🌟 How We Meet the Judging Criteria

- **Innovation & Technical Depth:** We combine LLM-based intent parsing (Google Gemini) with rigorous physics-based constraint validation and SegFormer-based terrain analysis. We don't just trust the AI; we verify it.
- **Engineering Quality:** A scalable split architecture featuring a high-performance Python/FastAPI backend and a React/Next.js frontend with declarative 3D rendering (React Three Fiber + Rapier physics).
- **Real-World Impact:** Significantly reduces the time and cost of the mission planning phase, allowing operators to iteratively test hypotheses without risking physical assets.
- **Design & User Experience:** An intuitive "mission console" allows operators to simply type what they want (e.g., "Send 1 rover to Green Peaks, avoid steep slopes"), watch the AI plan it, and instantly view the 3D replay.

---

## 📖 What is ARGUS?

ARGUS is a unified mission intelligence platform that:

1. **Parses** natural language mission descriptions into structured parameters.
2. **Analyzes** synthetic and real terrain to identify safe landing zones.
3. **Validates** mission feasibility against physics constraints (slopes, battery, distance).
4. **Replans** automatically if safety violations are detected.
5. **Simulates** the mission in a 3D digital twin before execution.

### The Problem We Solve
Current mission planning is **fragmented, slow, and opaque**:
- Intent is written in text, but planning happens in separate tools.
- Validation occurs late, after significant investment.
- AI-generated plans lack explainability and trust.

### Our Solution
**Unified Pipeline:** Prompt → Parse → Validate → Simulate in one workflow  
**Explainable AI:** Every decision includes supporting evidence (risk scores, constraint reports, confidence levels)  
**Early Validation:** Physics-based checks and simulation verification before committing resources  

---

## 🛠️ Technology Stack

### Backend (Mission Intelligence)
- **FastAPI** - High-performance async API
- **Google Gemini** - LLM for natural language intent parsing
- **OpenCV + NumPy** - Computer vision for landing zone detection and terrain analysis
- **Python 3.9+** - Scientific computing ecosystem

### Frontend (Simulation & UI)
- **Next.js 16** - React framework with SSR (AreoNET)
- **React Three Fiber & @react-three/rapier** - Declarative 3D rendering and physics engine
- **Tailwind CSS** - Utility-first styling

### AI & Existing Projects
- **IBM Bob (Windsurf AI)** - Our AI pair programming partner (70-80% code contribution, fulfilling the "Builder-first, AI-assisted" hackathon philosophy)
- **HuggingFace SegFormer** - Terrain segmentation
- **Custom Algorithms** - A* pathfinding, landing zone ranking, constraint validation

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                     User Interface (Next.js)                 │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐     │
│  │ Mission Input│  │  3D Simulation│  │   Timeline   │     │
│  │   Console    │  │   (Three.js)  │  │   & Replay   │     │
│  └──────┬───────┘  └──────┬───────┘  └──────┬───────┘     │
└─────────┼──────────────────┼──────────────────┼────────────┘
          │                  │                  │
          ▼                  ▼                  ▼
┌─────────────────────────────────────────────────────────────┐
│              Backend API (FastAPI + Python)                  │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐     │
│  │   Mission    │  │   Landing    │  │   Mission    │     │
│  │    Parser    │→ │   Detector   │→ │  Validator   │     │
│  │  (Gemini LLM)│  │  (OpenCV)    │  │  (Physics)   │     │
│  └──────────────┘  └──────────────┘  └──────┬───────┘     │
│                                              │              │
│                    ┌──────────────┐          │              │
│                    │   Replanner  │←─────────┘              │
│                    │  (Optimizer) │                         │
│                    └──────────────┘                         │
└─────────────────────────────────────────────────────────────┘
```

---

## 🚀 Getting Started

### Prerequisites
- **Python 3.9+**
- **Node.js 18+**
- **Gemini API Key** (Get it free from [Google AI Studio](https://aistudio.google.com/))

### Installation & Running

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd ARGUS
   ```

2. **Backend Setup**
   ```bash
   cd Argus/backend
   pip install -r requirements.txt
   copy .env.example .env
   # Edit .env and add your GEMINI_API_KEY
   ```

3. **Frontend Setup**
   ```bash
   cd AreoNET/AreoNet
   npm install
   ```

4. **Start the Servers (Windows PowerShell Recommended)**
   ```powershell
   # Terminal 1: Start Backend
   .\Argus\start-argus-backend.ps1

   # Terminal 2: Start Frontend
   .\Argus\start-argus-frontend.ps1
   ```

### Access Points
- **Mission Console:** `http://localhost:3001/mission` (main interface)
- **Dashboard:** `http://localhost:3001/dashboard`
- **Backend API Docs:** `http://localhost:8001/docs`

---

## 🎮 Demo Scenarios

Try these prompts in the Mission Console:

1. **Quick Scan:** 
   `"Quick scan of Green Peaks region. Prioritize speed over science."`
   *(Result: Short route, minimal constraints, fast execution)*

2. **Science Mission:**
   `"Detailed investigation of Violet Stones. Collect samples. Avoid steep terrain. Ensure safe return."`
   *(Result: Longer route, strict safety margins, science-optimized path)*

3. **Emergency Return:**
   `"Return to landing zone immediately. Battery critical."`
   *(Result: Shortest safe path, maximum speed, minimal risk)*

---

## 📁 Submission Deliverables

All required submission materials for Round 1 can be found in the `deliverables/` folder:
- **[Problem & Solution Statement](deliverables/PROBLEM_STATEMENT.md)**
- **[Technology Statement](deliverables/TECHNOLOGY_STATEMENT.md)**
- **[IBM Bob Usage Report](deliverables/BOB_USAGE_REPORT.md)** (Required documentation of AI assistance)
- **[Judge Q&A Guide](deliverables/JUDGE_QA_AND_DEMO_GUIDE.md)**

---

## 👥 Team corx4
- **Developer:** Palash Singh Tomar
- **AI Partner:** IBM Bob (Windsurf AI)

*Built for FAR AWAY 2026 - India's Biggest International Hackathon.*
