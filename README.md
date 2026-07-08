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

## 🌟 IDBI WealthAI: Total Key Features

### 🛡️ 1. Enterprise-Grade AI (Safe & Reliable)
- **Zero Hallucinations:** 100% grounded in real-time portfolio & transaction data via custom tool-calling. It never hallucinates financial numbers.
- **Total Transparency:** Maintains a full conversation history per customer and explicitly cites the "Sources used" for every financial answer to guarantee transparency and build trust.
- **Fail-Safe Architecture (Graceful Degradation):** Designed for high reliability; if the primary LLM API goes down, the application gracefully degrades to an offline deterministic mode (the demo *never* breaks).
- **Strict, Professional Persona Constraints:** The AI acts exclusively as *IDBI WealthAI*. It refuses to break character, avoids general trivia, and gracefully pivots non-financial questions back to wealth management.

### 🗣️ 2. Frictionless User Experience (Innovative UI)
- **Native Voice Interface:** Features a dynamic, voice-responsive animated orb using browser-native Speech-to-Text and Text-to-Speech (no third-party plugins required).
- **Context-Aware Memory & Continuous Learning:** Automatically extracts and remembers the client's past preferences, unrecorded goals, and financial concerns across sessions for highly personalized coaching.

### 📈 3. Proactive Wealth Coaching (Business Impact)
- **Money Leak Audits:** Actively scans detailed user bills and transaction data to identify "money leaks" (like unused subscriptions) and recommend ways to optimize cash flow.
- **Dynamic Financial Health Engine:** Instantly calculates complex financial metrics on the fly, including Savings Rate, Asset Allocation, and Weighted Portfolio Returns.
- **Actionable Goal Projections:** Uses compound growth (SIP) mathematics to calculate goal feasibility. Doesn't just highlight shortfalls—it recommends the *exact* additional monthly SIP required to get back on track.
