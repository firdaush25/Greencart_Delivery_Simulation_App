# 🚚 GreenCart Logistics

**Delivery Simulation & KPI Dashboard for Smarter Logistics Decisions**

🔗 **Live App:** [firdaushgreencartproject.netlify.app](https://firdaushgreencartproject.netlify.app/)

---

## 📦 Project Overview

GreenCart Logistics is a full-stack web application that simulates delivery operations and visualizes key performance indicators (KPIs) to help logistics managers make data-driven decisions. Users can:

- Run delivery simulations based on real-world parameters
- Analyze KPIs like profit, fuel cost, delivery efficiency, and driver fatigue
- View historical simulation results in an interactive dashboard

---

## 🛠️ Tech Stack

| Layer       | Technologies Used                                                                 |
|-------------|------------------------------------------------------------------------------------|
| **Frontend**| React.js, Tailwind CSS, Chart.js, React Toastify                                   |
| **Backend** | Flask (Python), Flask-JWT-Extended, Flask-CORS, SQLAlchemy ORM                    |
| **Database**| PostgreSQL / SQLite                                                                |
| **Deployment**| Netlify (Frontend), Railway / Render / PythonAnywhere (Backend)                 |
| **Utilities**| Native JS & Python datetime, JWT Auth, Toast Notifications                        |

---

## ⚙️ Setup Instructions

### 🔧 Prerequisites

- Python 3.8+
- Node.js & npm
- Git

---

### 🐍 Backend Setup

```bash
# Clone the repo
git clone <your-repo-url>
cd your-backend-folder

# Create virtual environment
python -m venv venv
source venv/bin/activate       # Linux/macOS
venv\Scripts\activate.bat      # Windows

# Install dependencies
pip install -r requirements.txt

# Create .env file
FLASK_APP=run.py
FLASK_ENV=development
SECRET_KEY=your_secret_key
JWT_SECRET_KEY=your_jwt_secret
DATABASE_URL=your_database_connection_string

# Initialize DB
flask db init
flask db migrate
flask db upgrade

# Run server
flask run
```

---

### ⚛️ Frontend Setup

```bash
# Navigate to frontend
cd your-frontend-folder

# Install dependencies
npm install

# Create .env file
REACT_APP_API_URL=http://localhost:5000

# Start development server
npm start
```

---

## 🌐 Environment Variables

### Backend `.env`

| Key              | Description                                 |
|------------------|---------------------------------------------|
| `FLASK_APP`      | Flask entry point (e.g., `run.py`)          |
| `FLASK_ENV`      | Environment mode (`development`/`production`)|
| `SECRET_KEY`     | Flask session secret                        |
| `JWT_SECRET_KEY` | JWT authentication secret                   |
| `DATABASE_URL`   | DB connection string                        |

### Frontend `.env`

| Key                   | Description                          |
|-----------------------|--------------------------------------|
| `REACT_APP_API_URL`   | Backend API base URL                 |

---

## 🚀 Deployment Guide

### Frontend (Netlify)

1. Connect GitHub repo to Netlify  
2. Set build command: `npm run build`  
3. Set publish directory: `build/`  
4. Deploy — Netlify handles CI/CD on push

### Backend (Railway / Render / PythonAnywhere)

1. Push code or connect GitHub repo  
2. Set environment variables  
3. Configure service to run Flask (`flask run` or `gunicorn`)  
4. Enable CORS for frontend domain

---

## 📊 API Documentation

### Base URL

```
http://<backend-host>/simulate
```

---

### 🔁 Run Simulation

- **POST** `/`
- **Description:** Simulates delivery run and returns KPIs
- **Request Body:**
```json
{
  "num_drivers": 10,
  "start_time": "2025-08-13 06:00:00",
  "max_hours": 8
}
```
- **Response Example:**
```json
{
  "total_profit": 1200.50,
  "efficiency_score": 85.0,
  "fuel_cost": 500,
  "late_percentage": 15.0,
  "total_deliveries": 100,
  "avg_order_value": 30.0
}
```

---

### 📜 Get Simulation History

- **GET** `/history`
- **Description:** Returns list of past simulation runs
- **Response Example:**
```json
[
  {
    "id": 1,
    "total_profit": 1200.50,
    "timestamp": "2025-08-13 06:00:00",
    "efficiency_score": 85.0,
    "fuel_cost": 500
  },
  ...
]
```

---

### 🧩 Additional APIs

- **Orders CRUD** — Create, read, update, delete orders  
- **Routes CRUD** — Manage delivery routes  
- **Drivers List** — View driver shifts and fatigue metrics  

---

## 🔐 Notes

- All API requests require JWT authentication (`Authorization: Bearer <token>`)
- Date-time format: `"YYYY-MM-DD HH:mm:ss"`
- KPIs factor in fatigue, traffic, route distance, and business rules

---

## 💬 Contact

Feel free to reach out for setup help, feedback, or collaboration ideas!

---


