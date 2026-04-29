<div align="center">

# Madhu Vishwanath Burra

**AI Engineer · LLM Systems · Agentic AI · Local Inference**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/madhu-vishwanath-burra/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:madhuv435@gmail.com)

</div>

---

## About Me

MS Applied Data Science @ SJSU (May 2025). Building production AI systems at the intersection of LLM inference, agent orchestration, and evaluation infrastructure.

Currently at **ASI Analytics** — built a LangGraph-based insurance claims processing pipeline in production. Two-prompt LLM architecture with OCR intake, multi-source RAG retrieval, grounded citations with PDF page numbers, and five-category discrepancy detection. Evaluation via human-in-the-loop, Pydantic structured output, and metadata grounding.

Running a local AI inference stack on an **RTX 3090** with LM Studio, Hermes Agent, and custom telemetry infrastructure — because you learn more from instrumenting real systems than reading papers.

---

## What I'm Building

| Project | What it does |
|---|---|
| **[lg-evals](https://github.com/Vishwanath98/lg-evals)** | LangGraph telemetry layer — measures graph coverage, finds unreachable execution paths, compares inline vs MCP tools |
| **[hermes-observatory](https://github.com/Vishwanath98/hermes-observatory)** | Framework-agnostic LLM proxy — detected 76.9% tool misrouting in production, fixed without touching agent code |

---

## Core Skills

**LLM & Agent Systems**

![LangGraph](https://img.shields.io/badge/LangGraph-000000?style=flat-square&logo=python&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-000000?style=flat-square&logo=chainlink&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-Protocol-blue?style=flat-square)
![RAG](https://img.shields.io/badge/RAG-Systems-purple?style=flat-square)
![vLLM](https://img.shields.io/badge/vLLM-Inference-green?style=flat-square)
![LM Studio](https://img.shields.io/badge/LM_Studio-Local_Inference-orange?style=flat-square)

**Languages & Frameworks**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat-square&logo=apachespark&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)

**Infrastructure & Cloud**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS_EC2-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Tailscale](https://img.shields.io/badge/Tailscale-Mesh_Network-blue?style=flat-square)
![Linux](https://img.shields.io/badge/Linux-Pop!_OS-48B9C7?style=flat-square&logo=linux&logoColor=white)

**ML & Data**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-189AB4?style=flat-square&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=python&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Postgres](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

**NLP & Analytics**

![NLTK](https://img.shields.io/badge/NLTK-NLP-green?style=flat-square)
![TextBlob](https://img.shields.io/badge/TextBlob-Sentiment-blue?style=flat-square)
![LDA](https://img.shields.io/badge/LDA-Topic_Modeling-purple?style=flat-square)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)

---

## Projects

### lg-evals — Agent Determinism Through Telemetry
> LangGraph + MCP instrumentation that finds and fixes coverage gaps

- Built a 3-node LangGraph agent (planner → executor → synthesizer) with full telemetry
- Discovered `executor→synthesizer` path was structurally unreachable across 7 runs
- Fixed with one routing condition change: **52% latency reduction, 60%→80% graph coverage**
- Compared inline Python tools vs MCP filesystem server (14 tools, 2x latency overhead)

**Stack:** LangGraph · MCP · SQLite · LM Studio · Python

**[→ View repo](https://github.com/Vishwanath98/lg-evals)**

---

### Hermes Observatory — Framework-Agnostic LLM Proxy
> Sits between any agent and its LLM backend — captures everything, changes nothing

- FastAPI proxy intercepts all LLM calls transparently (no agent code changes)
- Detected **76.9% tool misrouting** — agent using terminal shell commands instead of purpose-built tools
- Fixed via tool description rewriting at proxy layer — zero agent modifications
- Live dashboard: token costs, tool coverage heatmap, cost vs cloud APIs
- **$0 local vs $10.58 Claude Opus** for the same 689K token workload

**Stack:** FastAPI · SQLite · Chart.js · LM Studio · RTX 3090

**[→ View repo](https://github.com/Vishwanath98/hermes-observatory)**

---

### Reddit Social Media Listening Dashboard
> Real-time and historical Reddit analytics using Kafka, PySpark, and Streamlit

- Processed **1.4M+ comments across 15,000 posts** from r/technology using PySpark
- Sentiment analysis (TextBlob), topic modeling (LDA), and k-means clustering on post titles
- LDA identified 5 distinct AI-topic themes including deepfakes, copyright, and product launches
- Real-time pipeline: Kafka on AWS EC2 → PRAW → Streamlit dashboard with live keyword search
- Metrics: reach, impressions, sentiment, share of voice — all queryable by keyword

**Stack:** PySpark · Kafka · AWS EC2 · GCS · Streamlit · NLTK · TextBlob · LDA

**[→ Live App](https://reddit-realtime-listening.streamlit.app/)**

---

### IoT Network Anomaly Detection
> ML pipeline for classifying IoT network traffic as normal vs malicious

- Dataset: 82+ features extracted from PCAP files using CIC FlowMeter (IEC 60870-5-104 protocol)
- Evaluated 7 algorithms: Logistic Regression, Naive Bayes, SVM, Decision Trees, Random Forest, MLP, XGBoost
- **XGBoost best performer: 99.80% accuracy, 0.998 F1-score** — no hyperparameter tuning needed
- Feature selection via correlation matrix, Shapiro-Wilk normality test, and outlier analysis
- Deployed on multi-core CPUs for real-time IoT traffic classification

**Stack:** Python · Scikit-Learn · XGBoost · PySpark · Pandas · Seaborn

---

### Insurance Claims Processing Pipeline
> Production LangGraph system at ASI Analytics

- Two-prompt LLM architecture with tag-based routing
- OCR intake → multi-source RAG retrieval → grounded citations with PDF page numbers
- Five-category discrepancy detection
- Evaluation: human-in-the-loop + Pydantic structured output + metadata grounding

**Stack:** LangGraph · RAG · OCR · Pydantic · Python

*Production system — code not public*

---

## Local AI Stack

```
Hardware:  RTX 3090 (24GB VRAM) · Pop!_OS Linux
Inference: LM Studio (primary) · llama.cpp · vLLM
Models:    Qwen3.5-35B-A3B · Qwen2.5-Coder-7B
Agents:    Hermes Agent (Telegram + CLI)
Access:    Tailscale mesh — SSH from anywhere
Security:  LUKS encryption + TPM auto-unlock + Dropbear pre-boot SSH
```

Built telemetry infrastructure to observe, trace, and evaluate agent behavior on local hardware — the same problem enterprise V&V infrastructure solves at scale.

---

## Background

- **ASI Analytics** — AI Engineer (current) — LangGraph, RAG, production LLM pipelines
- **Accenture** — Data Engineering
- **SJSU** — MS Applied Data Science, May 2025

---

<div align="center">

*Building in public. Always learning.*

</div>
