
 🧠 MindGuard AI – Emotionally Intelligent Mental Health Platform

MindGuard AI is an all-in-one, AI-powered mental wellness platform designed to emulate and enhance psychological support. It integrates intelligent conversational AI, dynamic psychometric assessments, mood tracking, CBT micro-coaching, adaptive insights, and emergency support—all within a beautifully responsive UI/UX optimized for emotional care.

> “More than a product — it’s a vision for the future of mental wellness.”

---
🎥 YouTube Walkthrough:  
🔗 [Watch the Full Demo on YouTube](https://youtu.be/XxIqkEAO3KU)

📂 Project Assets (Video, Screenshots, Reports):  
🔗 [View on Google Drive](https://drive.google.com/file/d/1tqpk6sKnkKx5_eb2TA4CixtvN16Ve85q/view?usp=drive_link)

 🔍 Table of Contents

- [Overview](overview)
- [Features](features)
- [Modules](modules)
- [Tech Stack](tech-stack)
- [Architecture](architecture)
- [Requirements](requirements)
- [Setup & Installation](setup--installation)
  - [Backend Setup](backend-setup)
  - [Frontend Setup](frontend-setup)
- [Deployment](deployment)
- [Testing & Validation](testing--validation)
- [Security & Privacy](security--privacy)
- [License](license)

---

 🧩 Overview

MindGuard AI is a fully interactive system that supports users through daily mental health management. It combines advanced AI models (e.g., GPT-3.5, HuggingFace sentiment/risk models) with real-time feedback loops and visual dashboards to offer personalized, emotion-aware, and actionable psychological support.

---

 🌟 Features

 🔒 Authentication & User Management
- Single-user and multi-user mode support (configurable)
- User profile with UUID, email, preferences, emergency contact
- Anonymous mode support for privacy-first access

 💬 Chatbot + AI Psychologist
- GPT-3.5 based intelligent chatbot with memory
- Real-time emotion, sentiment, and risk analysis (HuggingFace)
- Crisis detection & escalation
- Adaptive conversation flow and CBT technique integration
- Typing indicators, voice input, text-to-speech AI reply
- Emoji reactions, timestamps, sticky headers

 📊 Mood Tracking + Visualization
- Daily mood check-in popup (mood + emotion)
- Weekly mood trend graphs
- Monthly mood heatmap calendar
- Confetti animations & streak tracking

 🧠 Psychometric Testing Engine
- Dynamic triggering (PHQ-9, GAD-7)
- Result interpretation, emotional score mapping
- CBT suggestions based on scores

 🏅 Gamification Engine
- Mood-based badge rewards
- Streak boosters
- Unlockable “Mood Packs” via positive activity

 📈 Dashboard & Emotional Insights
- Weekly reports & chat summaries
- Emotion radar chart
- Risk/resilience dual chart
- Cognitive insight ribbons
- Therapist referral cards
- Micro-journal displays

 ⚠️ Emergency & Risk Escalation
- Emergency Safe Mode UI
- Real-time crisis keyword detection
- High RAS auto-escalation + referral

 🧭 Adaptive Coaching System
- Context-aware AI recommendations
- Emotion→Coaching path mapper
- Micro-surveys & embedded links
- Time-aware adaptive advice engine

---

 🧱 Module Breakdown

| Module | Description |
|--------|-------------|
| 1. Core System | Authentication, user profile, preferences |
| 2. Chat Engine | GPT-based chat, sentiment/emotion/risk AI |
| 3. Mood Tracker | Daily check-in + mood heatmap |
| 4. Psychometric Engine | PHQ-9, GAD-7, auto-analysis |
| 5. Gamification | Badges, streaks, mood confetti |
| 6. Dashboard | Charts, summaries, recommendations |
| 7. Adaptive Coaching | Time-aware AI tips |
| 8. CBT Micro-Coaching | Cognitive distortion detection, reframing UI |
| 9. Cognitive Spike Detection | Emotion spike timeline, risk awareness |
| 10. Emergency System | Escalation UI, contact integration |
| 11. Admin Tools | (Optional) Minimal admin audit page |
| 12. CI & Testing Suite | Cypress, Pytest, Lighthouse |
| 13. Deployment & Hosting | Vercel (frontend), Fly.io / Railway (backend) |

---

 ⚙️ Tech Stack

Frontend:  
- React + Vite  
- Tailwind CSS + Framer Motion  
- Axios, ShadCN, Recharts  
- Headless UI, Lucide Icons  
- PWA + TTS + Web Speech API

Backend:  
- Python + FastAPI  
- PostgreSQL (via SQLAlchemy)  
- OpenAI GPT-3.5 API  
- HuggingFace Transformers  
- Pytest, Locust (for testing)

---

 🧠 Architecture Overview

```
User → React Frontend → FastAPI → NLP AI Engines → PostgreSQL
                            ↓
         HuggingFace (Sentiment, Emotion, Risk)
                            ↓
         OpenAI (Chat Response + Summarization)
```

---

 ✅ Requirements

 Backend
- Python 3.10+
- `pip install -r requirements.txt`
- PostgreSQL 13+
- `.env` with:
  ```
  OPENAI_API_KEY=your-key
  HUGGINGFACE_API_KEY=your-key
  DATABASE_URL=postgresql://postgres:2003@localhost/mindguard_db
  ```

 Frontend
- Node.js 18+
- `npm install`
- Vite (auto-installed)
- `.env` with:
  ```
  VITE_BACKEND_URL=http://localhost:8000
  ```

---

 🚀 Setup & Installation

 ⬅️ Backend Setup

```bash
 1. Create and activate virtual environment
python -m venv venv
source venv/bin/activate   or venv\Scripts\activate on Windows

 2. Install dependencies
pip install -r requirements.txt

 3. Setup PostgreSQL database
psql -U postgres
CREATE DATABASE mindguard_db;

 4. Run the API
uvicorn app.main:app --reload
```

 ➡️ Frontend Setup

```bash
 1. Navigate to frontend
cd frontend/

 2. Install dependencies
npm install

 3. Start development server
npm run dev
```

---

 ☁️ Deployment

 Local Deployment

- Frontend: `npm run dev` → [http://localhost:5173](http://localhost:5173)  
- Backend: `uvicorn app.main:app --reload` → [http://localhost:8000](http://localhost:8000)

 Production Deployment

- Frontend: Deploy via Vercel or Netlify  
- Backend: Deploy via Fly.io, Railway, or Render
- Setup CI pipelines with GitHub Actions (already included)
- Configure `.env.production` for production API keys

---

 🧪 Testing & Validation

- Backend:  
  `pytest tests/ --disable-warnings -v`
- Frontend:  
  `npm run test` (Jest + RTL)  
  `npx cypress open` (Accessibility + E2E)

- Performance & Audit:  
  `npx lighthouse http://localhost:5173 --view`

- Load Testing:  
  `locust -f locustfile.py`

---

 🔐 Security & Privacy

- No authentication data stored in frontend
- Session summaries stored securely with RAS flags
- Anonymous chat option available
- Future upgrade: Homomorphic encryption for sentiment vectors

---

 📄 License

This project is open-source under the MIT License.  
Please contact the project maintainer for commercial use or collaboration.

---

 🙋 Contribution

Want to improve the future of AI in mental health?  
Feel free to fork, clone, and contribute!

```bash
git clone https://github.com/Euronymous11/MindGuard_AI.git
```

---

💡 Tip: Always check the emotional tone of AI replies in `chat_service.py` to avoid harm during high-risk interactions.

---
