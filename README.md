# NextRoundAI 🚀

**NextRoundAI** is a video‑first interview practice platform that helps candidates master behavioral interviews using the **STAR method** (Situation, Task, Action, Result).

It uses your **Job Description** (and optional **Resume**) to generate tailored questions and strict feedback, backed by Gemini models running server‑side.

👉 Live website: https://next-round-ai.vercel.app/

## ✨ Key Features

- **🎥 Video-First Practice**: Record answers and get STAR-based feedback with evidence quotes.
- **🧠 JD + Resume Context**: AI references your job description + resume (PDF, TXT, or MD) to tailor feedback.
- **⚖️ Adaptive Difficulty**: Questions scale based on confidence (Beginner → Advanced).
- **⭐ Strict STAR Scoring**: Components only counted when explicitly stated.
- **🔐 Google-Only Login**: Simple OAuth sign-in for students.
- **📊 Performance Dashboard**: Readiness, momentum/consistency, and predictive growth insights.
- **🎓 Free Interviews**: No quota limits for students until out of free credits.
- **💼 Interview Modes**: Professional vs. Casual.
- **🎓 Role Types**: Internship vs. Full‑Time.
- **🏢 Company‑Aware Prompts**: Enter a company to tailor question style.

## 🧭 Guided User Flow
1. **Sign in with Google**
2. **Choose role type** (Internship or Full‑Time)
3. **Pick interview mode** (Professional or Casual)
4. **Paste a Job Description** + optional resume
5. **Set confidence** → difficulty adjusts automatically
6. **Record video responses**
7. **Receive STAR feedback + improvements**
8. **Review progress in the dashboard**

## 📊 Dashboard Highlights
- **Readiness Score** + trend
- **STAR Evidence** breakdown per response
- **Momentum & Consistency** tracking
- **Recent Activity** with reviewable feedback
- **Pre/Post Confidence** averages

## 🛠️ Tech Stack

- **Frontend**: React 19, Vite, Tailwind CSS, Motion, Lucide React.
- **Backend**: FastAPI, SQLAlchemy (async), Alembic, Postgres (Supabase).
- **AI Engine**: Google Gemini (server-side via `google-genai`).
- **Authentication**: Google OAuth (JWT issued by backend).
- **Deployment**: Vercel (frontend) + Render (backend).
