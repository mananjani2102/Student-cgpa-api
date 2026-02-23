# Student CGPA API

## Objective

This project is a RESTful API built using Express.js that manages student academic performance records using an in-memory JSON array.

The API supports multiple GET routes including static and dynamic routes.

---

## Technologies Used

- Node.js
- Express.js
- CORS Middleware
- In-Memory JSON Data

---

## Implemented Routes

### Static Routes

GET /students  
GET /students/topper  
GET /students/average  
GET /students/count  

### Dynamic Routes

GET /students/:id  
GET /students/branch/:branchName  

---

## Sample API URLs

http://localhost:5000/students  
http://localhost:5000/students/topper  
http://localhost:5000/students/average  
http://localhost:5000/students/count  
http://localhost:5000/students/3  
http://localhost:5000/students/branch/CSE  

---

## How to Run Locally

1. Clone the repository  
2. Run:

   npm install

3. Start server:

   node server.js

4. Open in browser or Postman:

   http://localhost:5000/students

---

## Deployment

Deployed on Render:

https://your-render-link.onrender.com

---

## Learning Outcomes

- Designed RESTful GET APIs
- Implemented dynamic route parameters
- Performed server-side filtering and aggregation
- Returned structured JSON responses
- Deployed backend API to production
- Documented APIs using Postman
