# 🏆 CertiMasterAI — Advanced PMP AI Preparation Platform

CertiMasterAI is a professional-grade Project Management Professional (PMP) exam preparation platform. It uses **Local AI (Ollama)** to provide high-precision question categorization, smart exam generation, and automated data extraction while keeping all your study data private and offline.

---

## 🚀 Key Features

- **🧠 AI-Powered Categorization**: Automatically maps questions to the PMP Exam Content Outline (ECO) hierarchy (Domains, Tasks, and Enablers).
- **📋 Smart Exam Generation**: Intelligent selection of questions based on your weak areas and topic distribution.
- **⚡ AI Question Extraction**: Paste raw text or PDFs to instantly extract structured MCQs (Multiple Choice Questions) using LLMs.
- **📂 Excel Auto-Synchronization**: Manage thousands of questions in Excel and sync them into your study bank with a single click.
- **📊 Performance Analytics**: Visual dashboard to track progress across different ECO domains and focus tasks.
- **🌙 Premium Dark Mode**: High-performance, modern interface designed for long study sessions.

---

## 📋 Prerequisites for Running the Application

To use the AI features (Categorization, Extraction, Smart Exams), you must have **Ollama** installed and configured correctly on your machine.

### 1. Install Ollama
Download and install it from [ollama.com](https://ollama.com).

### 2. Configure Environment (Crucial for UI Connectivity)
For the web UI to talk to Ollama, you must set the `OLLAMA_ORIGINS` environment variable.

**On Windows (PowerShell):**
```powershell
$env:OLLAMA_ORIGINS="*"
ollama serve
```
*(Tip: You can add this to your system environment variables permanently to avoid running it every time.)*

### 3. Pull the Required Model
We recommend using **Llama 3** for the best balance of speed and intelligence:
```bash
ollama pull llama3
```

---

## 📂 How to Manage Your Excel Questions

CertiMasterAI allows you to import questions in bulk using local Excel files.

### 📍 Where to keep your files
Place your `.xlsx` files in the **`excel file/`** directory (located in the same folder as the application).

### 📝 Excel Requirements
- Your Excel file must have a column named **`Questions`**.
- Each row in the `Questions` column should contain the question text, options (A, B, C, D), correct option, and explanation.
- **Automatic Formatting**: The app uses advanced AI and Regex to parse complex text formats automatically, so "raw" question dumps are usually handled fine as long as they follow a standard A-D option format.

---

## 📖 Application Guide

### 1. Synchronizing Questions
- Open the application and navigate to the **Question Bank**.
- Click the **"Sync Excel"** button. The app will scan the `excel file/` directory and update your local database instantly.

### 2. Generating Smart Exams
- Go to the **Exam Center**.
- Choose your focus area (or let the AI decide).
- The AI will select the most relevant questions based on the PMP Exam Content Outline to ensure a balanced test.

### 3. Extracting from Text
- If you have questions in a PDF or a website, copy the text.
- Use the **"AI Extractor"** tool, paste the text, and click **Extract**.
- The app will convert the raw text into a structured MCQ format and add it to your bank.

---

## 🏗️ Development Setup (For Developers)

If you want to run the project from source or contribute:

### Backend (FastAPI)
```bash
cd backend
pip install -r requirements.txt
python server.py
```

### Frontend (React + Vite)
```bash
cd frontend
npm install
npm run dev
```

### Packaging into .exe
To create your own standalone Windows application:
```bash
python package_app.py
```
This will generate a `dist/CertiMasterAI.exe` file.

---

## ⚖️ License
Distributed under the MIT License. See `LICENSE` for more information.
