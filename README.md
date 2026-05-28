# Spotify Clone Backend 🎵

A scalable backend API for a Spotify-inspired music streaming platform built using Node.js, Express.js, MongoDB, JWT Authentication, and ImageKit cloud storage.

---

# 📌 Project Overview

This project is a backend system for a music streaming application similar to Spotify. It provides secure authentication, role-based authorization, music upload functionality, album management, and protected API routes.

The backend is designed using a clean and scalable architecture with separate folders for controllers, models, middleware, routes, services, and database configuration.

This project demonstrates practical implementation of:

* REST API development
* Authentication & Authorization
* JWT-based login system
* Secure password hashing
* File upload handling
* Cloud storage integration
* MongoDB relationships
* Express middleware architecture
* Backend project structuring

---

# ✨ Features

## 🔐 Authentication System

* User Registration
* User Login
* JWT Authentication
* Cookie-based authentication
* Password hashing using bcryptjs

---

## 👤 Role-Based Authorization

* Artist role support
* Protected artist routes
* Protected user routes
* Middleware-based access control

---

## 🎵 Music Management

* Upload music files
* Store music metadata
* Cloud upload integration
* Fetch all musics
* Artist-based music ownership

---

## 💿 Album Management

* Create albums
* Associate multiple songs with albums
* Fetch all albums
* Fetch album details by ID
* MongoDB population support

---

## ☁️ Cloud Storage

* File upload using Multer
* Cloud storage using ImageKit
* Dynamic file URL generation

---

# 🛠️ Tech Stack

## Backend Framework

* Node.js
* Express.js

---

## Database

* MongoDB
* Mongoose

---

## Authentication & Security

* JSON Web Token (JWT)
* bcryptjs
* cookie-parser
* dotenv

---

## File Upload & Storage

* Multer
* ImageKit

---

# 📦 NPM Packages Used

```bash
npm install express mongoose jsonwebtoken bcryptjs cookie-parser dotenv multer imagekit
```

---

# 📂 Folder Structure

```bash
Spotify-Clone-Backend/
│
├── src/
│   ├── controllers/
│   │   ├── auth.controller.js
│   │   └── music.controller.js
│   │
│   ├── db/
│   │   └── db.js
│   │
│   ├── middleware/
│   │   └── auth.middleware.js
│   │
│   ├── models/
│   │   ├── album.model.js
│   │   ├── music.model.js
│   │   └── user.model.js
│   │
│   ├── routes/
│   │   ├── auth.routes.js
│   │   └── music.routes.js
│   │
│   ├── services/
│   │   └── storage.service.js
│   │
│   └── app.js
│
├── .gitignore
├── package.json
├── package-lock.json
└── server.js
```

---

# ⚙️ Environment Variables

Create a `.env` file in the root directory.

```env
PORT=3000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key

IMAGEKIT_PUBLIC_KEY=your_public_key
IMAGEKIT_PRIVATE_KEY=your_private_key
IMAGEKIT_URL_ENDPOINT=your_url_endpoint
```

---

# 🚀 Installation & Setup

## 1️⃣ Clone Repository

```bash
git clone https://github.com/DhruvTalati/spotify-clone-backend
```

---

## 2️⃣ Move Into Project Directory

```bash
cd spotify-clone-backend
```

---

## 3️⃣ Install Dependencies

```bash
npm install
```

---

## 4️⃣ Configure Environment Variables

Create a `.env` file and add all required credentials.

---

## 5️⃣ Start Server

```bash
npm start
```

OR

```bash
npm run dev
```

---

# 🌐 API Endpoints

# 🔐 Authentication Routes

## Register User

```http
POST /api/auth/register
```

### Request Body

```json
{
  "username": "sample",
  "email": "sample@gmail.com",
  "password": "123456",
  "role": "artist"
}
```

---

## Login User

```http
POST /api/auth/login
```

### Request Body

```json
{
  "email": "sample@gmail.com",
  "password": "123456"
}
```

---

# 🎵 Music Routes

## Upload Music

```http
POST /api/music/upload
```

### Form Data

| Key   | Type |
| ----- | ---- |
| music | File |
| title | Text |

---

## Get All Musics

```http
GET /api/music
```

---

# 💿 Album Routes

## Create Album

```http
POST /api/music/album
```

### Request Body

```json
{
  "title": "My Album",
  "musics": ["music_id_1", "music_id_2"]
}
```

---

## Get All Albums

```http
GET /api/music/albums
```

---

## Get Album By ID

```http
GET /api/music/albums/:albumId
```

---

# 🔒 Authentication Flow

1. User registers or logs in
2. JWT token is generated
3. Token is stored in cookies
4. Protected routes verify JWT
5. Middleware controls access permissions

---

# 🧠 Concepts Implemented

* MVC Architecture
* Middleware Chaining
* JWT Authentication
* Role-based Authorization
* MongoDB Population
* File Upload Handling
* Cloud File Storage
* RESTful API Design
* Environment Variable Security
* Async/Await Handling
* Express Routing

---

# 🚧 Future Improvements

* Song Streaming
* Playlist System
* Like & Favorite Feature
* Music Search
* Audio Player Integration
* Admin Dashboard
* User Profile System
* Refresh Tokens
* Music Recommendation System
* Frontend Integration
* Deployment

---

# 👨‍💻 Author

## Dhruv Talati

* GitHub: https://github.com/DhruvTalati

---

# ⭐ Support

If you liked this project, consider giving it a star on GitHub ⭐
