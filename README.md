# 📦 URL Shortener Backend

This is the **Backend API** for the URL Shortener application. It provides RESTful endpoints for URL shortening, user authentication, and click tracking. Built with **Node.js**, **Express**, and **MongoDB**.

## 🚀 Features

- 🔐 User Authentication (Login)
- 🔗 URL Shortening and Redirection
- 📊 Click Tracking (Analytics)
- 🧩 Modular Code Structure
- 🌐 CORS Enabled for Frontend Communication

---

## 📁 Project Structure

```
backend/
│
├── controllers/
│   └── url.js             # Business logic for shortening and redirecting URLs
│
├── models/
│   ├── Click.js           # Mongoose model for storing click stats
│   ├── Url.js             # Mongoose model for shortened URLs
│   └── User.js            # Mongoose model for users
│
├── routes/
│   └── routes.js          # All route definitions (URLs, login, analytics)
│
├── connection.js          # MongoDB database connection
├── index.js               # Main server entry point
├── .env                   # Environment variables (MONGO_URI, PORT, JWT_SECRET)
├── package.json           # Project metadata and dependencies
└── .gitignore             # Files and folders to ignore in git
```

---

## 🔧 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/url-shortener-backend.git
cd url-shortener-backend
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Create a `.env` File

```env
PORT=5000
MONGO_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/url-shortener
JWT_SECRET=your_jwt_secret
```

### 4. Run the Server

```bash
npm start
```

The server will run at `http://localhost:5000`.

---

## 🔌 API Endpoints

### Authentication

- `POST /api/login` — Authenticate user

### URL Management

- `POST /api/shorten` — Shorten a long URL
- `GET /:shortId` — Redirect to original URL
- `GET /api/urls` — Get all shortened URLs (authenticated)
- `GET /api/clicks/:shortId` — Get click analytics

---

## 🛠 Tech Stack

- **Node.js** + **Express**
- **MongoDB** + **Mongoose**
- **JWT** for authentication
- **Dotenv** for environment management

---

## 📬 Contact

For any queries or feedback, feel free to reach out!
