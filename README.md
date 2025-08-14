# 🚚 Greencart: Delivery Simulation App

![React](https://img.shields.io/badge/frontend-react-blue?logo=react)
![Flask](https://img.shields.io/badge/backend-flask-yellow?logo=flask)
![Supabase](https://img.shields.io/badge/database-supabase-green?logo=supabase)
![License](https://img.shields.io/badge/license-MIT-lightgrey)
![Deploy Backend](https://img.shields.io/badge/render-deployed-success?logo=render)
![Deploy Frontend](https://img.shields.io/badge/netlify-deployed-success?logo=netlify)

> A full-stack web app for simulating logistics and delivery operations with real-time tracking, route planning, and historical analytics.

---

## 📖 Table of Contents

- [✨ Overview](#-overview)  
- [🚀 Features](#-features)  
- [🛠 Tech Stack](#-tech-stack)  
- [⚙️ Getting Started](#-getting-started)  
- [🔐 Environment Variables](#-environment-variables)  
- [📦 Usage](#-usage)  
- [🌍 Deployment](#-deployment)  
- [📁 Folder Structure](#-folder-structure)
- [📸 Screenshots](#-screenshots)  
- [🤝 Contributing](#-contributing)  
- [📄 License](#-license)  
- [📬 Contact](#-contact)  

---

## ✨ Overview

Greencart is a simulation platform for logistics and delivery management. It enables fleet managers to plan routes, assign drivers, monitor delivery status, and analyze historical performance. Built with a modern tech stack and clean UI, it’s designed for scalability, clarity, and impact.

---

## 🚀 Features

- 🔐 JWT-based user authentication  
- 📍 Route simulation with driver status updates  
- 🧑‍💼 CRUD operations for drivers, routes, and orders  
- 📊 Historical tracking and analytics  
- 🔄 RESTful API with Flask and SQLAlchemy  
- 📱 Responsive UI with Tailwind CSS  
- 🗄 PostgreSQL database via Supabase  

---

## 🛠 Tech Stack

| Layer       | Tools & Frameworks                             |
|------------|-------------------------------------------------|
| Frontend   | React, React Router, Axios, Tailwind CSS        |
| Backend    | Flask, Flask-JWT-Extended, Flask-CORS, SQLAlchemy |
| Database   | PostgreSQL (Supabase)                           |
| Deployment | Render (backend), Netlify (frontend)            |
| Auth       | JWT Tokens                                      |

---

## ⚙️ Getting Started

### 🔧 Prerequisites

- Node.js & npm/yarn  
- Python 3.8+  
- Supabase account  
- Render & Netlify accounts (optional)

### 🐍 Backend Setup

```bash
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

Create a `.env` file:

```env
DATABASE_URL=your_supabase_postgres_connection_string
JWT_SECRET_KEY=your_jwt_secret_key
```

Run the server:

```bash
flask run
```

### ⚛️ Frontend Setup

```bash
cd frontend
npm install  # or yarn install
```

Create `.env` file:

```env
REACT_APP_API_URL=http://localhost:5000
```

Run the frontend:

```bash
npm start  # or yarn start
```

---

## 🔐 Environment Variables

| Variable            | Description                                  |
|---------------------|----------------------------------------------|
| `DATABASE_URL`      | Supabase PostgreSQL connection string        |
| `JWT_SECRET_KEY`    | Secret key for JWT token generation          |
| `REACT_APP_API_URL` | Backend API base URL (used by frontend)      |

---

## 📦 Usage

1. Register/login as a manager  
2. Add drivers, routes, and orders  
3. Run delivery simulations  
4. View real-time updates and historical analytics  

---

## 🌍 Deployment

- 🔧 Backend: [Render](https://render.com)  
- 🎨 Frontend: [Netlify](https://netlify.com)  
- ✅ Environment variables securely configured on both platforms

---

## 📁 Folder Structure

```bash
/backend
  ├── routes/         # API blueprints
  ├── models.py       # SQLAlchemy models
  └── app.py          # Flask entrypoint

/frontend
  └── src/
      ├── components/ # React components
      └── api.js      # Axios instance

README.md             # Project documentation
```

---

## 📸 Screenshots

> _A glimpse into Greencart’s simulation dashboard:_

<img width="788" height="946" alt="image" src="https://github.com/user-attachments/assets/471625bd-7ba8-4fcd-9e26-fabedbc2eca4" />

### Key Metrics Displayed:

- 💰 **Total Profit**: ₹78,327.80  
- ⚡ **Efficiency Score**: 100.00%  
- 🕒 **Late Deliveries**: 0.00%  
- 📦 **Avg Order Value**: ₹1,530.08  

### Visual Insights:

- 📊 **Delivery Performance**: On-time vs Late bar chart  
- ⛽ **Fuel Cost Breakdown**: Pie chart  
- 🚚 **First Attempt Delivery Rate**: Pie chart  
- 📈 **Profit Over Time**: Line graph  
- 📉 **Profit Margin Trend**: Line graph  
- ⏱ **Avg Time Per Delivery**: Line graph  
- 🧮 **On-Time vs Late Over Time**: Comparative bar chart  

---
### 🧪 Simulation Interface
#### > Configure delivery parameters and run simulations to evaluate fleet performance.

🎛 Input Parameters
👥 Number of Drivers: 3
⏰ Start Time: 10:00
⌛ Max Hours/Driver: 4
▶️ Action: Run Simulation

<img width="1174" height="915" alt="image" src="https://github.com/user-attachments/assets/d53a4866-ab31-4682-ad00-f992c52d8b70" />

---
### 🧭 Management Console Overview
#### A unified dashboard for managing drivers, routes, and orders with real-time control and CRUD operations upon API.
<img width="777" height="893" alt="image" src="https://github.com/user-attachments/assets/c36a5bd5-589c-4236-96c4-804b4e070bca" />
---


## 🤝 Contributing

Pull requests are welcome!  
Fork the repo → Create a branch → Make changes → Submit PR

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 📬 Contact

Created by **Firdaush Alam**  
Let’s connect on **[LinkedIn]** (https://www.linkedin.com/firdaush-alam) or 
**[Portfolio]** (https://firdaushalamportfolio.netlify.app/)
