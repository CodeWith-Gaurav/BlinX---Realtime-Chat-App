# 🚀 BlinX - Realtime Chat App

**BlinX** is a full-stack, real-time chat application built on the **MERN stack**.  
It offers instant messaging, secure authentication, thematic customization, and robust cloud-based media sharing.

---

## ✨ Features

- **💬 Real-time Messaging:**  
  Powered by **Socket.io** for instant, bidirectional communication between users.

- **🔐 Secure Authentication:**  
  User login and signup with **hashed passwords** (`bcryptjs`) and **session management** via **JWT (JSON Web Tokens)** stored in secure HTTP-only cookies.

- **☁️ Cloud Media Sharing:**  
  Seamless image sharing using **Cloudinary** for scalable, external storage.

- **🎨 Theming & Customization:**  
  Multiple color themes managed via **Zustand** and **Daisy UI**, allowing users to personalize their chat environment  
  *(e.g., Acid, Night, Sunset themes)*.

- **👥 Contact Management:**  
  Sidebar displays all users and highlights users currently online.

- **📱 Responsive UI:**  
  Built with **React** and styled using **Tailwind CSS** for a clean, modern, and mobile-friendly interface.

---

## 🛠️ Tech Stack

BlinX is a **full-stack MERN application** split into two main services — **Frontend** and **Backend**.

---

### 🖥️ Frontend

| **Technology**       | **Purpose** |
|-----------------------|-------------|
| **React**             | Core JavaScript library for building the user interface. |
| **Vite**              | Next-generation frontend tooling for fast development and bundling. |
| **Zustand**           | Lightweight and scalable state management for global state (e.g., auth, chat, theme). |
| **Tailwind CSS & Daisy UI** | Utility-first CSS framework + component library for rapid, thematic styling. |
| **Axios**             | Promise-based HTTP client for making API requests. |

---

### ⚙️ Backend

| **Technology**       | **Purpose** |
|-----------------------|-------------|
| **Node.js & Express** | Runtime environment and web framework for building REST APIs. |
| **MongoDB & Mongoose** | NoSQL database and ODM library for managing `User` and `Message` models. |
| **Socket.io**         | Enables real-time, low-latency, two-way communication between users. |
| **JWT (JSON Web Tokens)** | Secure and stateless authentication system. |
| **bcryptjs**          | Library for hashing and securing user passwords. |
| **Cloudinary**        | Cloud-based service for managing and storing message images and profile pictures. |

---
## ⚙️ Installation and Setup

---

### 🧩 **Prerequisites**

Before starting, ensure you have the following installed and configured:

- **Node.js** (v18 or later)
- **MongoDB** (Local instance or MongoDB Atlas connection string)
- **Cloudinary** account credentials

---

### 1️⃣ **Initial Setup and Dependencies**

The root `package.json` includes a build script to handle installations in both directories (backend and frontend).

```bash
# 1. Clone the repository
git clone <YOUR_REPO_LINK>
cd chat_app

# 2. Install all dependencies (Backend and Frontend)
npm run build 
# This command executes:
# - npm install --prefix backend 
# - npm install --prefix frontend 
# - npm run build --prefix frontend (to create the production build)
```
## 2️⃣ Environment Variables Configuration

You must create and configure **`.env` files** for both **backend** and **frontend** directories to ensure proper communication between the servers and external services.

---

### 🗄️ a. Backend Configuration

**📁 Path:** `chat_app/backend/.env`

The backend `.env` file contains all environment variables necessary for connecting to MongoDB, handling authentication, and integrating with Cloudinary for media uploads.

Create a file named `.env` inside the `backend` folder and add the following variables:

```bash
# Server Configuration
PORT=5001

# MongoDB Database Connection
MONGODB_URI="<YOUR_MONGODB_CONNECTION_STRING>"

# JWT Secret Key
JWT_SECRET="<A_LONG_SECURE_SECRET_KEY>"

# Cloudinary Credentials
CLOUDINARY_CLOUD_NAME="<YOUR_CLOUD_NAME>"
CLOUDINARY_API_KEY="<YOUR_API_KEY>"
CLOUDINARY_API_SECRET="<YOUR_API_SECRET>"
```

## 💻 Frontend Configuration

**📁 Path:** `chat_app/frontend/.env`

Create a file named `.env` in the **frontend** folder to set the API base URL for your application.

```bash
VITE_BASE_URL=http://localhost:5001/api
```

## ▶️ Running the Application

You will need two separate terminal windows to run the backend and frontend concurrently.

- Start the Backend (API Server)
The backend runs on port 5001 (as defined in .env).

```bash
cd backend

# For Production (using `node`)
npm start 

# For Development (using `nodemon` for automatic restarts)
npm run dev 
```
- Start the Frontend (Development Server)
The frontend development server typically runs on http://localhost:5173.

```bash
cd frontend

# Start the Vite development server
npm run dev
```
- Once both servers are running, open your web browser and navigate to http://localhost:5173 to access the BlinX chat application.

## 🤝 Contribution

Contributions are always welcome! 💡  

If you find any bugs, issues, or have suggestions for new features or improvements:

- 🐛 **Open an issue** describing the problem or idea.  
- 🔧 **Submit a pull request** with your proposed changes.  

Please make sure your code follows the existing style and includes clear commit messages.  
Together, we can make **BlinX** even better! 🚀
