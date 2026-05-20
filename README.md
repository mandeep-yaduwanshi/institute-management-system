# 🏛️ Institute Management System

A scalable backend application for managing institutional data — students, courses, faculty, and fees — powered by **FastAPI**, **PostgreSQL**, and **GenAI** (LangChain + RAG).

---

## ✨ Features

- 🔐 **JWT Authentication** — Secure API access with token-based auth and middleware
- 📚 **Student & Course Management** — Full CRUD APIs for students, courses, faculty, and fee records
- 🗄️ **Optimized Database** — Relational schemas with SQLAlchemy ORM and PostgreSQL
- 🤖 **GenAI Natural Language Queries** — Ask questions about institutional data in plain English using LangChain + RAG
- ⚡ **High Performance** — Async FastAPI with optimized query handling

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| Language | Python |
| Framework | FastAPI |
| ORM | SQLAlchemy |
| Database | PostgreSQL |
| AI / GenAI | LangChain, RAG |
| Auth | JWT (JSON Web Tokens) |
| Validation | Pydantic |
| Testing | Postman |
| Version Control | Git & GitHub |

---

## 📁 Project Structure

```
institute-management-system/
├── app/
│   ├── main.py              # FastAPI app entry point
│   ├── models/              # SQLAlchemy ORM models
│   ├── schemas/             # Pydantic request/response schemas
│   ├── routers/             # API route handlers
│   │   ├── students.py
│   │   ├── courses.py
│   │   ├── faculty.py
│   │   └── fees.py
│   ├── services/            # Business logic
│   ├── ai/                  # LangChain + RAG integration
│   └── auth/                # JWT authentication
├── database.py              # DB connection & session
├── requirements.txt
└── README.md
```

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/institute-management-system.git
cd institute-management-system
```

### 2. Create a Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Set Up Environment Variables
Create a `.env` file:
```env
DATABASE_URL=postgresql://user:password@localhost/institute_db
SECRET_KEY=your_jwt_secret_key
OPENAI_API_KEY=your_openai_or_groq_api_key
```

### 5. Run the Application
```bash
uvicorn app.main:app --reload
```

### 6. Access API Docs
Open your browser at: `http://localhost:8000/docs`

---

## 🤖 GenAI Feature — Natural Language Queries

Ask questions like:
- *"How many students are enrolled in the Computer Science course?"*
- *"List all faculty members in the Engineering department."*
- *"Show me students with pending fees."*

This feature uses **LangChain** and **RAG (Retrieval-Augmented Generation)** to convert plain English questions into database queries and return meaningful answers.

---

## 📡 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/auth/login` | Login & get JWT token |
| GET | `/students/` | List all students |
| POST | `/students/` | Add a new student |
| GET | `/courses/` | List all courses |
| POST | `/courses/` | Add a new course |
| GET | `/faculty/` | List all faculty |
| GET | `/fees/` | View fee records |
| POST | `/ai/query` | Ask a natural language question |

---

## 👨‍💻 Author

**Mandeep Yaduwanshi**
- 📧 mandeepyaduwanshi5@gmail.com
- 🔗 [LinkedIn](https://linkedin.com/in/your-profile)
- 🐙 [GitHub](https://github.com/your-username)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
