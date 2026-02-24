# Student CGPA API

A lightweight RESTful API built with **Express.js** to manage and query student academic performance records, powered by in-memory JSON data.

---

## Objective

This project demonstrates the fundamentals of building a RESTful backend using **Node.js** and **Express.js**. It exposes multiple GET endpoints — both static and dynamic — to retrieve, filter, and aggregate student CGPA records without any external database.

---

## Tech Stack

| Technology | Purpose |
|---|---|
| Node.js | JavaScript runtime |
| Express.js | Web framework and routing |
| CORS | Cross-origin request handling |
| In-Memory JSON | Data storage (no database required) |

---

## Project Structure

```
student-cgpa-api/
├── server.js        # Entry point — all routes and logic
├── package.json     # Project metadata and dependencies
├── .gitignore       # Ignored files (node_modules, etc.)
└── README.md        # Project documentation
```

---

## Implemented Routes

### Static Routes

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/students` | Returns all student records |
| GET | `/students/topper` | Returns the student with the highest CGPA |
| GET | `/students/average` | Returns the average CGPA of all students |
| GET | `/students/count` | Returns the total number of students |

### Dynamic Routes

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/students/:id` | Returns a student by their ID |
| GET | `/students/branch/:branchName` | Returns all students from a specific branch |

---

## Sample API URLs

```
# Get all students
GET https://student-cgpa-api-1-q73f.onrender.com/students

# Get the topper
GET https://student-cgpa-api-1-q73f.onrender.com/students/topper

# Get average CGPA
GET https://student-cgpa-api-1-q73f.onrender.com/students/average

# Get total student count
GET https://student-cgpa-api-1-q73f.onrender.com/students/count

# Get student by ID
GET https://student-cgpa-api-1-q73f.onrender.com/students/3

# Get students by branch
GET https://student-cgpa-api-1-q73f.onrender.com/students/branch/CSE
```

---

## Steps to Run Locally

**Prerequisites:** Make sure [Node.js](https://nodejs.org) is installed on your machine.

**1. Clone the repository**
```bash
git clone https://github.com/mananjani2102/Student-cgpa-api.git
cd Student-cgpa-api
```

**2. Install dependencies**
```bash
npm install
```

**3. Start the server**
```bash
node server.js
```

**4. Test the API**

Open your browser or Postman and navigate to:
```
http://localhost:5000/students
```

---

## Sample JSON Response

```json
// GET /students/topper
{
  "id": 2,
  "name": "Ayesha Khan",
  "branch": "CSE",
  "cgpa": 9.8
}
```

```json
// GET /students/average
{
  "averageCGPA": 8.45
}
```

---

## API Documentation

Full API documentation is available on Postman:  
https://documenter.getpostman.com/view/50839334/2sBXcGCe9h

---

## Deployed Link

Live API hosted on Render:  
https://student-cgpa-api-1-q73f.onrender.com

> Note: The free Render instance may spin down after inactivity. The first request might take up to 30 seconds to respond.

---

## GitHub Repository

https://github.com/mananjani2102/Student-cgpa-api

---

## Learning Outcomes

- Designed and implemented RESTful GET APIs using Express.js
- Used dynamic route parameters (`:id`, `:branchName`) for flexible querying
- Performed server-side filtering and aggregation on in-memory JSON data
- Returned structured and consistent JSON responses
- Configured CORS middleware for cross-origin access
- Deployed a live backend API to a cloud platform (Render)
- Documented and tested all API endpoints using Postman
