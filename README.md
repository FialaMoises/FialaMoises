<img width=100% src="https://capsule-render.vercel.app/api?type=waving&color=00BFFF&height=150&section=header&text=Moisés%20Fiala&fontSize=40&fontColor=ffffff&animation=twinkling&fontAlignY=35"/>

<h2 align="center">AI & Data Engineer</h2>

<p align="center">
LLM agents, RAG systems and production ML — on top of data platforms built to be reliable.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/fialamoises/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="mailto:fiala.dev@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white" alt="Email"/></a>
  <img src="https://img.shields.io/badge/Belém,%20PA%20—%20Brazil-333333?style=flat" alt="Location"/>
</p>

---

## About

I build systems that turn data into decisions — and I care most about the part everyone skips: **proving they actually work**.

Day to day I ship LLM agents and semantic search into production (RAG over BigQuery, a multimodal WhatsApp agent, natural-language reporting), backed by the data engineering that keeps them honest — Spark, Kafka, Airflow, and quality gates that fail loudly instead of silently corrupting a dashboard.

Physics background (UFPA), so I tend to ask for the error bars before I ask for the demo.

**What I'm good at**
- LLM systems in production — agents, RAG, embeddings, structured outputs, cost and latency control
- Evaluation — golden tests, regression baselines, threshold optimization against real business cost
- Supervised ML end-to-end — feature engineering → training → explainability (SHAP/LIME) → FastAPI serving
- Streaming and lakehouse data platforms — exactly-once semantics, DLQs, data contracts, ADRs
- Backend in Go — concurrency, idempotency, immutable ledgers

---

## Featured Projects

### 🛡️ [Financial Fraud Detection Platform](https://github.com/FialaMoises/Plataforma-de-Detec-o-de-Fraudes-em-Transa-es-Financeiras)
End-to-end ML on the IEEE-CIS dataset (~590k transactions, 3.44% fraud) — PySpark ingestion → DuckDB feature store → LightGBM → FastAPI serving.

**AUC-ROC 0.883 · Average Precision 0.458.** Threshold tuned for cost (0.82) catches **40% of fraud at a 1.35% false-positive rate** — the tradeoff is argued explicitly, not hidden behind an accuracy number.

`PySpark` `LightGBM` `XGBoost` `DuckDB` `FastAPI` `Docker`

---

### 🏗️ [Real-Time E-commerce Lakehouse](https://github.com/FialaMoises/Plataforma-de-Dados-de-E-commerce-em-Tempo-Real)
Kafka → Spark Structured Streaming → Apache Iceberg in a medallion architecture. Not another pipeline — the point is the **guarantees**:

- **Effective exactly-once at the sink** — checkpoint + idempotent `MERGE` on `event_id`. The simulator injects duplicates and revenue provably doesn't inflate.
- **Dead Letter Queue** — bad events are diverted, never crash the stream or pollute Bronze.
- **Data quality gate as a circuit breaker** — Gold only publishes if expectations pass; otherwise the DAG fails.
- **Versioned data contract** validated in CI, plus 8 ADRs documenting the tradeoffs.

`Kafka` `Spark` `Iceberg` `Airflow` `dbt` `Trino` `Terraform` `Prometheus` `Grafana`

---

### 🔍 [AI Semantic Search API](https://github.com/FialaMoises/AI-Semantic-Search-API)
Go/Gin REST API for document indexing and semantic retrieval, with a Python embedding microservice and a pluggable provider — local `sentence-transformers` or OpenAI. Custom cosine-similarity vector store, Docker Compose deploy.

`Go` `Gin` `Python` `Embeddings` `Vector Search` `Docker`

---

### 📉 [Churn Prediction with Explainability & ROI](https://github.com/FialaMoises/churn_explicabilidade)
XGBoost/LightGBM over 40+ engineered features, with SHAP and LIME for global and per-customer explanations. Goes past classification into **cost-based threshold optimization and retention ROI simulation** — answering not just *who will churn* but *who is worth saving*.

`XGBoost` `SHAP` `LIME` `Streamlit` `Docker`

---

### 💳 [Real-Time Payment Processing System](https://github.com/FialaMoises/Real-Time-Payment-Processing-System)
High-throughput payments in Go — goroutines and mutexes with deadlock prevention, idempotency keys, an append-only immutable ledger, JWT auth and ACID guarantees.

`Go` `PostgreSQL` `Redis` `RabbitMQ` `JWT`

---

### 📈 [Time Series Forecasting — Comparative Study](https://github.com/FialaMoises/time-series-forecasting)
Systematic comparison across baselines, statistical models (ARIMA/SARIMA, Prophet, ETS, TBATS), ML (XGBoost, LightGBM, CatBoost), deep learning (LSTM, GRU, N-BEATS, TFT) and ensembles — built to find out **when the extra complexity actually earns its keep**, and when a seasonal naive forecast wins.

`Prophet` `LSTM` `N-BEATS` `CatBoost`

---

<details>
<summary><b>More projects</b></summary>

- **[SNCR Data Pipeline](https://github.com/FialaMoises/Desafio-T-cnico-Data-Engineer-DadosFazenda)** — end-to-end rural land registry pipeline: scraping → PostgreSQL (3NF) → FastAPI → web UI. Clean Architecture, idempotent loads, retry with checkpointing, sub-2ms queries.
- **[High-Performance Web Crawler in Go](https://github.com/FialaMoises/High-Performance-Web-Crawler-em-Go)** — concurrent crawler with worker pool, exponential backoff, multi-format export and thread-safety tests.
- **[Mini Spring Framework](https://github.com/FialaMoises/mini-spring-framework)** — dependency injection container built from scratch in Java to understand what Spring is doing under the hood.

</details>

---

## Tech Stack

**AI & ML**
<br>
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat&logo=openai&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-337AB7?style=flat)
![FAISS](https://img.shields.io/badge/FAISS-0467DF?style=flat)
![Pinecone](https://img.shields.io/badge/Pinecone-000000?style=flat)

**Data Engineering**
<br>
![Spark](https://img.shields.io/badge/Apache%20Spark-E25A1C?style=flat&logo=apachespark&logoColor=white)
![Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat&logo=apachekafka&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat&logo=apacheairflow&logoColor=white)
![Iceberg](https://img.shields.io/badge/Apache%20Iceberg-1B72BE?style=flat)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat&logo=dbt&logoColor=white)
![BigQuery](https://img.shields.io/badge/BigQuery-669DF6?style=flat&logo=googlebigquery&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat&logo=databricks&logoColor=white)

**Backend & Infra**
<br>
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat&logo=terraform&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white)

---

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=FialaMoises&show_icons=true&hide_border=true&theme=tokyonight&hide=stars" height="150"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=FialaMoises&layout=compact&hide_border=true&theme=tokyonight&langs_count=8" height="150"/>
</p>

<p align="center">
  <i>Open to AI / ML / Data Engineering roles — remote or Belém.</i>
</p>
