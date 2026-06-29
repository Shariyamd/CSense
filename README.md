# CSense – Intelligent Customer Success Action Platform

## Overview

CSense is an AI-powered, multi-agent Decision Intelligence Platform designed to help Customer Success Managers (CSMs) proactively identify churn risks, recommend validated Next Best Actions, and automate customer engagement.

Instead of manually analyzing CRM records, product usage, meeting history, support tickets, and stakeholder interactions, CSense orchestrates multiple AI agents to reason over customer data, explain business decisions, validate recommendations through an independent review, and automate execution workflows.

Unlike traditional chatbots or RAG applications, CSense follows a planner-driven multi-agent architecture where every recommendation is independently challenged and validated before execution, enabling explainable and trustworthy business decisions.

---

# Features

- Multi-Agent AI workflow using LangGraph
- Planner Agent for dynamic orchestration
- Context Retrieval from multiple enterprise data sources
- AI-Powered Risk & Opportunity Analysis
- Next Best Action Recommendation Engine
- Devil's Advocate Agent for independent validation
- Shared Memory for continuous learning
- Human-in-the-Loop decision approval
- Zoom meeting automation
- Recall.ai meeting transcription
- AI-generated meeting summaries and action items
- Interactive React dashboard

---

# Technology Stack

## Frontend

- React (Vite)
- Tailwind CSS
- Framer Motion
- Lucide React
- Axios

## Backend

- FastAPI
- Python
- LangGraph
- Pydantic
- HTTPX

## AI

- Google Gemini 2.5 Flash
- Multi-Agent Architecture

## Integrations

- Zoom Server-to-Server OAuth
- Recall.ai
- Google Gemini API

## Data Layer

- CRM Data
- Product Usage
- Support Tickets
- Customer Contacts
- Meeting History
- JSON-based Knowledge Store

---

# System Architecture

```text
                    React Dashboard
                           │
                           ▼
                  FastAPI Backend API
                           │
                           ▼
                 LangGraph Agent Pipeline
                           │
      ┌─────────────────────────────────────────┐
      │ Planner Agent                           │
      │          ↓                              │
      │ Context Retrieval Agent                 │
      │          ↓                              │
      │ Risk Analysis Agent                     │
      │          ↓                              │
      │ Recommendation Agent                    │
      │          ↓                              │
      │ Devil's Advocate Agent                  │
      │          ↓                              │
      │ Memory Agent                            │
      └─────────────────────────────────────────┘
                           │
                           ▼
                 Decision Workspace
                           │
                           ▼
           Zoom + Recall.ai Automation
                           │
                           ▼
         AI Meeting Summary & Memory Update
```

---

# Project Structure

```text
CSense/
│
├── backend/
│   ├── agents/
│   ├── data/
│   ├── graph/
│   ├── models/
│   ├── services/
│   ├── main.py
│   ├── ai_client.py
│   ├── requirements.txt
│   └── .env.example
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   ├── package-lock.json
│   └── vite.config.js
│
├── run_app.bat
├── .gitignore
└── README.md
```

---

# Environment Variables

Create a `.env` file inside the **backend** folder using `.env.example` as a reference.

```env
GOOGLE_API_KEY=your_google_api_key

RECALL_AI_API_KEY=your_recall_api_key

ZOOM_ACCOUNT_ID=your_zoom_account_id
ZOOM_CLIENT_ID=your_zoom_client_id
ZOOM_CLIENT_SECRET=your_zoom_client_secret
```

> **Note:** The `.env` file is intentionally excluded from this repository to protect sensitive credentials. Use your own API keys to run the project.

---

# Installation

## 1. Clone the Repository

```bash
git clone https://github.com/ShafiyaMasrath/CSense.git
```

```bash
cd CSense
```

---

## 2. Backend Setup

```bash
cd backend

python -m venv venv
```

### Activate Virtual Environment

Windows

```bash
venv\Scripts\activate
```

Install dependencies

```bash
pip install -r requirements.txt
```

Start the backend

```bash
uvicorn main:app --reload
```

Backend runs at:

```
http://localhost:8000
```

---

## 3. Frontend Setup

Open another terminal.

```bash
cd frontend

npm install

npm run dev
```

Frontend runs at:

```
http://localhost:5173
```

---

# Quick Start (Windows)

To launch both backend and frontend automatically, simply run:

```bash
.\run_app.bat
```

---

# Multi-Agent Workflow

1. Customer selected from dashboard
2. Planner Agent initializes workflow
3. Context Retrieval Agent gathers enterprise knowledge
4. Risk Analysis Agent evaluates customer health and business risks
5. Recommendation Agent generates Next Best Actions
6. Devil's Advocate Agent validates and challenges recommendations
7. Human reviews and approves the final strategy
8. Zoom meeting, executive email, and Recall.ai bot are automatically created
9. Meeting transcript is analyzed using Gemini
10. Summary, sentiment, and action items are stored as customer memory

---

# AI Agents

### Planner Agent

Coordinates the complete execution workflow and determines agent sequencing.

### Context Retrieval Agent

Collects customer information from CRM records, support tickets, product usage, meetings, and stakeholder data.

### Risk Analysis Agent

Evaluates churn risk, expansion opportunity, product adoption, and champion stability using Gemini.

### Recommendation Agent

Generates prioritized Next Best Actions supported by business evidence.

### Devil's Advocate Agent

Independently challenges recommendations by identifying hidden assumptions, potential risks, and mitigation strategies before execution.

### Memory Agent

Stores summaries, execution history, and customer insights to improve future recommendations.

---

# Demo Highlights

- AI-powered Customer Success Dashboard
- Planner-based Multi-Agent Workflow
- Explainable Risk Analysis
- Independent Recommendation Validation
- Decision Workspace
- Zoom Meeting Automation
- Recall.ai Meeting Intelligence
- Customer Memory & History

---

# Future Enhancements

- Salesforce Integration
- HubSpot Integration
- Microsoft Teams Integration
- Slack Notifications
- Predictive Churn Forecasting
- Vector Database Integration
- Voice Sentiment Analysis
- Multi-language Support
- Real-time CRM Synchronization

---

# Team

**Team Name:** **IGNITERS**

### Team Members

- Shafiya Masrath
- Shariya Md
- Samreen Shaik

---

# Acknowledgements

Built for the **XLVentures.AI Intelligent Next Best Action Platform Hackathon**.

CSense demonstrates how reusable multi-agent AI systems can transform Customer Success by combining contextual understanding, explainable reasoning, independent validation, shared memory, and intelligent workflow automation.

