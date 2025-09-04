# Smart Restaurant Menu Assistant

## Description

AI-powered full-stack restaurant menu assistant. Restaurant owners can upload menus (PDF/image), automatically parsed by a Python AI microservice into structured dishes. Customers can browse menus and interact with an AI-powered chat to ask questions about menu items.

---

## Features

* JWT-based authentication (owners & customers)
* Menu upload with AWS S3 storage
* AI menu parsing via Python FastAPI microservice
* Structured menu display in React frontend
* AI-powered Q\&A on menu items
* PostgreSQL database with vector search for embeddings

---

## Tech Stack

**Frontend:** React, TailwindCSS, Axios
**Backend (Node.js):** Express, JWT, bcrypt, Multer, aws-sdk, Prisma/Sequelize
**Database:** PostgreSQL, pgvector
**Python AI Microservice:** FastAPI, Uvicorn, boto3, PyPDF2/pytesseract, OpenAI API, LangChain (optional)
**Cloud / Deployment:** AWS S3, AWS RDS / Supabase, Vercel/Netlify (frontend), Render / EC2 (backend), Docker

---

## 7-Week Roadmap

### Week 1 – Environment Setup & Backend Basics (15 hrs)

* Install Node.js, PostgreSQL, Python, and required libraries
* Set up GitHub repo with backend/frontend/python folders
* Build basic Express server with one test route
* Explore REST APIs, JSON, HTTP methods (GET, POST, etc.)

### Week 2 – Database & Authentication (15 hrs)

* Create database with `users` and `restaurants` tables
* Add `/register` and `/login` routes with bcrypt password hashing
* Implement JWT middleware for protected routes
* Test routes with Postman, document API endpoints

### Week 3 – React Frontend Basics (15 hrs)

* Initialize React project with Vite + TailwindCSS
* Build Login/Register forms, connect to backend APIs
* Store JWT in local storage, redirect after login
* Add basic navigation: Home, Login, Register pages

### Week 4 – Menu Upload + AWS S3 Integration (15 hrs)

* Set up AWS S3 bucket and IAM credentials
* Build file upload endpoint with Multer + aws-sdk
* Save S3 URL in database for each menu
* Build React file upload form connected to backend
* Test end-to-end: frontend → backend → S3 → DB

### Week 5 – Python AI Microservice (15 hrs)

* Set up FastAPI project with basic `/parseMenu` endpoint
* Add code to fetch menu files from S3
* Use PyPDF2/pytesseract to extract text from PDFs/images
* Send text to OpenAI API → parse into structured menu JSON
* Send structured menu data back to Node.js → store in DB

### Week 6 – AI Q\&A Chat Feature (15 hrs)

* Generate embeddings for menu items, store in pgvector/PostgreSQL
* Create Q\&A endpoint: question → similarity search → GPT answer
* Build simple React chat UI for customers
* Connect frontend → backend → AI Q\&A pipeline

### Week 7 – Testing, Deployment & Polish (15 hrs)

* Add role-based auth (owners vs customers)
* Test full flow: Register → Upload → Parse → Browse → Q\&A
* Deploy backend (Node.js + Python) on Render/AWS EC2
* Deploy frontend on Vercel/Netlify
* Deploy DB on AWS RDS or Supabase
* Write README with screenshots & final documentation

---

## Usage

1. Register as a restaurant owner or customer.
2. Login to access protected routes.
3. Owners upload menu files (PDF/image) to S3.
4. AI parses menus into structured dishes.
5. Customers browse menus and chat with AI.

---

## Screenshots / Demo

*(Optional: Add screenshots or GIFs of app in action)*

---

## License

MIT License
