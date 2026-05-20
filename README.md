<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:0f1923,100:1a2332&height=140&section=header&text=&animation=fadeIn" width="100%"/>
</div>

<div align="center">

```
╔══════════════════════════════════════════════════════════════════════════════╗
║                                                                              ║
║   SHIRSHENDU SEN                                                             ║
║   AI Systems Engineer  ×  Backend Engineer  ×  Applied ML                   ║
║                                                                              ║
║   GNN  ·  RAG  ·  LLM  ·  Microservices  ·  Production CI/CD               ║
║                                                                              ║
╚══════════════════════════════════════════════════════════════════════════════╝
```

<p>
Building production systems where <strong>knowledge graphs meet scalable APIs</strong> —<br/>
clinical NLP pipelines, LLM-integrated platforms, and security-hardened backends shipped to real users.
</p>

<p>
  <a href="https://linkedin.com/in/shirshendu-sen">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/>
  </a>
  &nbsp;
  <a href="https://portfolio-shirshendu.web.app">
    <img src="https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=vercel&logoColor=white"/>
  </a>
  &nbsp;
  <a href="mailto:shirshendusen7@gmail.com">
    <img src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white"/>
  </a>
  &nbsp;
  <img src="https://komarev.com/ghpvc/?username=Shirshendu-sen&style=flat-square&color=1f6feb&label=profile+views"/>
</p>

</div>

---

## Engineering Identity

I design and ship systems at the **intersection of applied machine learning and production backend engineering** — not one or the other. My work involves fine-tuning transformer models, building graph neural networks for clinical risk prediction, and wrapping those capabilities inside secure, observable, continuously-deployed APIs that serve real users.

The stack I operate in: **Python · TypeScript · Node.js · Next.js · Flask · PostgreSQL · PyTorch · FAISS · LangChain · Docker · GitHub Actions**.

> Currently completing MSc Computer Science at the University of Calcutta (Jun 2026) · Open to AI Engineer, Backend Engineer, and Applied ML roles at product companies and AI-first startups.

---

## Flagship Systems

### ① CHARTA — Clinical Risk Intelligence Pipeline
> `Research-grade · 5-layer architecture · ACL BioNLP / EMNLP target`

A fully modular, end-to-end pipeline that ingests raw, unstructured medical documents and produces multi-task clinical risk scores with natural-language, per-entity explainability. Designed from first principles — no gated datasets, no monolithic inference blocks.

```
┌──────────────────────────────────────────────────────────────────────────┐
│                       CHARTA — Layer Architecture                        │
├──────────────┬───────────────────────────────────────────────────────────┤
│  L1 Ingest   │  pdfplumber · PyMuPDF · Tesseract OCR · OpenCV           │
│              │  Deskew, denoise, normalize → structured JSON handoff     │
├──────────────┼───────────────────────────────────────────────────────────┤
│  L2 NLP      │  scispaCy · ClinicalBERT + LoRA fine-tune                │
│              │  NER · relation extraction · temporal normalization        │
│              │  MeSH / RxNorm / SNOMED ontology resolution               │
├──────────────┼───────────────────────────────────────────────────────────┤
│  L3 Graph    │  PyTorch Geometric · HeteroData                          │
│              │  Patient history → heterogeneous temporal knowledge graph  │
├──────────────┼───────────────────────────────────────────────────────────┤
│  L4 Predict  │  GraphSAGE · FAISS vector index · RAG augmentation       │
│              │  Multi-task heads: readmission / deterioration / med risk  │
├──────────────┼───────────────────────────────────────────────────────────┤
│  L5 Explain  │  SHAP DeepExplainer · BioGPT + LoRA                     │
│              │  Per-entity attribution + counterfactual generation        │
└──────────────┴───────────────────────────────────────────────────────────┘
```

**Architecture decisions that matter:** Layer boundaries enforced via JSON contracts (zero cross-layer imports) · Ablation harness covers L2–L4 independently · Typed throughout · Full pytest suite per layer · Evaluation against standard BioNLP benchmarks.

[![Repo](https://img.shields.io/badge/GitHub-MedGraph--AI--Clinical--Risk--Pipeline-8b5cf6?style=flat-square&logo=github)](https://github.com/Shirshendu-sen/MedGraph-AI-Clinical-Risk-Intelligence-Pipeline)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![PyTorch Geometric](https://img.shields.io/badge/PyG-3C2179?style=flat-square&logo=pytorch&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![FAISS](https://img.shields.io/badge/FAISS-0467DF?style=flat-square&logo=meta&logoColor=white)

---

### ② Smart Academic Platform — AI-Integrated LMS
> `Three-service microarchitecture · Vercel + Render · 200+ active users · production CI/CD`

Three independently deployable services — a Next.js edge frontend, an Express.js API layer, and a Flask AI microservice — wired together behind a stateless JWT auth pipeline with role-based access control, security headers, rate limiting, and zero-error deployment gates.

```
┌──────────────────────────────────────────────────────────────────────────┐
│                       Platform Architecture                               │
├─────────────────────┬────────────────────────────────────────────────────┤
│  Client             │  Next.js 14 (App Router) · React Query · Zustand  │
│  Vercel Edge CDN    │  TypeScript · Zod runtime validation               │
├─────────────────────┼────────────────────────────────────────────────────┤
│  API Layer          │  Express.js · Prisma ORM · NeonDB (PostgreSQL)    │
│  Render             │  JWT RS256 · bcrypt cost-12 · Helmet · rate limit  │
│                     │  Timing-attack-resistant auth · role middleware     │
├─────────────────────┼────────────────────────────────────────────────────┤
│  AI Microservice    │  Flask · Gemini 1.5 Flash · LangChain              │
│  Render             │  10 context-aware MCQs from notes in <4s           │
│                     │  Multi-turn doubt chatbot · context grounding       │
├─────────────────────┼────────────────────────────────────────────────────┤
│  CI/CD              │  GitHub Actions · TS + lint + build gates           │
│                     │  Branch protection · zero-error deploy policy       │
└─────────────────────┴────────────────────────────────────────────────────┘
```

[![Repo](https://img.shields.io/badge/GitHub-Smart--Academic--Platform-1f6feb?style=flat-square&logo=github)](https://github.com/Shirshendu-sen/Smart-Academic-Platform-with-AI-Integration)
[![Live](https://img.shields.io/badge/Live-Deployed-16a34a?style=flat-square&logo=vercel)](https://portfolio-shirshendu.web.app)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)

---

### ③ YouTube & Article Summarizer — Chrome Extension
> `Chrome Web Store · 100+ installs · sub-3s inference · Firebase + GitHub Actions`

A production Chrome extension that extracts YouTube transcripts and article content, forwards to a Flask microservice powered by LangChain, and returns AI-generated summaries in under 3 seconds. Deployed entirely on Firebase with automated CI/CD.

[![Repo](https://img.shields.io/badge/GitHub-Article--Summarizer-16a34a?style=flat-square&logo=github)](https://github.com/Shirshendu-sen)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-DD2C00?style=flat-square&logo=firebase&logoColor=white)

---

## Technical Stack

<div align="center">

| Domain | Technologies |
|--------|-------------|
| **AI / ML** | PyTorch · PyTorch Geometric · HuggingFace Transformers · LangChain · FAISS · SHAP · scispaCy · Scikit-learn |
| **Backend** | Node.js · Express.js · Flask · REST · JWT · RBAC · Prisma · GraphQL |
| **Frontend** | Next.js 14 · React · TypeScript · Tailwind CSS · Zustand · React Query |
| **Databases** | PostgreSQL · MongoDB · Firebase · NeonDB |
| **DevOps** | Docker · GitHub Actions · Linux · Vercel · Render · AWS · Azure |
| **Languages** | Python · TypeScript · JavaScript · Java · PHP · Shell/Bash |

</div>

---

## Engineering Principles

```python
@dataclass
class SystemDesignPhilosophy:

    architecture:    str = "microservice-first — independently deployable, contract-isolated layers"
    security:        str = "auth-first design — JWT, RBAC, Helmet, rate-limiting, timing-attack hardening"
    ai_systems:      str = "RAG-augmented, explainable, ablation-ready — models that can be interrogated"
    data_layer:      str = "schema-first, migration-tracked, typed ORM — Prisma + Zod across services"
    delivery:        str = "CI/CD gated — zero-error policy enforced at branch level, not post-deploy"
    observability:   str = "structured typed returns, failure-explicit handlers, no silent error swallowing"
```

---

## GitHub Statistics

<div align="center">

<img height="175" src="https://github-readme-stats.vercel.app/api?username=Shirshendu-sen&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=1f6feb&text_color=8b949e&ring_color=1f6feb&count_private=true&include_all_commits=true"/>
<img height="175" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Shirshendu-sen&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&text_color=8b949e&langs_count=7"/>

</div>

<div align="center">

[![GitHub Streak](https://streak-stats.demolab.com?user=Shirshendu-sen&theme=github-dark-blue&hide_border=true&background=0d1117&stroke=1f6feb&ring=58a6ff&fire=58a6ff&currStreakLabel=58a6ff&sideLabels=8b949e&dates=8b949e&currStreakNum=ffffff&sideNums=ffffff)](https://git.io/streak-stats)

</div>

<div align="center">

[![Activity](https://github-readme-activity-graph.vercel.app/graph?username=Shirshendu-sen&bg_color=0d1117&color=58a6ff&line=1f6feb&point=58a6ff&area=true&area_color=1f2f5f&hide_border=true&radius=6)](https://github.com/ashutosh00710/github-readme-activity-graph)

</div>

---

## Certifications & Recognition

| | Credential | Issuer |
|--|-----------|--------|
| `2025` | **Generative AI Fundamentals** — Transformer architectures, prompt engineering, AI deployment | Google Cloud |
| `2025` | **Software Engineer Certification** — Data structures, algorithms, OOP | HackerRank |
| `2025` | **ICDMAI 2025 Hackathon Participant** — 9th International Conference on Data Management, Analytics & Innovation | ICDMAI, Kolkata |
| `2024` | **TCS CodeVita Season 13 — Global Rank 1,640** in competitive programming | TCS |

---

## Work Experience

**Generative AI Intern** · AI Wallah *(Remote, May–Jun 2025)*
Optimized transformer-based NLP models in production — 18% accuracy gain, 12% latency reduction. Shipped a RESTful AI chatbot that reached 200+ active users in the first week, 4× faster than the 30-day target.

**Project Lead, Learning Management System** · University of Calcutta *(Jan–May 2024)*
Led a 5-member Agile team through the full SDLC on a platform adopted by 210+ students and 10+ educators. Automated exam workflows, reducing setup time by 40%.

---

<div align="center">

```
MSc Computer Science · University of Calcutta · 2024 – 2026
BSc Computer Science · University of Calcutta · 2021 – 2024
```

**Kolkata, India · Available for remote and relocation**

<br/>

<a href="https://linkedin.com/in/shirshendu-sen">
  <img src="https://img.shields.io/badge/Open%20to%20opportunities%20—%20Let's%20connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

<br/><br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a2332,50:0f1923,100:0d1117&height=100&section=footer" width="100%"/>

</div>
