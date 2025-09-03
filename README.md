# Smart Restaurant Menu Assistant

![Full-Stack AI](https://img.shields.io/badge/Full-Stack-AI-blue)

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

## Detailed Roadmap

### Week 1 – Node.js + Express + PostgreSQL + JWT (15 hrs)

* Day 1: Setup Node.js, Express server, test route
* Day 2: PostgreSQL setup, create `users` and `restaurants` tables, Prisma init
* Day 3: Implement `/register` & `/login` endpoints with JWT auth
* Day 4: Test auth with Postman, protect sample route
* Day 5: Create restaurant routes (`POST /restaurants`, `GET /restaurants/:id`)
* Day 6: Setup React frontend, login/register forms, store JWT

### Week 2 – Menu Upload + AWS S3 (15 hrs)

* Day 1: AWS S3 setup, IAM keys
* Day 2: Upload route using Multer & aws-sdk, store `s3_url` in DB
* Day 3: List menus (`GET /restaurants/:id/menus`), integrate frontend
* Day 4: React file upload form, Axios POST
* Day 5: Test multiple uploads, check S3 & DB
* Day 6: Cleanup, error handling, Tailwind styling

### Week 3 – Python AI Microservice (15 hrs)

* Day 1: Python & FastAPI setup, basic route
* Day 2: `/parseMenu` endpoint accepting S3 URL, return dummy JSON
* Day 3: Download file from S3, extract text (PyPDF2/pytesseract)
* Day 4: Call OpenAI API, parse menu into structured JSON
* Day 5: Node calls Python service, insert JSON into `menu_items`
* Day 6: Display structured menu in React, test full flow

### Week 4 – AI Q\&A + Polish + Deploy (15 hrs)

* Day 1: Generate OpenAI embeddings for menu items, store in pgvector
* Day 2-3: AI chat endpoint: question → similarity search → GPT response
* Day 4: React chat UI, send question, display AI answer
* Day 5: Role-based auth, error handling, JWT refresh (optional)
* Day 6: Deployment: Node.js & Python services, frontend, DB, test full flow

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
