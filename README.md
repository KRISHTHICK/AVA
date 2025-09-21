# Agent-Avan Demo (Frontend + FastAPI backend)

This repository contains a prototype frontend (HTML/CSS/JS using Tailwind CDN) and a small FastAPI backend that:
- Serves the UI (index.html)
- Accepts file uploads at /api/upload (mock processing)
- Provides a mock chat endpoint at /api/chat

## Run locally

1. Create virtualenv and install:
```
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

2. Run:
```
uvicorn app:app --reload
```

3. Open http://localhost:8000

## Notes & Integration points (for production)
- Replace mock endpoints with real Google services:
  - Use Vertex AI Document AI for OCR and extraction.
  - Use Gemini via Vertex AI for LLM tasks (simplify, classify, translate).
  - Store policies in BigQuery and use Vector Search for RAG retrieval.
  - Use Firebase Auth for authentication and Cloud Storage for files.
  - Use Cloud Pub/Sub to implement multi-agent event bus.
- The frontend is built with Tailwind CDN for quick prototyping. For production, convert to a proper build pipeline.

## Packaging
The files are in this zip. Unzip and run as above.
