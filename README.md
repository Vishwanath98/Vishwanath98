## Hi there 👋
<div align="center">

# Madhu Vishwanath Burra

**AI Engineer · LLM Systems · Agentic AI · Local Inference**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/madhu-vishwanath-burra/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:madhuv435@gmail.com)

</div>

---

## About Me

MS Applied Data Science @ SJSU. Building production AI systems at the intersection of LLM inference, agent orchestration, and evaluation infrastructure.

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
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)

**Infrastructure**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Tailscale](https://img.shields.io/badge/Tailscale-Mesh_Network-blue?style=flat-square)
![Linux](https://img.shields.io/badge/Linux-Pop!_OS-48B9C7?style=flat-square&logo=linux&logoColor=white)

**ML & Data**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=python&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Postgres](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

---

## Key Projects

### lg-evals — Agent Determinism Through Telemetry
> LangGraph + MCP instrumentation that finds and fixes coverage gaps

- Built a 3-node LangGraph agent (planner → executor → synthesizer) with full telemetry
- Discovered `executor→synthesizer` path was structurally unreachable across 7 runs
- Fixed with one routing condition change: **52% latency reduction, 60%→80% graph coverage**
- Compared inline Python tools vs MCP filesystem server (14 tools, 2x latency overhead)

**[→ View repo](https://github.com/Vishwanath98/lg-evals)**

---

### Hermes Observatory — Framework-Agnostic LLM Proxy
> Sits between any agent and its LLM backend — captures everything, changes nothing

- FastAPI proxy intercepts all LLM calls transparently (no agent code changes)
- Detected **76.9% tool misrouting** — agent using terminal shell commands instead of purpose-built tools
- Fixed via tool description rewriting at proxy layer — zero agent modifications
- Live dashboard: token costs, tool coverage heatmap, cost vs cloud APIs
- **$0 local vs $10.58 Claude Opus** for the same 689K token workload

**[→ View repo](https://github.com/Vishwanath98/hermes-observatory)**

---

### Insurance Claims Processing Pipeline (Production — ASI Analytics)
> LangGraph-based claims processing with grounded citations and structured evaluation

- Two-prompt LLM architecture with tag-based routing
- OCR intake → multi-source retrieval → grounded citations with PDF page numbers
- Five-category discrepancy detection
- Evaluation: human-in-the-loop + Pydantic structured output + metadata grounding

*Production system — code not public*

---

## Local AI Stack

Running a home lab AI inference server for long-running autonomous agent workloads:

```
Hardware:  RTX 3090 (24GB VRAM) · Pop!_OS Linux
Inference: LM Studio (primary) · llama.cpp · vLLM
Models:    Qwen3.5-35B-A3B · Qwen2.5-Coder-7B
Agents:    Hermes Agent (Telegram + CLI)
Access:    Tailscale mesh — SSH from anywhere
Security:  LUKS encryption + TPM auto-unlock + Dropbear pre-boot SSH
```

Built telemetry infrastructure to observe, trace, and evaluate agent behavior on local hardware — the same problem AgentCombine solves at enterprise scale.

---

## Background

- **ASI Analytics** — AI Engineer (current) — LangGraph, RAG, production LLM pipelines
- **Accenture** — Data Engineering
- **SJSU** — MS Applied Data Science (in progress)

---

<div align="center">

*Building in public. Always learning.*

</div>
<!--
**Vishwanath98/Vishwanath98** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
