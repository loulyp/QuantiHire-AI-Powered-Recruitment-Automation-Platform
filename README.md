# QuantiHire: AI-Powered Recruitment Automation Platform

**QuantaHire** is an end-to-end AI recruitment platform that automates candidate screening, eliminates human bias, and delivers transparent feedback. It uses a two-stage **Retrieval-Augmented Generation (RAG)** pipeline to semantically match candidates to job descriptions, ensuring fast, fair, and explainable hiring decisions.


## The Problem
Traditional hiring is :
- **Inefficiency:** Recruiters manually screen hundreds of CVs per role, wasting weeks of productivity.
- **Human Bias:** Subjective decisions introduce gender, racial, and educational biases.
- **Opacity:** Candidates are rejected with zero feedback, creating a frustrating experience and damaging employer branding.

QuantaHire solves these issues by acting as an **"AI Recruiting Agent"** that handles parsing, matching, ranking, and feedback generation end-to-end.

---

## Features

### Admin Portal
- **Recruiter Validation:** Approve or reject recruiter registrations with certificate verification.
- **Platform Monitoring:** Real-time dashboards with KPIs (active jobs, users, applications, average match scores).
- **System Analytics:** View recruiter growth, job posting trends, and application status distributions.

### Recruiter Portal
- **Job Posting & Parsing:** Create jobs; AI auto-extracts skills and requirements from job descriptions.
- **AI Candidate Ranking:** Run the RAG pipeline to rank candidates by fit (initial score + final LLM score).
- **Agentic Re-ranking:** Provide feedback to the AI to dynamically re-rank candidates using LangGraph.
- **Explainable Feedback:** Generate and send personalized feedback reports to candidates.

### andidate Portal
- **CV Upload & Auto-Parsing:** Upload PDF/DOCX; AI extracts skills, experience, and education.
- **Big Five Personality Assessment:** Optional psychometric test for deeper candidate insights (decoupled from ranking).
- **Job Discovery & Tracking:** Browse jobs, apply, and track application status (In Review, Shortlisted, Accepted, Rejected).
- **Transparent Feedback:** Receive AI-generated feedback reports explaining why they were selected or rejected.

---
##  Tech Stack

| Category | Technology |
|----------|------------|
| **Language** | Python 3.10+ |
| **Backend Framework** | FastAPI + AntiGravity (Full-stack) |
| **Frontend** | React.js, HTML5, CSS3 |
| **Database** | MongoDB Atlas (11 collections) |
| **Primary LLM** | OpenAI GPT‑4o (Scoring, Parsing, Feedback) |
| **Baseline LLM** | Llama 3 via Ollama (Prototyping) |
| **Embedding Models** | `all-mpnet-base-v2`, OpenAI `ada-002` |
| **Vector Stores** | FAISS, ChromaDB |
| **RAG Frameworks** | LangGraph (Agentic RAG), RAGAnything |
| **Document Parsing** | PyMuPDF (fitz), MinerU, python-docx |
| **NLP / ML** | spaCy, scikit‑learn |
| **Email Service** | Resend / Gmail SMTP |
| **Hosting / Cloud** | AntiGravity (Google Cloud) |
| **Version Control** | GitHub |

## Results

| Metric | Score | Meaning |
|--------|-------|---------|
| **Precision@1 (P@1)** | **1.000** | Correct candidate ranked #1 in 100% of test cases. |
| **Recall@1 (R@1)** | **1.000** | Correct candidate always retrieved at the top. |
| **Mean Reciprocal Rank (MRR)** | **1.000** | First relevant candidate appeared at top on average. |
| **NDCG@10** | **1.000** | Perfect ranking order within the top 10 results. |
| **Test Coverage** | **170+** | All Admin, Recruiter, Candidate portal tests passed. |
| **CVs Processed** | **100+** | Real‑world test dataset across 5 job domains. |
