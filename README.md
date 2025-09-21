# 🩺 Physician Notetaker — NLP Doctor System 

An end-to-end AI system for clinical transcription analysis:
Extracts symptoms, treatments, diagnoses, prognosis
Generates summaries & keywords
Performs sentiment & intent analysis
Produces structured SOAP notes

# Built with:

Backend: Python, FastAPI, spaCy, HuggingFace Transformers
Frontend: React (Vite), Fetch API


1. Project Repositry
```
NLPDoctor System/
├── backend/
│   ├── app/
│   │   ├── __init__.py
│   │   ├── main.py
│   │   ├── utils_ner.py
│   │   ├── utils_summarizer.py
│   │   ├── utils_keywords.py
│   │   ├── utils_sentiment.py
│   │   └── utils_soap.py
│   ├── requirements.txt
│   └── Dockerfile
├── frontend/
│   ├── index.html
│   ├── package.json
│   ├── vite.config.js
│   └── src/
│       ├── App.jsx
│       ├── main.jsx
│       └── index.css
```

⚙️ Backend Setup (FastAPI)

Navigate to backend folder:
```
cd backend
```

Create virtual environment:
```

python -m venv venv
venv\Scripts\activate   # Windows
# or
source venv/bin/activate   # Mac/Linux
```

Install dependencies:
```
pip install -r requirements.txt
python -m spacy download en_core_web_sm
```

Run FastAPI server:
```
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000

```
Test health check:
```
http://localhost:8000/health
```

🎨 Frontend Setup (React + Vite)

Navigate to frontend folder:
```

cd frontend
```

Install dependencies:
```
npm install

```
Start dev server:
```
npm run dev
```

