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
* **Deployment:** Cloudfare Pages

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

# 🛡️ TrueWrite Scan: AI-Powered Writing Assistant

> **TrueWrite Scan** is a production-grade SaaS platform designed to analyze, validate, and enhance written content using advanced Natural Language Processing (NLP), Machine Learning, and transformer-based AI models.

It delivers **accurate writing assessment, grammar intelligence, semantic analysis, and document validation** through a secure, scalable, and modern cloud-native architecture.

---

## 📘 Overview

TrueWrite Scan provides an end-to-end AI-driven pipeline for evaluating textual content across multiple dimensions including:
- linguistic quality
- grammatical correctness
- semantic similarity
- structural coherence
- document integrity (PDF / DOCX)

The platform is engineered with **enterprise-level security practices**, **modular microservice-style architecture**, and **model-centric AI workflows**, making it suitable for academic, professional, and SaaS-scale deployments.

---

## 🎯 Core Capabilities

- 🧠 Transformer-based NLP analysis  
- ✍️ Advanced grammar & language correction  
- 📊 Semantic similarity and vector-based scoring  
- 📄 PDF and DOCX document ingestion & processing  
- 🔐 JWT-based authentication & secure APIs  
- ⚡ High-performance FastAPI backend  
- 🌐 Cloud deployment with public inference access  

---

## 🏗️ System Architecture

### 🔹 Backend
- **FastAPI** — High-performance async API framework  
- **Uvicorn (standard)** — ASGI production server  
- **JWT Authentication** — Secure token-based access  
- **Passlib (bcrypt)** — Password hashing  
- **Python Multipart** — File uploads  
- **Email validation & reporting utilities**

### 🔹 AI / ML Stack
- **PyTorch (CPU-only)** — Model inference  
- **Transformers** — NLP pipelines  
- **Sentence Transformers** — Embedding & similarity analysis  
- **Scikit-learn & NumPy** — Feature processing  
- **GECToR** — Grammar Error Correction  
- **LanguageTool** — Linguistic validation  

### 🔹 Document Processing
- **python-docx** — DOCX parsing  
- **PyPDF2** — PDF reading  
- **ReportLab** — PDF generation & reporting  

### 🔹 Frontend
- **HTML**
- **Tailwind CSS**
- **Vanilla JavaScript**

### 🔹 Databases
- **MongoDB Atlas** — Unstructured & AI-related data  
- **PostgreSQL** — Relational & transactional data  
- **Supabase** — Auth, storage, and auxiliary services  

### 🔹 Deployment
- **Hugging Face Spaces** — Model hosting & API exposure  

---

## 🚀 Workflow Overview

1. User uploads text or document (PDF / DOCX)
2. Secure API authentication is validated
3. Text is parsed and normalized
4. AI models perform:
   - grammar analysis
   - semantic scoring
   - linguistic evaluation
5. Structured results are generated
6. Optional PDF reports are produced
7. Results are returned via REST API

---

## 📂 Supported Inputs
- Raw text
- PDF documents
- DOCX documents

## 📤 Outputs
- Grammar and correction feedback
- Semantic similarity scores
- Structured AI evaluation reports
- Downloadable PDFs

---

## 🔐 Security & Compliance
- Environment-based secrets (`.env`)
- No hardcoded credentials
- Encrypted password storage
- Token-based access control
- Safe file handling and validation

---

## 🧠 Why TrueWrite Scan Matters

- Demonstrates real-world AI SaaS engineering
- Combines ML research with production APIs
- Designed for scalability and maintainability
- Clean separation of AI logic and API services
- Suitable for academic, enterprise, and startup use cases

---

## ⚠️ Usage Restrictions

This repository and platform are **NOT open source**.

Unauthorized use, copying, redistribution, or modification of:
- source code
- AI models
- datasets
- UI assets
- logos and branding

is **strictly prohibited**.

See `LICENSE.txt` and `NOTICE.txt` for full legal terms.

---

## 📬 Contact

For licensing inquiries, partnerships, or professional communication:

**Author:** Gopal Krushna Mahapatra  

📧 Email: mahapatragopalkrushna34@gmail.com  
💼 LinkedIn: https://www.linkedin.com/in/gopal-krushna-mahapatra-3a974928b
🧑‍💻 GitHub: https://github.com/Gopal-star2005  

---

*TrueWrite Scan** — engineered for authenticity, precision, and trust.*
