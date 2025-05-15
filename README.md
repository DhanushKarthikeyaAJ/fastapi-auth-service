# 🔐 fastapi-auth-service

fastapi-auth-service is a lightweight, secure, and modular authentication microservice built using FastAPI, designed to handle user registration, login, and role-based access control using JWT (JSON Web Tokens). The service is containerized with Docker, making it portable and easy to integrate within larger microservice-based architectures such as event management systems or SaaS platforms.

This is a simple and secure **Authentication Microservice** built with **FastAPI**, using **JWT-based authentication**. It includes user registration, login, and role-based access (organizer/attendee). The service is fully containerized with Docker.

---

## 🚀 Features

- ✅ FastAPI framework (Python)
- 🔐 JWT Authentication
- 🧑‍💻 User registration, login, and role support
- 🗃️ SQLite (easy to upgrade to PostgreSQL)
- 🐳 Dockerized for portability
- 📄 Swagger UI for API docs (`/docs`)

---
## 🧰 Tech Stack

- Python 3.10+
- FastAPI
- SQLAlchemy
- JWT (python-jose)
- Passlib for password hashing
- Docker

---

## 🗂️ Folder Structure

```
auth_service/
├── app/
│   ├── main.py          # FastAPI entry point
│   ├── database.py      # SQLAlchemy DB setup
│   ├── models.py        # DB models (User)
│   ├── schemas.py       # Pydantic models
│   ├── routes.py        # Routes for /register, /login, /me
│   └── auth.py          # JWT logic, password hashing
├── requirements.txt     # Dependencies
├── Dockerfile           # Docker setup
└── .env                 # Environment variables
```

---

## 🛠️ Getting Started

### 📦 Requirements

- Python 3.10+
- Docker (optional but recommended)

### ▶️ Run Locally

```bash
pip install -r requirements.txt
uvicorn app.main:app --reload
```

### 🐳 Run with Docker

```bash
docker build -t auth_service .
docker run -p 8000:8000 auth_service
```

---

## 🔑 API Endpoints

Visit: [http://localhost:8000/docs](http://localhost:8000/docs)

| Method | Endpoint      | Description               |
|--------|---------------|---------------------------|
| POST   | `/register`   | Register a new user       |
| POST   | `/login`      | Get JWT access token      |
| GET    | `/me`         | Get current user (token)  |

---

## 📚 Environment Variables (`.env`)

```env
SECRET_KEY=supersecretkey
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30
```

---

## 🧠 Concepts Used

- FastAPI Dependency Injection
- JWT with `python-jose`
- Password Hashing with `passlib`
- SQLite with SQLAlchemy
- Dockerfile for image creation

---

## 📈 To Do (Next Steps)

- Replace SQLite with PostgreSQL
- Add Docker Compose for DB service
- Add unit tests with Pytest
- Set up CI/CD (GitHub Actions)
- Deploy on Render/Railway/EC2

---

## 🧑‍💻 Author

Built by [Dhanush Karthikeya A J] 
