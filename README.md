NextRoundAI 🚀
NextRoundAI is a high-signal, video-exclusive interview intelligence platform designed to help candidates master behavioral interviews using the STAR method (Situation, Task, Action, Result).

By leveraging Retrieval-Augmented Generation (RAG) and the latest Gemini 3.1 Pro multimodal models, NextRoundAI provides personalized, industry-specific coaching grounded in your target job description.

✨ Key Features
🎥 Video-Only Behavioral Practice: Focus on high-signal video responses to prepare for real-world assessments.
🧠 RAG-Powered Scoring: The AI uses your provided Job Description as a knowledge base to evaluate your answers against specific role requirements.
⚖️ Adaptive Difficulty: Questions are dynamically generated based on your self-reported confidence level (Entry-level, Intermediate, or Advanced).
⭐ STAR Schema Measurement: Rigorous extraction and validation of Situation, Task, Action, and Result components.
🔐 Secure User Accounts: Full signup/login system with encrypted password storage using bcryptjs.
🔄 Session Resume: Mid-interview progress is automatically saved, allowing you to pick up exactly where you left off.
📊 Performance Dashboard: Track your readiness scores, confidence trends, and practice history over time.
🛠️ Tech Stack
Frontend: React 19, Tailwind CSS, Motion (Framer Motion), Lucide React.
Backend: Node.js, Express, SQLite (better-sqlite3).
AI Engine: Google Gemini 3.1 Pro (Multimodal Video & Text Analysis).
Authentication: Custom Auth with bcryptjs hashing.
Deployment: Optimized for Vercel and other modern cloud platforms.
🚀 Getting Started
Prerequisites
Node.js 18+
Gemini API Key
Installation
Clone the repository.
Install dependencies:
npm install
Create a .env file and add your Gemini API Key:
GEMINI_API_KEY=your_api_key_here
Start the development server:
npm run dev
🌐 Deployment on Vercel
This application is designed to be easily deployed on Vercel.

Push your code to a GitHub repository.
Connect the repository to Vercel.
Add your GEMINI_API_KEY to the Vercel environment variables.
Vercel will automatically detect the build settings and deploy your app.
🐍 Backend (FastAPI Skeleton)
A FastAPI backend is available in backend/ for Render + Postgres. It keeps the same /api/* routes used by the frontend and uses Postgres for storage.

Run locally
cd backend
pip install -r requirements.txt
alembic upgrade head
uvicorn main:app --reload --host 0.0.0.0 --port 8000
Local dev helpers
Use the Makefile for common tasks:

make db-up
make migrate
make dev-backend
Example analytics and seed SQL live in:

notes/analytics_queries.sql
notes/seed_data.sql
Data engineering helpers
Export tables to CSV:

DATABASE_URL=postgres+asyncpg://... python scripts/export_csv.py
Seed data from SQL:

DATABASE_URL=postgres+asyncpg://... python scripts/seed.py
If these scripts complain about psycopg2, install backend deps:

pip install -r backend/requirements.txt
Supabase connection string
Set DATABASE_URL to your Supabase Postgres connection string. Example:

postgres+asyncpg://postgres:YOUR_PASSWORD@db.YOUR_PROJECT.supabase.co:5432/postgres
Frontend API base URL
Set this in your frontend environment to point at the FastAPI backend:

VITE_API_BASE_URL=https://your-render-backend.onrender.com
Gemini on the backend
Set GEMINI_API_KEY in Render for the backend service. The frontend no longer needs the key.

JWT auth
Set JWT_SECRET_KEY in Render. The backend issues JWTs on login/signup and expects them in Authorization: Bearer <token> for protected routes.

Keeping Render Awake (cron-job.org)
If you’re on the free Render tier, the service can sleep when idle. You can keep it warm by pinging /health every 5 minutes using cron-job.org:

Create an account on cron-job.org.
Create a new cron job with URL https://nextroundai.onrender.com/health.
Set the schedule to every 5 minutes.
NextRoundAI — Secure your next round with confidence.
