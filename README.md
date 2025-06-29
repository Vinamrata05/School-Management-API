# 🎓 School Management API

This project implements a School Management backend system using **Node.js**, **Express.js**, and **MySQL**, allowing users to add schools and retrieve a list of schools sorted by proximity. The API is:

* 🌐 **Hosted on Render**
* 🗄️ **Connected to a MySQL database deployed via Aiven**
* 📫 **Accessible via RESTful endpoints and testable through Postman**

## 🚀 Features

* Add new schools with name, address, latitude, and longitude
* List all schools sorted by proximity to user-provided coordinates
* Distance calculated using Haversine formula

---

## 📦 Tech Stack

* Node.js
* Express.js
* MySQL (hosted on Aiven)
* dotenv
* MySQL2

---

## 📬 API Endpoints

### ➕ POST `/addSchool`

Add a new school to the system.

**Request Body:**

```json
{
  "name": "Delhi School",
  "address": "New Delhi",
  "latitude": 28.6139,
  "longitude": 77.2090
}
```

**Deployed URL:**

```
POST https://school-management-api-zpvo.onrender.com/addSchool
```

---

### 📍 GET `/listSchools?latitude=...&longitude=...`

Returns schools sorted by distance from user’s location.

**Example:**

```
GET https://school-management-api-zpvo.onrender.com/listSchools?latitude=19.076&longitude=72.877
```

You can change the latitude and longitude parameters in the above URL to get the schools sorted by proximity.

---

## 🥪 Postman Collection

You can test the API using this Postman collection:

👉 [Download School Management API.postman\_collection.json](https://raw.githubusercontent.com/Vinamrata05/School-Management-API/main/School%20Management%20API.postman_collection.json)

🔗 Base URL for all requests: `https://school-management-api-zpvo.onrender.com`

---

## 🛠 Setup Instructions

### 1. Clone & Install

```bash
git clone https://github.com/Vinamrata05/School-Management-API.git
cd School-Management-API
npm install
```

### 2. Create `.env` file

```env
PORT=3000
DB_HOST=your-db-host
DB_USER=your-db-user
DB_PASSWORD=your-db-password
DB_NAME=your-db-name
SSL_CA_PATH=./certs/ca.pem
```

### 3. Start the server

```bash
# For development (auto-restart on changes)
npm run dev

# For production
npm run start
```
