# FastAPI + PostgreSQL Setup

This repository contains a basic setup for a FastAPI project with PostgreSQL using SQLAlchemy and Pydantic.

## 📂 Project Structure
```
fastapi_project/
│── venv/                 # Virtual environment (not pushed to GitHub)
│── requirements.txt       # Project dependencies
│── main.py                # FastAPI entry point
│── README.md              # Documentation
```

## 🚀 Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/fastapi_project.git
cd fastapi_project
```

### 2. Create a Virtual Environment

**Windows**
```bash
python -m venv venv
```

**macOS/Linux**
```bash
python3 -m venv venv
```

### 3. Activate the Virtual Environment

**Windows (Command Prompt)**
```bash
venv\Scripts\activate
```

**macOS/Linux**
```bash
source venv/bin/activate
```

### 4. Install Dependencies
```bash
pip install -r requirements.txt
```

**requirements.txt**
```
fastapi
uvicorn
sqlalchemy
psycopg2-binary
pydantic
```

### 5. Run the FastAPI App
```bash
uvicorn main:app --reload
```

Now, open:

- **API:** 👉 http://127.0.0.1:8000
- **Docs (Swagger UI):** 👉 http://127.0.0.1:8000/docs
- **Docs (ReDoc):** 👉 http://127.0.0.1:8000/redoc

## ✅ Quick Example

**main.py**
```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def home():
    return {"message": "Hello, FastAPI is running!"}
```

**Run:**
```bash
uvicorn main:app --reload
```

## ⚡ Useful Commands

**Check installed packages:**
```bash
pip list
```

**Export dependencies:**
```bash
pip freeze > requirements.txt
```

**Deactivate virtual environment:**
```bash
deactivate
```

## 🛠 Tech Stack

- **FastAPI** – Web framework
- **Uvicorn** – ASGI server
- **SQLAlchemy** – ORM
- **Pydantic** – Data validation
- **PostgreSQL** – Database

✨ **That's it! You now have a clean FastAPI + PostgreSQL starter setup.**