# 🎓 School Management API

A Node.js + Express.js backend with MySQL that allows adding schools and retrieving them sorted by distance from the user's location.

## 🚀 Features

* Add new schools with name, address, latitude, and longitude
* List all schools sorted by proximity to user-provided coordinates
* Distance calculated using Haversine formula

---

## 📦 Tech Stack

* Node.js
* Express.js
* MySQL
* dotenv
* MySQL2

---

## 📬 API Endpoints

### ➕ POST `/addSchool`

Add a new school to the system.

**Request Body:**

```json
{
  "name": "Delhi Public School",
  "address": "RK Puram, New Delhi",
  "latitude": 28.5672,
  "longitude": 77.2100
}
```

---

### 📍 GET `/listSchools?latitude=...&longitude=...`

Returns schools sorted by distance from user’s location.

**Example:**

```
GET /listSchools?latitude=28.6139&longitude=77.2090
```

---

## 🥪 Postman Collection

You can test the API using this Postman collection:

👉 [Download School Management API.postman_collection.json](https://raw.githubusercontent.com/Vinamrata05/School-Management-API/main/School%20Management%20API.postman_collection.json)

🔗 Base URL for all requests: `https://your-live-url.onrender.com`

For example:

* `POST https://your-live-url.onrender.com/addSchool`
* `GET https://your-live-url.onrender.com/listSchools?latitude=28.6139&longitude=77.2090`

---

## 🛠 Setup Instructions

### 1. Clone & Install

```bash
git clone https://github.com/YOUR_USERNAME/school-api.git
cd school-api
npm install
```

### 2. Create `.env` file

```env
PORT=3000
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_mysql_password
DB_NAME=school_db
```

### 3. Start the server

```bash
# For development (auto-restart on changes)
npm run dev

# For production
npm run start
```
