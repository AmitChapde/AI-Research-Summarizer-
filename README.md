# Research Brief AI

A small web app that generates structured research briefs from multiple links.

You can paste 5–10 URLs (articles, blogs, docs), and the app will fetch the content, clean it, and generate a summarized research brief using an LLM.


---

## 🔗 Live Demo

*(Add your deployed URL here)*


---

## ✨ Features

* Paste multiple URLs and generate a structured research brief
* Extracts readable content from each link
* Generates:

  * Summary
  * Key points
  * Conflicting claims (if any)
  * “What to verify” checklist
  * Source citations with snippets
* Graceful handling of failed links (skipped sources shown)
* Saves last 5 generated briefs (MongoDB)
* History page
* Status page (backend, DB, LLM health)

---

## 🧠 Tech Stack

**Frontend**

* React + TypeScript
* Vite
* Basic CSS 

**Backend**

* Node.js + Express + TypeScript
* MongoDB (Mongoose)
* Google Gemini API (LLM)

---

## 🧪 How It Works

1. User pastes multiple URLs
2. Backend fetches HTML and extracts readable text
3. Low-quality sources are filtered out
4. Cleaned content is sent to the LLM
5. LLM returns structured JSON
6. Result is saved and returned to UI


---

## 🚀 How to Run Locally

### 1. Clone repo

```bash
git clone <repo-url>
cd research-brief-ai
```

---

### 2. Setup backend

```bash
cd server
npm install
```

Create `.env` using `.env.example`:

```
PORT=5000
MONGO_URI=mongodb://127.0.0.1:27017/research-ai
GEMINI_API_KEY=your_key_here
```

Run backend:

```bash
npm run dev
```

---

### 3. Setup frontend

```bash
cd client
npm install
```

Create `.env`:

```
VITE_API_URL=http://localhost:5000
```

Run frontend:

```bash
npm run dev
```

---

## 🧩 What Is Done

* Core research brief generation
* Multi-source content extraction
* Structured LLM output
* Partial success handling 
* History persistence (last 5 briefs)
* Status page
* Basic validation and error handling

---

## ⚠️ What Is Not Done / Known Limitations

* Some modern sites (Medium, social media, JS-heavy pages) are hard to scrape
* No auth
* LLM output depends on input quality

---

## 🛡️ Basic Safety Measures

* Input validation on URLs
* Graceful fallback when sources fail
* Helmet for basic security headers
* No API keys committed

---


## 📄 Other Docs

* `AI_NOTES.md` – how AI was used during development
* `PROMPTS_USED.md` – prompts used while building
* `ABOUTME.md` – short intro and resume
# AI-Research-Summarizer-
