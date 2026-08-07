<div align="center">

# Shivam Rajput

### Junior Data Scientist · Applied ML & AI Systems

**I turn large, messy datasets into tested decisions.**

Final-year B.Tech CSE (AI & ML) student building end-to-end systems across
**Data Science · Statistics · Machine Learning · NLP · Applied AI**

**Open to Data Science, Machine Learning, NLP, and Applied AI internships.**

[Portfolio](https://shivamrajput-ds.github.io/portfolio-website/) ·
[LinkedIn](https://www.linkedin.com/in/shivam-rajput-b0407632b/) ·
[LeetCode](https://leetcode.com/u/ShivamSynapse/) ·
[Kaggle](https://www.kaggle.com/shivamja)

</div>

---

## About Me

I enjoy problems where the difficult part is not simply training a model, but making the complete path from **raw data → evidence → decision** reliable.

My work currently spans:

* **Large-scale Data Science** — processing millions of records into decision-ready analytics
* **Statistical experimentation** — measuring treatment effects with uncertainty and practical significance
* **ML reliability** — detecting data and modeling risks before training
* **Applied AI** — combining deterministic analytics with retrieval, reranking, and grounded generation

> **Evidence before claims. Baselines before complexity. Limitations documented, not hidden.**

---

# Selected Work

## 01 · Customer Complaint Intelligence Platform

**Large-Scale Analytics · NLP · Forecasting**

Built an end-to-end intelligence platform on the CFPB Consumer Complaint dataset to transform a very large raw dataset into analytics, risk signals, forecasts, NLP routing, and business recommendations.

* Processed **15.95M complaint records** from an **8–9 GB raw CSV**
* Built chunked preprocessing and reusable **Parquet** analytical storage
* Developed product, issue, company, geography, response, and narrative analytics
* Trained TF-IDF + Logistic Regression NLP routing models
* Achieved **3.57% MAPE** on a documented six-month forecasting holdout
* Added risk scoring, growth analysis, forecasting, and **14/14 core unit tests**

**Core Stack:** `Python` · `Pandas` · `PyArrow` · `scikit-learn` · `Prophet` · `Streamlit` · `Docker`

[Repository](https://github.com/shivamrajput-ds/customer-complaint-intelligence) ·
[Demo](https://youtu.be/ZrXg5p7wbqM?si=yEwHq2tT-l8_nTfY) ·
[Evaluation](https://github.com/shivamrajput-ds/customer-complaint-intelligence/blob/main/docs/evaluation.md)

---

## 02 · Marketing A/B Testing & Experiment Analysis

**Statistics · Experimentation · Business Decision-Making**

Analyzed a controlled marketing experiment to determine whether advertising improved conversion over a PSA control group.

* Evaluated **588,101 users**
* Advertisement conversion: **2.5547%**
* PSA conversion: **1.7854%**
* Absolute uplift: **+0.7692 percentage points**
* Relative uplift: **+43.09%**
* 95% uplift interval: **+0.5951 to +0.9434 pp**
* Approximately **130 users per additional conversion**
* Used hypothesis testing, effect sizes, simulation, logistic-regression consistency checks, and power analysis

**Decision:** The treatment produced a statistically reliable conversion improvement, while ROI was intentionally not claimed without campaign-cost and customer-value inputs.

**Core Stack:** `Python` · `Pandas` · `SciPy` · `Statsmodels` · `Matplotlib` · `Statistical Inference`

[Repository](https://github.com/shivamrajput-ds/marketing-ab-testing-analysis)

---

## 03 · Agentic ML Audit Copilot

**ML Reliability · Human-in-the-Loop · MLOps**

Built a pre-training audit workflow that evaluates whether tabular data is sufficiently reliable for baseline modeling before allowing the workflow to continue.

`Dataset → Profiling → Risk Checks → Human Review → Baselines → MLflow → SHAP → Report`

* Detects data-quality, target-leakage, class-imbalance, and modeling risks
* Uses deterministic Python for ML calculations and audit decisions
* Pauses risky workflows at a **human review gate**
* Compares baseline models instead of pretending to be AutoML
* Tracks experiments with **MLflow**
* Provides model evidence using **SHAP**
* Uses the LLM only for grounded explanations, reports, and Q&A
* Includes automated pytest coverage, API serving, and Docker packaging

**Core Stack:** `Python` · `scikit-learn` · `LangGraph` · `MLflow` · `SHAP` · `FastAPI` · `Streamlit` · `Docker`

[Repository](https://github.com/shivamrajput-ds/Agentic-ML-Audit-Copilot) ·
[Live App](https://shivamrajput-ds-agentic-ml-audit-copilo-appstreamlit-app-joxap5.streamlit.app/) ·
[Walkthrough](https://youtu.be/kFzNam74QBc)

---

## 04 · Enterprise RAG Assistant

**Hybrid Retrieval · Exact Analytics · Grounded AI**

Built an enterprise document assistant that separates exact structured analytics from semantic document retrieval instead of forcing every question through the same RAG pipeline.

**Structured queries**

`CSV / Excel → Query Router → Pandas Analytics → Exact Result`

**Semantic queries**

`Documents → BGE + BM25 → Fusion → CrossEncoder → Grounded Answer + Citations`

* Supports **PDF, DOCX, CSV, JSON, TXT, XLS, and XLSX**
* Combines BGE dense retrieval with **BM25 lexical retrieval**
* Adds query expansion, fusion, deduplication, and CrossEncoder reranking
* Routes structured questions to deterministic **Pandas analytics**
* Preserves source evidence and fallback behavior
* Uses a **FastAPI backend with React + Vite frontend**
* Supports Docker workflows and feedback persistence

### Evaluation

**29-case strict hybrid RAGAS evaluation**

* Composite: **0.947**
* Faithfulness: **0.966**
* Context Precision: **1.000**
* Context Recall: **1.000**
* Tier: **PRODUCTION_STRONG**

A separate **1,642-case production benchmark** is documented independently. Final acceptance is intentionally not claimed while its latency gate remains open.

**Core Stack:** `Python` · `FastAPI` · `React/Vite` · `BGE` · `BM25` · `CrossEncoder` · `ChromaDB` · `Pandas` · `Docker`

[Repository](https://github.com/shivamrajput-ds/enterprise-rag-assistant) ·
[Walkthrough](https://youtu.be/Rvdz9DKtz5o) ·
[Evaluation](https://github.com/shivamrajput-ds/enterprise-rag-assistant/blob/main/docs/EVALUATION_REPORT.md)

---

# Core Toolkit

**Data & Statistics**
Python · SQL · Pandas · NumPy · PyArrow · Parquet · EDA · A/B Testing · Confidence Intervals · Hypothesis Testing · Forecasting

**Machine Learning & NLP**
scikit-learn · Classification · Regression · Cross-validation · Feature Engineering · Model Evaluation · TF-IDF · Text Classification · Topic Modeling · SHAP

**Applied AI**
LangGraph · Embeddings · BM25 · Hybrid Retrieval · CrossEncoder Reranking · ChromaDB · Grounded Generation · Human-in-the-Loop Workflows

**Engineering & MLOps**
FastAPI · REST APIs · Streamlit · Docker · MLflow · pytest · Ruff · Git · GitHub Actions

---

## Engineering Principles

**Baseline before complexity**
Start with the simplest defensible approach and add complexity only when evidence justifies it.

**Evaluation before claims**
Report holdout performance, uncertainty, failure cases, and relevant baselines instead of relying on headline accuracy.

**Deterministic systems before LLM judgment**
Use code for calculations and business rules; use LLMs where language understanding or explanation genuinely adds value.

**Limitations belong in the project**
A project should clearly state what was measured, what remains unverified, and what it cannot claim.

---

## Coding

**LeetCode: 511+ problems solved**

Focus: Arrays · Strings · Hashing · Stack/Queue · Linked Lists · Trees · Heaps · Recursion · SQL

[LeetCode Profile](https://leetcode.com/u/ShivamSynapse/)

---

## Profiles

[Portfolio](https://shivamrajput-ds.github.io/portfolio-website/) ·
[LinkedIn](https://www.linkedin.com/in/shivam-rajput-b0407632b/) ·
[Kaggle](https://www.kaggle.com/shivamja) ·
[Docker Hub](https://hub.docker.com/u/shivamrajput130) ·
[YouTube](https://youtube.com/@shivamrajputds?si=n_NyC-mHNO6MWCr0)

---

## Contact

**Email:** [shivamrajput.datascientist@gmail.com](mailto:shivamrajput.datascientist@gmail.com)
**LinkedIn:** [Shivam Rajput](https://www.linkedin.com/in/shivam-rajput-b0407632b/)

---

<div align="center">

### Building Data Science systems where the evidence is as important as the model.

</div>
