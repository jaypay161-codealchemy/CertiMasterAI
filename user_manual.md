# CertiMasterAI User Manual

Welcome to CertiMasterAI! This guide will walk you through the process of setting up and using the software for your PMP exam preparation.

## 📋 Table of Contents
1. [Getting Started](#1-getting-started)
2. [Ollama Configuration](#2-ollama-configuration)
3. [Dashboard Overview](#3-dashboard-overview)
4. [Managing the Question Bank](#4-managing-the-question-bank)
5. [Importing Questions via AI](#5-importing-questions-via-ai)
6. [Generating and Taking Exams](#6-generating-and-taking-exams)
7. [Syncing from Excel](#7-syncing-from-excel)
8. [Troubleshooting](#8-troubleshooting)

---

## 🚀 1. Getting Started
To use CertiMasterAI, ensure both the **Frontend** and **Backend** are running.
- **Frontend URL**: `http://localhost:5173`
- **Backend URL**: `http://localhost:8000`

## 🤖 2. Ollama Configuration
Ollama is required for AI-powered features.
1. Download Ollama from [ollama.com](https://ollama.com).
2. Start the server with CORS enabled:
   ```cmd
   set OLLAMA_ORIGINS=*
   ollama serve
   ```
3. Pull a model (e.g., `llama3`):
   ```cmd
   ollama pull llama3
   ```
4. Access **Ollama Settings** from the dashboard to configure the host and model.

## 📊 3. Dashboard Overview
The dashboard provides a snapshot of your progress:
- **Metrics**: Total questions, exams taken, average score, and chapters covered.
- **Focus Areas**: Identify your weak chapters based on exam performance.
- **Quick Start**: Quick buttons to add, import, sync, or start an exam.

## 📚 4. Managing the Question Bank
- **Search**: Use the search bar to find questions by text.
- **Filtering**: Filters by Chapter, Topic, Question Type (MCQ/MSQ), and Difficulty.
- **Actions**: Edit or delete questions directly from the bank.

## ⚡ 5. Importing Questions via AI
1. Go to **Import via AI**.
2. Paste any text (raw content, PDF copy-paste).
3. Specify a **Chapter** and **Topic** (optional).
4. Click **Parse with AI**. The system will automatically structure the text into questions.
5. Review and select the questions you want to import.

## 📝 6. Generating and Taking Exams
1. Go to **Start Exam**.
2. Configure your exam:
   - Filter by chapter, topic, or difficulty.
   - Choose the number of questions and the time limit.
   - Enable **AI Smart Selection** for a balanced exam.
3. Once started, answer questions within the timer.
4. Review your **Results** at the end.

## 📂 7. Syncing from Excel
If you have questions in Excel files:
1. Place your `.xlsx` files in the backend's designated folder (`backend\excel file`).
2. Click **Sync Excel** on the dashboard.
3. The server will parse all questions and add them to your database.

## 🛠️ 8. Troubleshooting
- **Ollama Not Reachable**: Ensure the `OLLAMA_ORIGINS=*` variable is set and the server is running.
- **Empty Question Bank**: Ensure the backend is running and you have successfully synced Excel files or added questions manually.
- **Excel Not Syncing**: Check if the column name is exactly "Questions" in your spreadsheet.
