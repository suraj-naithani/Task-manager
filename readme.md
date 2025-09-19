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

### Step 1: Create a Project Folder
```bash
mkdir fastapi_project
cd fastapi_project
```

### 🛠 Step 2: Create a Virtual Environment

A virtual environment keeps your dependencies isolated.

**For Windows:**
```bash
python -m venv venv
```

**For macOS/Linux:**
```bash
python3 -m venv venv
```

### 🛠 Step 3: Activate the Virtual Environment

**Windows (Command Prompt):**
```bash
venv\Scripts\activate
```

**macOS/Linux:**
```bash
source venv/bin/activate
```

👉 You should now see (venv) at the start of your terminal.

### 🛠 Step 4: Create requirements.txt

Create a file named requirements.txt inside the project folder with this content:

```
fastapi
uvicorn
sqlalchemy
psycopg2-binary
pydantic
```

### 🛠 Step 5: Install Dependencies

Run:

```bash
pip install -r requirements.txt
```

This will install:

- **FastAPI** → Web framework
- **Uvicorn** → ASGI server (to run FastAPI)
- **SQLAlchemy** → ORM for database handling
- **psycopg2-binary** → PostgreSQL driver
- **Pydantic** → Data validation and settings management

### 🛠 Step 6: Verify Installation

Check installed packages:

```bash
pip list
```

Run a quick FastAPI test app (main.py):

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def home():
    return {"message": "Hello, FastAPI is running!"}
```

Run the app:

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