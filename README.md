# 💼 AI Resume Screening System

An intelligent web application that analyzes resumes and ranks candidates based on job description using AI.

---

## 🌐 Live Demo

🔗 https://ai-resume-screening-jet.vercel.app/

👉 Try uploading resumes and see AI ranking in action!

---

## 🔥 Features

- 📄 Upload multiple resumes (PDF)
- 🧠 AI-powered resume analysis
- 📊 Candidate ranking with match score
- ✅ Strengths & ❌ gaps identification
- ⚡ Fast and responsive UI

---

## 🛠️ Tech Stack

- **Frontend** — HTML5, CSS3 (Custom Premium Dark Theme), Vanilla JS
- **Backend Framework** — Python 3, Flask (Vercel Serverless Functions)
- **AI / LLM** — Groq API (Llama 3.3 70B Model)
- **PDF Processing** — PyPDF2 
---


## Output Format

| Rank | Candidate | Score | Strengths | Gaps | Recommendation |
|------|-----------|-------|-----------|------|----------------|
| 1 | Candidate A | 85 | Strong SQL, Tableau expert | Limited cloud exp | Strong Fit |
| 2 | Candidate B | 62 | Good Python | No visualization tools | Moderate Fit |
| 3 | Candidate C | 28 | Creative design skills | No data/SQL skills | Not Fit |


## Setup & Run Locally

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/sindhura082005/AI-Resume-Screening-System.git
cd AI-Resume-Screening-System

### 1. Install Dependencies
```bash
pip install -r requirements.txt
```

### 2. Configure API Key
Create a `.env` file in the root directory and add your Groq API key:
```env
GROQ_API_KEY=gsk_your_api_key_here
```

### 3. Run the Servers
Since this app separates the backend and frontend:

**Terminal 1 (Backend API):**
```bash
python api/index.py
# Server will run on http://127.0.0.1:5000
```

**Terminal 2 (Frontend UI):**
```bash
python -m http.server 8505
# Open your browser and go to http://localhost:8505
```
---

### 4. Use the App
1. Paste the **Job Description** in the sidebar.
2. Upload **resume PDFs** (you can accumulate up to 10 files before screening).
3. Click **Screen Resumes**.
4. View ranked results, scores, and individual analysis cards.

## Deployment on Vercel
This repository is configured out-of-the-box for deployment on **Vercel**.
1. Import the repository in Vercel.
2. Vercel will auto-detect the `vercel.json` routing configuration.
3. Add your `GROQ_API_KEY` to Vercel's Environment Variables.
4. Hit Deploy!

---

## Scoring Criteria

| Score Range | Recommendation | Meaning |
|-------------|---------------|---------|
| 80–100 | Strong Fit | Meets most/all key requirements |
| 50–79 | Moderate Fit | Meets some requirements, has notable gaps |
| 0–49 | Not Fit | Lacks critical requirements |
