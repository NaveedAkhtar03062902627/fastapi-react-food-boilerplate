# Full-Stack Food Ordering App Template (React + FastAPI)

A clean, production-ready full-stack boilerplate built with **React** (Frontend) and **FastAPI** (Backend) using **PostgreSQL** for data persistence. This template is designed as a lightweight, un-opinionated foundation to jumpstart your e-commerce or food delivery SaaS project, saving you over 10+ hours of boilerplate configuration.

---

## ✨ Features Included
- **Dynamic Meal Page:** Renders predefined menu items directly from the backend endpoints.
- **Stateful Shopping Cart:** Interactive cart popup allowing users to add items, change quantities dynamically, or remove items.
- **Streamlined Checkout Form:** Captures vital customer info (Name, Email, Post Code, City) securely.
- **Database Persistence:** Saves successful order details directly to your connected PostgreSQL instance.
- **Clean Architecture:** Divided into strict frontend and backend folders for easy modular development.

*Note: This is a developer template. User authentication (Login) and admin control panels (Adding meals via UI) are intentionally excluded so you can easily plug in your own preferred workflow (e.g., Auth0, Firebase, or JWT).*

---

## 🏗️ Project Structure
```text
├── backend/          # FastAPI App (Pydantic, SQLAlchemy/SQLModel configuration)
├── frontend/         # React Application (Vite/Tailwind CSS design)
└── render.yaml       # 1-Click Infrastructure Deployment Blueprint
```

---

## ⚙️ Local Development Setup

### 🗄️ 1. Database Configuration
This application is compatible with **any PostgreSQL database instance** (Supabase, Neon, AWS RDS, or local Postgres).

1. Create a `.env` file in the root of the `/backend` directory.
2. Add your PostgreSQL connection string to the environment variables:
   ```env
   DATABASE_URL="postgresql://user:password@host:port/dbname"
   ```

### 🐍 2. Backend Setup (FastAPI)
Navigate to the backend directory and spin up your development server:
```bash
cd backend

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

# Install required dependencies
pip install -r requirements.txt

# Start the FastAPI server
uvicorn main:app --reload
```
The backend API documentation will be interactively available at: `http://localhost:8000/docs`

### ⚛️ 3. Frontend Setup (React)
Open a new terminal window, navigate to the frontend directory, and run the interface:
```bash
cd frontend

# Install package dependencies
npm install

# Start the local development server
npm run dev
```
The frontend interface will open natively at: `http://localhost:5173/`

---

## 🚀 Deployment

## 🚀 1-Click Cloud Deployment (Render)

We have included a pre-configured `render.yaml` blueprint file in this repository. This allows you to deploy both the React frontend and FastAPI backend online instantly without configuring servers manually.

### How to Deploy Online:
1. **Fork or Push** this code to your own public GitHub account.
2. Click the blue **Deploy to Render** button below:

[![Deploy to Render](https://render.com)](https://render.com)


3. Render will open automatically. If prompted, log into your free Render account.
4. Give your deployment group a name (e.g., `my-food-app`).
5. Render will scan the `render.yaml` file and request your database connection string. Paste your **PostgreSQL/Supabase Database URL** into the input field.
6. Click **Apply**. 

Render will automatically build your React frontend, install your FastAPI python packages, and provide you with a live, functioning URL for your application in under 3 minutes!


---

## 📄 License & Terms
This project source code is delivered "as-is" for development, educational, and commercial template use. Custom software deployment support, code debugging assistance, or external environment configurations are entirely the responsibility of the purchaser.
