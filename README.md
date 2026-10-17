# 🚀 JobMatch AI – Smart Resume Matching System

A full-stack AI-powered job matching platform that intelligently connects job seekers with relevant opportunities and helps recruiters identify the best candidates using advanced Natural Language Processing (NLP) and semantic similarity.

---

## 🌟 Overview

JobMatch AI analyzes resumes and job descriptions using both **keyword-based** and **semantic AI techniques** to generate an accurate match score. It provides detailed insights into skills, experience, and missing requirements — helping users improve their chances of selection.

---

## ✨ Features

### 👩‍💻 For Job Seekers

* 📄 Upload resumes (PDF/DOCX)
* 🎯 Get AI-based match percentage
* 📊 Detailed breakdown (skills, experience, education)
* 💡 Personalized improvement suggestions
* 🔍 Browse and apply for jobs

---

### 🧑‍💼 For Recruiters

* 🛠️ Create job postings easily
* 👥 View candidate applications
* 📈 Sort candidates by match score
* 📑 Resume analysis with highlights
* 📸 Extract job data from images (OCR)

---

## 🧠 AI / NLP Implementation

This project uses multiple NLP techniques:

### 🔹 1. TF-IDF (Term Frequency - Inverse Document Frequency)

* Identifies important keywords
* Used for keyword-based matching

---

### 🔹 2. Cosine Similarity

* Measures similarity between vectors
* Used for comparing resume & job vectors

---

### 🔹 3. SBERT (Sentence-BERT) ⭐

* Deep learning-based semantic model
* Understands meaning (not just keywords)
* Handles different wordings with same meaning

---

## 🔗 System Architecture

```text
Frontend (React)
        ↓
Backend (Node.js / Express)
        ↓
SBERT API (Python Flask)
        ↓
Semantic Similarity Score
```

👉 This follows a **microservice architecture**, where:

* Node.js handles application logic
* Python handles AI model

---

## 🛠️ Tech Stack

### 🔹 Frontend

* React.js
* Vite
* Tailwind CSS
* React Router

---

### 🔹 Backend

* Node.js
* Express.js
* MongoDB (Mongoose)
* JWT Authentication

---

### 🔹 AI / NLP

* natural (TF-IDF)
* string-similarity
* SBERT (sentence-transformers in Python)
* Cosine Similarity

---

## 🚀 Installation & Setup

### 📌 Prerequisites

* Node.js (v16+)
* MongoDB
* Python 3.x
* npm

---

## 📥 Step 1: Clone Repository

```bash
git clone https://github.com/Sakshiwalunj5/JobMatchAI.git
cd JobMatchAI
```

---

## 📦 Step 2: Install Dependencies

```bash
npm install
```

---

## 🐍 Step 3: Install Python Packages

```bash
pip install flask sentence-transformers
```

---

## ⚙️ Step 4: Environment Setup

The `.env.server` file is already included in the project with the following configuration:

```env
PORT=5003
NODE_ENV=development
MONGODB_URI=mongodb://localhost:27017/jobmatch-ai
SESSION_SECRET=jobmatch-ai-super-secret-session-key-2024
CORS_ORIGIN=http://localhost:3000
```

**Note:** Make sure MongoDB is running on your system before starting the application.

---

## ▶️ Step 5: Run the Project

### 🔹 Option A: Run Everything Together (Recommended)

**Terminal 1: Start Python SBERT API**
```bash
python sbert_api.py
```
This will run on `http://127.0.0.1:5000`

**Terminal 2: Start Backend & Frontend**
```bash
npm start
```
This runs both services concurrently using the `concurrently` package.

---

### 🔹 Option B: Run Services Individually

If you prefer to run services separately, open three terminals:

**Terminal 1: Python SBERT API**
```bash
python sbert_api.py
```

**Terminal 2: Backend Server**
```bash
npm run server:dev
```

**Terminal 3: Frontend Dev Server**
```bash
npm run dev
```

---

## 🌐 Access URLs

| Service   | URL                   |
| --------- | --------------------- |
| Frontend  | http://localhost:3000 |
| Backend   | http://localhost:5003 |
| SBERT API | http://127.0.0.1:5000 |

**Note:** The frontend and backend ports may vary if they are already in use. The application will automatically use the next available port. Check the terminal output for the actual URLs.

---

## 🔧 Troubleshooting

### Port Already in Use
If you get a "Port already in use" error:

**Windows:**
```bash
netstat -ano | find "5003"
taskkill /PID <PID> /F
```

**Mac/Linux:**
```bash
lsof -i :5003
kill -9 <PID>
```

### MongoDB Connection Error
Make sure MongoDB is running:
- **Windows:** Start MongoDB service from Services
- **Mac:** `brew services start mongodb-community`
- **Linux:** `sudo systemctl start mongod`

### Frontend Cannot Reach Backend
If you see "Cannot reach server" error:
1. Verify backend is running on port 5003
2. Clear browser cache and refresh
3. Check if CORS_ORIGIN in `.env.server` matches your frontend URL

---

## 📁 Project Structure

```text
smart-resume-matcher/
│
├── src/                      # Frontend (React)
├── server/                   # Backend (Node.js)
│   ├── routes/
│   ├── models/
│   ├── controllers/
│   └── utils/
│       └── nlpMatcher.js     # Matching logic (TF-IDF + SBERT)
│
├── public/
├── sbert_api.py              # SBERT Python API
├── .env.server
└── package.json
```

---

## 🎯 Matching Algorithm

Final score is calculated using:

```text
Final Score =
0.25 × TF-IDF +
0.25 × Skills Match +
0.15 × String Similarity +
0.35 × SBERT Semantic Similarity
```

---

## 🔥 Key Highlights

* 🤖 AI-powered resume analysis
* 🧠 Semantic understanding using SBERT
* ⚡ Real-time scoring system
* 📊 Multi-factor evaluation
* 🏗️ Scalable microservice architecture

---

## 🔮 Future Enhancements

* GPT-based resume suggestions
* Email notifications
* Advanced analytics dashboard
* Mobile app (React Native)
* Multi-language support

---

## 🤝 Contributing

1. Fork repository
2. Create feature branch
3. Commit changes
4. Push to GitHub
5. Create Pull Request

---

## 📄 License

MIT License

---

## 🙏 Acknowledgments

* Sentence Transformers (SBERT)
* React & Node.js community
* Inspired by LinkedIn & modern job platforms

---

