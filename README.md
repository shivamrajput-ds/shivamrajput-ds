<div align="center">

# Shivam Rajput

### Junior Data Scientist · Applied ML & AI Systems

**I build evidence-first Data Science systems — from large-scale analytics and statistical experiments to ML reliability and grounded AI.**

B.Tech CSE (AI & ML) · Uttaranchal University · 2023–2027 · **CGPA 8.7/10**  
Dehradun, India

[![Open to Internships](https://img.shields.io/badge/Open%20to-Data%20Science%20%26%20Applied%20ML%20Internships-0b8f78?style=flat-square)](mailto:shivamrajput.datascientist@gmail.com)

[Portfolio](https://shivamrajput-ds.github.io/portfolio-website/) ·
[LinkedIn](https://www.linkedin.com/in/shivam-rajput-b0407632b/) ·
[LeetCode](https://leetcode.com/u/ShivamSynapse/) ·
[Kaggle](https://www.kaggle.com/shivamja) ·
[Docker Hub](https://hub.docker.com/u/shivamrajput130) ·
[Email](mailto:shivamrajput.datascientist@gmail.com)

</div>

---

## Evidence Index

<div align="center">

| **15.95M** | **+0.7692 pp** | **0.947** | **483** |
|:---:|:---:|:---:|:---:|
| complaint records processed | A/B absolute conversion uplift | strict hybrid RAGAS composite | Python3 LeetCode problems solved |

</div>

> **Evidence before claims · Baselines before complexity · Limitations documented, not hidden.**

---

## What I Build

I like problems where the hard part is not only training a model — it is building a trustworthy path from raw evidence to a defensible decision.

```text
QUESTION → DATA → METHOD → EVALUATE → DECIDE
```

My work sits across four connected areas:

- **Large-scale Data Science** — converting multi-million-row data into reusable analytics, risk signals and forecasts.
- **Statistical Experimentation** — estimating treatment effects with uncertainty, effect size and practical significance.
- **ML Reliability** — checking data quality, leakage, imbalance, baselines and explainability before trusting model results.
- **Applied AI** — combining deterministic analytics with retrieval, reranking, orchestration and grounded generation.

---

# Selected Systems

## 01 · Customer Complaint Intelligence Platform

**Large-Scale Data Science · NLP · Forecasting**

Built an end-to-end intelligence platform on the CFPB Consumer Complaint dataset, turning an **8–9 GB raw CSV** into reusable analytical layers, NLP routing, forecasting and decision views.

`15.95M complaints` · `3.57% forecast MAPE` · `75.28% product classifier accuracy` · `14/14 core tests`

**Architecture**

```text
8–9 GB CSV
   ↓
Chunk + validate
   ↓
Parquet analytical layers
   ↓
Analytics · NLP · Forecasting
   ↓
Decision views
```

**Key decision —** pre-aggregate expensive analysis and reuse validated Parquet outputs instead of loading the multi-GB raw CSV inside the application.

**Boundary —** complaint volume is not normalized by company customer base; forecasts and risk labels support investigation, not causal claims.

**Stack —** Python · Pandas · NumPy · PyArrow · Parquet · scikit-learn · TF-IDF · Logistic Regression · Prophet · Streamlit · Docker

[Repository](https://github.com/shivamrajput-ds/customer-complaint-intelligence) ·
[Walkthrough](https://youtu.be/ZrXg5p7wbqM) ·
[Evaluation](https://github.com/shivamrajput-ds/customer-complaint-intelligence/blob/main/docs/evaluation.md)

---

## 02 · Marketing A/B Testing & Experiment Analysis

**Statistics · Experimentation · Business Decision-Making**

Analyzed a controlled advertising experiment to determine whether the advertisement treatment produced a meaningful conversion improvement over a PSA control.

`588,101 users` · `2.5547% vs 1.7854% conversion` · `+0.7692 pp uplift` · `+43.09% relative uplift`

**95% uplift interval —** `+0.5951 to +0.9434 percentage points`

**Method**

```text
Experiment data
   ↓
Validation + group checks
   ↓
Conversion estimates
   ↓
Two-proportion test
   ↓
Confidence intervals + effect sizes
   ↓
Simulation + logistic consistency
   ↓
Power planning
   ↓
Decision
```

**Key principle —** never present only a p-value. Report absolute uplift, relative uplift, uncertainty, effect size and practical significance together.

**Boundary —** ROI is not claimed because campaign cost, incremental revenue and customer lifetime value are unavailable.

**Stack —** Python · Pandas · SciPy · Statsmodels · Matplotlib · Logistic Regression · Statistical Inference

[Repository](https://github.com/shivamrajput-ds/marketing-ab-testing-analysis)

---

## 03 · Agentic ML Audit Copilot

**ML Reliability · Human-in-the-Loop · MLOps**

Built a deterministic-first pre-training audit workflow that checks whether tabular data is sufficiently reliable for responsible baseline modeling.

```text
Dataset
   ↓
Profiling
   ↓
Data Quality · Leakage · Imbalance
   ↓
Risk Aggregation
   ↓
Human Review Gate
   ↓
Baselines
   ↓
MLflow · SHAP
   ↓
Grounded Report + Q&A
```

**Key design —** Python owns profiling, checks, calculations, routing and model evaluation. The LLM is restricted to explanation, report generation and follow-up Q&A.

**Engineering proof —** human review gate · baseline comparison · MLflow tracking · SHAP evidence · FastAPI · pytest · Docker · LangGraph

**Boundary —** this is not AutoML, a governance certification platform or a replacement for domain review.

**Stack —** Python · scikit-learn · LangGraph · MLflow · SHAP · FastAPI · Streamlit · pytest · Ruff · Docker

[Repository](https://github.com/shivamrajput-ds/Agentic-ML-Audit-Copilot) ·
[Live App](https://shivamrajput-ds-agentic-ml-audit-copilo-appstreamlit-app-joxap5.streamlit.app/) ·
[Walkthrough](https://youtu.be/kFzNam74QBc)

---

## 04 · Enterprise RAG Assistant

**Hybrid Retrieval · Exact Analytics · Grounded AI**

Built a document-intelligence system that separates **exact structured analytics** from **semantic retrieval**, instead of forcing every question through one RAG path.

<table>
<tr>
<td width="50%" valign="top">

**Structured path**

```text
CSV / Excel
    ↓
Query Router
    ↓
Pandas Analytics
    ↓
Exact Result
```

</td>
<td width="50%" valign="top">

**Semantic path**

```text
Documents
    ↓
BGE + BM25
    ↓
RRF + Dedup
    ↓
CrossEncoder
    ↓
Grounded Answer + Citations
```

</td>
</tr>
</table>

**Strict hybrid RAGAS —** `0.947 composite` · `0.966 faithfulness` · `1.000 context precision` · `1.000 context recall`

A separate **1,642-case production benchmark** passed its defined factual, source, safety, conversation and HTTP checks. Final benchmark acceptance remains intentionally open because the latency gate has not yet passed.

**Key decision —** deterministic Pandas analytics answer structured questions; hybrid retrieval + reranking handles semantic questions.

**Stack —** Python · FastAPI · React · Vite · BGE · BM25 · RRF · CrossEncoder · ChromaDB · Pandas · PostgreSQL · Docker · RAGAS

[Repository](https://github.com/shivamrajput-ds/enterprise-rag-assistant) ·
[Live Demo](https://enterprise-rag-assistant-kappa.vercel.app/) ·
[Walkthrough](https://youtu.be/Rvdz9DKtz5o) ·
[Evaluation](https://github.com/shivamrajput-ds/enterprise-rag-assistant/blob/main/docs/EVALUATION_REPORT.md)

---

## Capability Map

| Area | Tools / Concepts |
|---|---|
| **Data** | Python · SQL · Pandas · NumPy · PyArrow · Parquet |
| **Statistics** | A/B Testing · Confidence Intervals · Hypothesis Testing · SciPy · Statsmodels · Forecasting |
| **Machine Learning** | scikit-learn · Classification · Regression · Cross-validation · Feature Engineering · Model Evaluation · SHAP |
| **NLP / Applied AI** | TF-IDF · Topic Modeling · Embeddings · BM25 · Hybrid Retrieval · CrossEncoder · RAG · LangGraph |
| **Engineering** | FastAPI · REST APIs · React · Vite · Streamlit · Docker · MLflow · pytest · Ruff · GitHub Actions · MS SQL Server |

---

## How I Think About ML Systems

**01 · Baseline before complexity**  
Start with the simplest defensible method. Add complexity only when measurement justifies it.

**02 · Evaluation before claims**  
Use holdouts, uncertainty, baselines, failure analysis and explicit acceptance criteria.

**03 · Deterministic code before LLM judgment**  
Calculations, validation and business rules belong in code. LLMs are useful when language understanding or explanation genuinely adds value.

**04 · Boundaries are part of the result**  
A strong project states what was measured, what remains uncertain and what the system cannot prove.

---

## Practice / Build Log

The flagship projects above are portfolio systems. The work below is ongoing practice — kept separate so exercises are not inflated into project claims.

| Track | Current work |
|---|---|
| **SQL → Pandas** | joins · CTEs · windows · aggregation · `groupby` · `merge` · filtering |
| **DSA** | arrays · strings · hashing · stack/queue · linked lists · trees · heaps · binary search · DFS/BFS |
| **Python** | OOP · dunder methods · iterators · generators · decorators · debugging · clean code |
| **Engineering Labs** | validation · duplicate handling · idempotency · chunk processing · retries · failure isolation · storage choices |
| **Ship** | FastAPI · REST · SQL databases · Git · Docker · YAML · CI/CD · environment variables · MLflow |

---

## Coding Signal

**LeetCode public language counts**

`483 Python3` · `75 MS SQL Server` · `36 Pandas`

**100 Days Badge 2026**

[View LeetCode profile →](https://leetcode.com/u/ShivamSynapse/)

---

## About

I am pursuing **B.Tech Computer Science Engineering (AI & ML)** at **Uttaranchal University, Dehradun**.

My strongest work sits where Data Science meets engineering: large-scale analytics, statistical experimentation, ML reliability, NLP/retrieval and grounded AI systems.

I care about the part after *“the model works”* — validation, failure modes, reproducibility, interfaces, testing and clearly explaining what the result does **not** prove.

---

<div align="center">

### Open to Data Science · Machine Learning · NLP · Applied AI internships

[Email](mailto:shivamrajput.datascientist@gmail.com) ·
[LinkedIn](https://www.linkedin.com/in/shivam-rajput-b0407632b/) ·
[Portfolio](https://shivamrajput-ds.github.io/portfolio-website/) ·
[GitHub](https://github.com/shivamrajput-ds)

<br>

**Building Data Science systems where the evidence is as important as the model.**

</div>
