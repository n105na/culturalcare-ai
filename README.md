# culturalcare-ai
AI-powered multilingual emotional wellness chatbot


```
culturalcare-ai/
│
├── README.md                # Project overview, setup, usage
├── LICENSE                  # (optional) choose MIT/Apache for open-source
├── .gitignore               # Ignore venv, __pycache__, etc.
├── .env.example             # Template for environment variables
│
├── backend/                 # FastAPI backend (core logic + APIs)
│   ├── app/
│   │   ├── main.py          # FastAPI entrypoint
│   │   ├── api/             # Routes/endpoints
│   │   │   ├── chat.py      # /chat, /analyze_text endpoints
│   │   │   ├── users.py     # (future: auth/users)
│   │   │   └── history.py   # /chat_history
│   │   ├── core/            # Config, settings
│   │   │   ├── config.py    # Reads env vars
│   │   │   └── utils.py     # Common helpers
│   │   ├── models/          # Pydantic + DB models
│   │   │   ├── db_models.py # SQLAlchemy ORM classes
│   │   │   └── schemas.py   # Pydantic schemas
│   │   ├── services/        # Business logic
│   │   │   ├── nlp.py       # Preprocessing pipeline (spaCy + embeddings)
│   │   │   ├── classifier.py# ML model load/predict
│   │   │   └── responses.py # Rule/template-based replies
│   │   └── database.py      # DB connection
│   └── requirements.txt     # Backend deps (FastAPI, scikit-learn, etc.)
│
├── frontend/                # React + Tailwind UI
│   ├── public/              # Static assets
│   ├── src/
│   │   ├── components/      # Chat UI, Mood Chart, Navbar, etc.
│   │   ├── pages/           # HomePage, ChatPage
│   │   ├── services/        # API calls (Axios)
│   │   └── App.js
│   └── package.json
│
├── notebooks/               # Experiments & model training
│   ├── 01_preprocessing.ipynb   # Cleaning + embeddings
│   ├── 02_model_training.ipynb  # Classifier training (LogReg/SVM)
│   ├── 03_evaluation.ipynb      # Metrics + confusion matrix
│   └── 04_export_model.ipynb    # Save model for backend
│
├── models/                  # Saved models
│   └── emotion_classifier.pkl   # Trained sklearn model
│
├── data/                    # Datasets
│   ├── raw/                 # Unprocessed texts
│   ├── processed/           # Cleaned/labeled
│   └── examples.json        # Small sample for testing
│
└── tests/                   # Unit & integration tests
    ├── test_api.py
    ├── test_nlp.py
    └── test_classifier.py
```