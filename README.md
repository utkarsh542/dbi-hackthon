# AI Wealth Advisor — IDBI Innovate 2026

## Problem Statement
Traditional banking apps present raw data without actionable insights, leaving users overwhelmed. They lack personalized, context-aware financial advice grounded in a user's actual portfolio, spending habits, and long-term goals.

## Solution
An AI-powered Wealth Advisor that seamlessly integrates with IDBI's banking ecosystem. It provides proactive, personalized financial guidance using a voice-enabled conversational interface, grounded entirely in the user's real-time financial metrics to eliminate hallucinations and ensure trustworthy advice.

## Quick Start

### 1. Backend
```bash
cd backend
pip install -r requirements.txt
cp .env.example .env          # Add your ANTHROPIC_API_KEY
uvicorn app.main:app --reload --port 8000
```

### 2. Frontend
```bash
cd frontend
npm install
npm run dev
# Opens at http://localhost:5173
```

## Tech Stack
- **Backend:** FastAPI, Python, Anthropic Claude API (tool-calling)
- **Frontend:** React, Vite, Tailwind CSS, Recharts
- **Voice:** Browser-native Web Speech API (STT + TTS), no external service
- **Data:** Synthetic customer personas (8 profiles)
- **Architecture:** Provider-agnostic LLMGateway pattern (swap Claude for any LLM in one line)

## Key Features
- **Grounded AI:** Personalized advice grounded in real customer data via tool-calling (not hallucinated).
- **Voice Interaction:** Voice interaction with animated orb synced to speech, utilizing browser-native Web Speech API.
- **Graceful Degradation:** The application gracefully degrades to deterministic data if the API is unavailable (the demo never breaks).
- **Goal Projection:** Goal feasibility projection using SIP compound growth math.
- **Auditability:** Full conversation history per customer, displaying exact "Sources used" for maximum transparency.
