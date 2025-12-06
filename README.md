# 🚀 TrueWrite Scan: AI-Powered Writing Assistant

TrueWrite Scan is a full-stack AI application designed to enhance writing integrity. It integrates state-of-the-art NLP models to provide real-time Grammar Checking, Plagiarism Detection, and AI Content Classification.

## 🌟 Key Features

* **📝 Advanced Grammar Checker:** Utilizes `language-tool-python` and custom rule sets to detect syntax and stylistic errors.
* **🔍 Semantic Plagiarism Detection:** Powered by `sentence-transformers` to detect paraphrased content, not just exact matches.
* **🤖 AI Content Detector:** Implements Hugging Face Transformers to analyze perplexity and burstiness, identifying machine-generated text.
* **📄 Multi-Format Support:** Parses text from `.txt`, `.docx`, and `.pdf` files.

## 🛠️ Tech Stack

### Frontend
* **Framework:** Next.js 13+ (React)
* **Styling:** Tailwind CSS
* **Deployment:** Vercel

### Backend
* **Framework:** FastAPI (Python)
* **ML Libraries:** PyTorch, Transformers, Scikit-learn, NumPy
* **Deployment:** Hugging Face Spaces (Dockerized)

## 🏗️ Architecture & Deployment Strategy

Running heavy ML models (PyTorch + JVM for Grammar) requires significant RAM. I implemented a **Split Deployment Strategy** to optimize performance on free-tier infrastructure:

1.  **Frontend (Vercel):** Handles UI/UX and client-side logic.
2.  **Backend (Hugging Face Spaces):** A custom Docker container running FastAPI.
    * **Why Docker?** To install System-level dependencies (`OpenJDK 21` for Grammar check, `build-essential` for Auth).
    * **Optimization:** Configured to use CPU-optimized PyTorch builds to reduce slug size and memory footprint.
