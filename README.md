# <p align="center"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&pause=1000&color=3670A0&center=true&vCenter=true&width=850&lines=Kishan+K;SWE(AI/ML)+Engineer+at+Silo+Fortune;Production+GenAI+and+Computer+Vision;I+publish+my+baselines+too;IEEE+Published+Researcher" alt="Typing SVG" /></p>

<p align="center">
  <a href="https://linkedin.com/in/kishan-k-823049259"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
  <a href="https://kishan-k.pages.dev"><img src="https://img.shields.io/badge/Portfolio-255E63?style=for-the-badge&logo=About.me&logoColor=white"/></a>
  <a href="#-blogs"><img src="https://img.shields.io/badge/Blogs-3670A0?style=for-the-badge&logo=hashnode&logoColor=white"/></a>
  <a href="mailto:kishan.k.naik.ai@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
  <a href="https://leetcode.com/u/ZXO2yYfahk"><img src="https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=LeetCode&logoColor=black"/></a>
  <a href="https://huggingface.co/kishanaik5"><img src="https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black"/></a>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=kishanaik5&color=3670A0&style=for-the-badge&label=PROFILE+VIEWS"/>
</p>

---

## 👨‍💻 About Me

```python
kishan = {
    "role":      "Software Engineer (AI/ML) @ Silo Fortune",
    "location":  "Bengaluru, Karnataka, India",
    "education": "B.E. Artificial Intelligence & Machine Learning (CGPA: 8.6)",
    "builds":    ["GenAI & LLM fine-tuning", "Computer Vision", "AI agents", "Forecasting", "Backend systems"],
    "publications": ["IEEE Bangalore 2024", "ICAI-ARSSS 2025"],
    "in_production": {
        "markets":   "6,273 agricultural markets (mandis)",
        "languages": "12 Indian languages",
        "crops":     "312 crops · 1,693 diseases in the advisory knowledge base",
        "platforms": ["Kisaan Sampurna", "Gau Sampurna"],
    },
    "currently_building": "Sentinel: agentic research + compliance copilot for Indian equities",
    "principle": "A result I can't defend under hostile questions is not a result.",
    "fun_fact":  "Building AI for the people who feed the world 🌾",
}
```

---

## 🚀 Featured Projects

<table>
<tr>
<td width="50%" valign="top">

### 🌾 Kisaan Sampurna
<a href="https://play.google.com/store/apps/details?id=com.kissansampurna.app&hl=en_IN">📱 Google Play Store</a>

Agri-advisory and market-intelligence platform: crop-disease diagnosis, satellite-based farm health, weather advisories and multilingual advice in **12 Indian languages**. I fine-tuned a small Qwen-2.5-1.5B on **178,980** knowledge-base-generated advisories, built the 12-week price-forecasting service for **6,273 mandis**, and designed a two-level report cache that sharply cuts LLM calls.

`FastAPI` `Gemini` `Qwen-2.5 QLoRA` `PostgreSQL` `AWS ECS Fargate`

</td>
<td width="50%" valign="top">

### 🤖 Sentinel — Agentic Research & Compliance
<a href="https://github.com/sentinel-ai-lab/sentinel">GitHub</a> · <a href="https://huggingface.co/kishanaik5/sentinel-compliance-qwen25-7b-lora">🤗 Model</a>

A LangGraph agent that searches annual reports with **hybrid retrieval** (BM25 + pgvector, reciprocal-rank fusion, BGE reranker), drafts a cited brief, then a **QLoRA-tuned Qwen-2.5-7B** audits it for SEBI rules. **270/271** on a held-out synthetic set (and a simple TF-IDF baseline reaches 269 — [I wrote about it](#-blogs)). CI with lint, type checks, 27 tests and a citation-validity checker ([how I test it](blogs/06-testing-an-agent-that-cites-sources.md)).

`LangGraph` `pgvector` `Qwen-2.5` `QLoRA` `RAGAS` `FastAPI`

</td>
</tr>

<tr>
<td width="50%" valign="top">

### 🐄 Gau Sampurna — Semen Motility Analysis
<a href="https://github.com/kishanaik5/sperm_motility_project">GitHub (prototype)</a>

Computer-vision pipeline: **YOLOv8** detects cells, **DeepSORT** tracks them, and a motility classifier reports progressive / non-progressive / immotile shares. Served as an async service: FastAPI → Celery worker on a strict-FIFO Redis queue → S3 + PostgreSQL, sized for a 2 vCPU / 4 GB container. Client demo.

`YOLOv8` `DeepSORT` `FastAPI` `Celery` `Redis`

</td>
<td width="50%" valign="top">

### 🕸️ Agri-Expert Copilot
<a href="https://github.com/kishanaik5/Agri-expert-agent">GitHub</a> · <a href="https://agri-expert-agent.onrender.com/agri-ui">🔗 Live demo</a> <sub>(free tier: first load can take ~30 s)</sub>

Proof-of-concept advisory copilot over a **Neo4j** knowledge graph, with **LangGraph** (extract → traverse → synthesise), a **Strawberry GraphQL** API, RabbitMQ workers, an in-memory fallback graph, and **19,000+ PIN-code** zone mappings.

`Neo4j` `Cypher` `GraphQL` `LangGraph` `FastAPI` `RabbitMQ`

</td>
</tr>

<tr>
<td width="50%" valign="top">

### 🌱 AI Crop Stage Prediction
<a href="https://github.com/kishanaik5/Crop_stages_prediction_model">GitHub</a>

Satellite pipeline over **5 years of NDVI/EVI imagery** to infer growth stages across **80+ crops**, using asynchronous workflows and parallel Gemini inference.

`Gemini` `AgroMonitoring API` `AsyncIO` `PostgreSQL`

</td>
<td width="50%" valign="top">

### 📊 Mandi Price Intelligence
Price-forecasting API for **6,273 mandis × 346 commodities**: weekly series, lag and seasonal features, a 6-model ensemble (CatBoost, LightGBM, XGBoost, GBR, RF, SVR) with a 12-week recursive forecast. [How I backtest it](#-blogs).

`FastAPI` `PostgreSQL` `scikit-learn` `Docker`

</td>
</tr>

<tr>
<td width="50%" valign="top">

### 🧮 Lead Scoring (Alpify)
ETL that unifies **611 leads from 12 sheets / 6 channels**, plus an XGBoost contactability model (**5-fold CV AUC 0.81**) that assigns P1/P2/P3 call priorities. Rule-based lead-quality validation is next.

`pandas` `XGBoost` `scikit-learn`

</td>
<td width="50%" valign="top">

### 📚 RAG for VLSI Automation
Retrieval-augmented system over **1,000+ technical documents** that generates assessment questions, reducing manual authoring effort.

`LlamaIndex` `FAISS` `MongoDB` `AWS S3`

</td>
</tr>
</table>

---

## ✍️ Blogs

Short, honest engineering write-ups: what I measured, what I got wrong, and what I'd do differently.

| # | Post | Topic |
|:-:|:-----|:------|
| 1 | [**A 5-line baseline humbled my 99.6%**](blogs/01-auditing-my-own-ml-numbers.md) | Evaluation · fine-tuning |
| 2 | [**Tracking microscopic swimmers with YOLOv8 + DeepSORT on 2 vCPUs**](blogs/02-tracking-sperm-cells-yolov8-deepsort.md) | Computer vision · backend |
| 3 | [**How to backtest a price forecaster without fooling yourself**](blogs/03-backtest-a-price-model-honestly.md) | Forecasting · evaluation |
| 4 | [**Cache your LLM like a database**](blogs/04-cache-your-llm-like-a-database.md) | LLMs · system design |
| 5 | [**When your validation set is secretly your training set**](blogs/05-when-validation-is-secretly-training.md) | Fine-tuning · data |

<sub>Also on my portfolio: <a href="https://kishan-k.pages.dev/blog/">kishan-k.pages.dev/blog</a></sub>

---

## 🛠️ Tech Stack

| Category | Tools |
|:---------|:------|
| **Languages** | ![Python](https://img.shields.io/badge/python-3670A0?style=flat&logo=python&logoColor=ffdd54) ![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=flat&logo=c%2B%2B&logoColor=white) ![SQL](https://img.shields.io/badge/sql-%23336791.svg?style=flat&logo=sqlite&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=flat&logo=javascript&logoColor=%23F7DF1E) |
| **AI & GenAI** | ![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=flat&logo=PyTorch&logoColor=white) ![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=flat&logo=TensorFlow&logoColor=white) ![Gemini](https://img.shields.io/badge/Google%20Gemini-%238E75B2.svg?style=flat&logo=Google%20Gemini&logoColor=white) ![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white) ![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat&logo=huggingface&logoColor=black) |
| **Backend** | ![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=flat&logo=fastapi) ![Django](https://img.shields.io/badge/django-%23092E20.svg?style=flat&logo=django&logoColor=white) ![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=flat&logo=node.js&logoColor=white) ![React](https://img.shields.io/badge/react-%2320232a.svg?style=flat&logo=react&logoColor=%2361DAFB) ![GraphQL](https://img.shields.io/badge/GraphQL-E10098?style=flat&logo=graphql&logoColor=white) |
| **Cloud & MLOps** | ![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=flat&logo=amazon-aws&logoColor=white) ![GCP](https://img.shields.io/badge/GoogleCloud-%234285F4.svg?style=flat&logo=google-cloud&logoColor=white) ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=flat&logo=docker&logoColor=white) ![Jenkins](https://img.shields.io/badge/jenkins-%232C5263.svg?style=flat&logo=jenkins&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/CI/CD-FFB13B?style=flat&logo=githubactions&logoColor=white) |
| **Databases** | ![PostgreSQL](https://img.shields.io/badge/postgresql-%23316192.svg?style=flat&logo=postgresql&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=flat&logo=mongodb&logoColor=white) ![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=flat&logo=redis&logoColor=white) ![FAISS](https://img.shields.io/badge/FAISS-005571?style=flat) ![Neo4j](https://img.shields.io/badge/Neo4j-4581C3?style=flat&logo=neo4j&logoColor=white) |
| **Currently Learning** | ![AWS](https://img.shields.io/badge/AWS_Cloud_Practitioner-FF9900?style=flat&logo=amazon-aws&logoColor=white) → Solutions Architect |

---

## 📄 Publications

| Year | Title | Venue |
|:-----|:------|:------|
| 2024 | *Performance Evaluation of Deep Learning Models for Predicting Alzheimer's Disease* | **IEEE Bangalore Section** |
| 2025 | *Enhancing Predictive Maintenance with SHAP and LIME: A Framework for Explainable AI* | **ICAI – ARSSS** |

---

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=kishanaik5&theme=tokyo-night&hide_border=true" width="95%"/>
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=kishanaik5&theme=tokyonight&hide_border=true"/>
</p>

---

## 📈 Highlights

- 🌾 Production advisory and market-intelligence platform across **6,273 mandis** and **12 Indian languages**
- 🧠 Fine-tuned **Qwen-2.5** (1.5B and 7B) with **QLoRA**, evaluated against baselines with intervals, not just loss
- 🛰️ Satellite pipelines using **NDVI, EVI, NDWI**
- 🎥 **YOLOv8 + DeepSORT** video analysis as an async, memory-bounded service
- 🕸️ **Neo4j + LangGraph + GraphQL** advisory prototype with a live demo
- 📚 Published research: **IEEE Bangalore (2024)**, **ICAI-ARSSS (2025)**
- ☁️ Deployed on **AWS ECS Fargate, S3, PostgreSQL, Redis**

---

## 🐍 Contribution Snake

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/kishanaik5/kishanaik5/output/github-contribution-grid-snake-dark.svg"/>
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/kishanaik5/kishanaik5/output/github-contribution-grid-snake.svg"/>
    <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/kishanaik5/kishanaik5/output/github-contribution-grid-snake.svg"/>
  </picture>
</p>

---

<p align="center">
  <i>"Building AI for the people who feed the world 🌾"</i><br><br>
  <b>Open to MLOps, Cloud AI, and GenAI engineering roles</b><br>
  <a href="mailto:kishan.k.naik.ai@gmail.com">kishan.k.naik.ai@gmail.com</a> · <a href="https://kishan-k.pages.dev">kishan-k.pages.dev</a>
</p>
