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

1. Navigate to backend folder:
```
cd backend
```

2. Create virtual environment:
```

python -m venv venv
venv\Scripts\activate   # Windows
# or
source venv/bin/activate   # Mac/Linux
```

3. Install dependencies:
```
pip install -r requirements.txt
python -m spacy download en_core_web_sm
```

4. Run FastAPI server:
```
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```


🎨 Frontend Setup (React + Vite)

1. Navigate to frontend folder:
```

cd frontend
```

2. Install dependencies:
```
npm install

```
3. Start dev server:
```
npm run dev
```

⚠️ Notes & Limitations

This project is a demo / prototype — not for clinical use without expert review.
Models may hallucinate or miss entities. Always verify.
For better accuracy, swap spaCy small model (en_core_web_sm) with scispaCy / medSpaCy.
HuggingFace models will download on first run — ensure internet access.

🚀 Next Steps

Add user-friendly frontend UI (tabs for Entities, Summary, Sentiment, SOAP Note).
Use nvm-windows for managing Node.js versions.
Fine-tune ClinicalBERT / BioBERT for medical sentiment.
Add negation detection (e.g., “no headache” should not extract “headache”).
Deploy to cloud (Heroku, Render, or Docker on AWS).

👨‍💻 Author

Made with ❤️ using FastAPI + React + NLP.
For educational and prototyping purposes only.
