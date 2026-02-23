# Hi, I'm Adityo Nugroho

**AI/ML Engineer - Telecom/Industrial Domain Expert | 18+ Years Network Optimization Leadership (Deputy GM at Huawei)**

> After leading network optimization strategy for operators serving millions, I witnessed what breaks at scale and built AI systems to fix it. I pivoted into AI/ML engineering to address these bottlenecks, architecting and deploying 12 end-to-end systems in 14 months (Nov 2024-Jan 2026), including AI/ML systems (GenAI, RAG, Agentic AI, MLOps, AI Observability) and production infrastructure.

&nbsp;

![Featured Projects](https://img.shields.io/badge/Featured_Projects-2d3436?style=for-the-badge)

### 1. [AgentLens - Agentic RAG Portfolio](https://agentlens.adityonugroho.com/) LIVE
**Multi-Agent RAG System Built From First Principles**

A multi-agent RAG system built from scratch -- no LangGraph, LlamaIndex, CrewAI, or AutoGen. Each version introduced progressively deeper autonomy, culminating in AgentLens with a 6-layer observation model and dual-tab pipeline debugger (live NDJSON streaming + post-mortem trace). Includes a 25-page documentation site.

- **Multi-Agent Pipeline:** ReAct reasoning loop with hybrid retrieval (vector + BM25), two-agent orchestrator with Quality Judge that evaluates chunks and retries with feedback, per-role model selection across 4 pipeline stages
- **Evolution:** v1 (25 tests) -> v2 (69 tests) -> v3 (208 tests) -> AgentLens (263 tests), each version adding deeper autonomy
- **Infrastructure:** 21 containers on a single EC2 m7i-flex.large via Terraform IaC, Cloudflare SSL, nginx routing to 4 apps
- **Observability:** 6-layer observation model (Prompt -> Thinking -> Raw -> Parsed -> Execution -> Observation), NDJSON streaming debugger, per-tool timing, confidence scoring
- **Live:** [agentlens.adityonugroho.com](https://agentlens.adityonugroho.com/)

### 2. [pAIjo RAG](https://github.com/adityonugrohoid/pAIjo-rag)
**Islamic Knowledge Retrieval for the Indonesian Muslim Community**

Retrieval backbone for pAIjo -- a WhatsApp/Telegram-based Islamic knowledge assistant. Collaboration with [Ainun Najib](https://github.com/ainunnajib) (project lead, Singapore-based data platform & civic tech leader). The core design constraint: fabricating or misattributing Islamic quotes is a critical failure mode, so RAG ensures every response is grounded in verified, curated content from trusted Islamic scholars.

- **Architecture:** FastAPI server -> OpenAI embeddings -> Qdrant vector database (68 curated chunks across 3 categories: Fiqih & Traditions, Ramadan Guidance, General Islamic Q&A)
- **Performance:** ~100ms query latency, 25 concurrent connections stable, 100% retrieval coverage verified
- **Hallucination-Resistant Design:** Responses grounded in verified Islamic scholarly content via RAG retrieval rather than relying on LLM training data

### 3. [RAG Systems & Local LLM Infrastructure](https://github.com/search?q=user%3Aadityonugrohoid+enterprise-rag-platform+OR+rag-operator-console+OR+ollama-multi-llm-server+OR+ollama-runtime&type=repositories)
**Enterprise RAG Platform + Phased Local LLM Stack**

Two tracks of RAG and LLM infrastructure. An enterprise RAG platform with multi-provider support, and a phased local LLM stack where all phases share a single Ollama runtime via a common Docker network.

- **[Enterprise RAG Platform](https://github.com/adityonugrohoid/enterprise-rag-platform):** 4-microservice architecture (API Gateway, Ingestion, Retrieval, Query) with **5 LLM providers** (Ollama, OpenAI, Anthropic, Azure, Vertex AI), Streamlit UI with side-by-side Direct LLM vs RAG comparison, and **PII detection** with automatic redaction
- **[RAG Operator Console](https://github.com/adityonugrohoid/rag-operator-console):** 4-layer PromptAssembler with token budgeting (4096 tokens), operator debugging UI for prompt assembly and chunk visualization, 2-turn clarification context
- **[Ollama Multi-LLM Server](https://github.com/adityonugrohoid/ollama-multi-llm-server):** Multi-model hot-swap switching, side-by-side model comparison, automated benchmarking, 3-tier model selection (fast/balanced/quality)
- **[Ollama Runtime](https://github.com/adityonugrohoid/ollama-runtime):** Shared GPU-accelerated Ollama container on dedicated Docker network, centralized model storage, lifecycle independence from downstream phases

### 4. [TRINITY Operations Suite](https://github.com/search?q=user%3Aadityonugrohoid+incident-commander+OR+noc-oracle+OR+net-ops-agent&type=repositories)
**AI-Powered Network Operations: Observe -> Decide -> Act**

A three-component AI system designed to reduce Mean Time To Repair (MTTR) in Network Operations Center workflows. Each component maps to one phase of the operational decision cycle:

- **[Incident Commander](https://github.com/adityonugrohoid/incident-commander):** Event-driven log analyzer with **tumbling window batching** (5s or 100 items) and **async architecture** for non-blocking I/O. Uses semantic root cause clustering via Gemini 2.0 Flash Lite with **Pydantic-enforced structured outputs** for real-time incident detection. **63x noise reduction** via tumbling-window aggregation.
- **[NOC-Oracle](https://github.com/adityonugrohoid/noc-oracle):** RAG-powered troubleshooting with **hybrid search** combining semantic vector search and keyword boosting for exact code matching. Features **context-aware chunking** preserving error-solution relationships and **hallucination-resistant retrieval** via strict context enforcement and source citations.
- **[Net-Ops Agent](https://github.com/adityonugrohoid/net-ops-agent):** Agentic AI with **reasoning-action separation** pattern and **human-in-the-loop approval gates**. Uses deterministic function calling from pre-defined toolbelt with **Pydantic validation** ensuring type safety. All actions require explicit authorization.

### 5. [Telecom ML](https://github.com/search?q=user%3Aadityonugrohoid+telecom-ml-portfolio+OR+telecom-ml-framework+OR+telecom-churn+OR+telecom-root-cause+OR+telecom-anomaly+OR+telecom-qoe-prediction+OR+telecom-capacity+OR+telecom-network-optimization&type=repositories)
**Classical ML Applied to Telecom: 6 End-to-End Use Cases + Framework**

Two tracks grounded in 10+ years of network operations domain expertise. The **telecom-ml-framework** provides 6 use case specifications with problem framing, data requirements, and model architectures. The **telecom-ml-portfolio** links 6 independent, end-to-end implementations with domain-informed synthetic data generators embedding real telecom physics.

**Implementation Results ([telecom-ml-portfolio](https://github.com/adityonugrohoid/telecom-ml-portfolio)):**

| Use Case | ML Type | Algorithm | Result |
|:---------|:--------|:----------|:-------|
| Churn Prediction | Binary Classification | XGBoost | AUROC: 0.86 |
| Root Cause Analysis | Multi-class Classification | XGBoost | Acc@1: 0.91 |
| Anomaly Detection | Unsupervised | Isolation Forest | F1: 0.70 |
| QoE Prediction | Regression | LightGBM | RMSE: 0.45 |
| Capacity Forecasting | Time-Series | LightGBM+Prophet | MAPE: 14.5% |
| Network Optimization | Reinforcement Learning | Q-Learning | +61% vs random |

- **[Telecom ML Framework](https://github.com/adityonugrohoid/telecom-ml-framework):** 6 production-ready ML project templates with complete specs, domain-informed data generator patterns, unified standards (SHAP-compatible versions, CI/CD, pytest)
- **Key Differentiator:** Telecom domain knowledge embedded at every stage -- synthetic data uses physics-based models (SINR, Shannon capacity, congestion patterns), SHAP interpretability connects model outputs to operational decisions

### 6. [Telecom Digital Twin + MLOps Pipeline](https://github.com/search?q=user%3Aadityonugrohoid+telecom-digital-twin+OR+telecom-qoe-analytics&type=repositories)
**End-to-End MLOps: Synthetic Generation -> Model Training -> Strategic Insights**

Data foundation and analytics layer for telecom ML work. The digital twin generates deterministic, multi-table LTE datasets with physics-based KPIs and bit-exact reproducibility. The analytics layer consumes this through a six-phase data science pipeline.

- **[Digital Twin](https://github.com/adityonugrohoid/telecom-digital-twin):** Deterministic multi-table generator with cascade-based seeding for bit-exact reproducibility. Produces **50K users, 2K cells, ~5.6M sessions** across 6 output tables with referential integrity validation. Parquet columnar storage with embedded schema metadata.
- **[QoE Analytics](https://github.com/adityonugrohoid/telecom-qoe-analytics):** Six-phase pipeline achieving **R²=0.7247** (XGBoost, MAE=0.3672, RMSE=0.4560) and **ROC-AUC=0.9645** (LightGBM, precision=0.46, recall=0.92). Features **SHAP interpretability** and **Cohen's d effect size analysis** (d=-2.12 for congestion effect on QoE).

### 7. [Google GenAI Platform](https://github.com/search?q=user%3Aadityonugrohoid+google-cloud-ai-studio+OR+google-ai-studio&type=repositories) LIVE
**Multi-Step GenAI Workflow for Architectural Design**

Same 3-step interior design render pipeline (Text Enhancement -> Sketch Generation -> Photorealistic Rendering) deployed on two platforms. Transforms simple text descriptions into photorealistic architectural renders.

- **[Cloud Run Version](https://github.com/adityonugrohoid/google-cloud-ai-studio):** Cloud-native Streamlit app on Google Cloud Run with Vertex AI integration. Uses gemini-2.0-flash-lite (text) + gemini-2.5-flash-image (sketch/render). Docker + Cloud Build CI/CD. **[Live App](https://google-cloud-ai-studio-1099058340933.us-central1.run.app)**
- **[Vercel Version](https://github.com/adityonugrohoid/google-ai-studio):** Next.js 14 + TypeScript on Vercel with 3 dedicated API routes. Uses gemini-3-pro-image-preview for rendering -- delivers near-exact sketch-to-render correspondence for production interior design workflows
- **Model Progression:** gemini-2.5-flash-image (fast, minor drift) -> gemini-3-pro-image-preview (high-fidelity 1:1 alignment)

### 8. [Observability & Agent Frameworks](https://github.com/adityonugrohoid/openclaw-dashboard)
**Custom Observability for Autonomous AI Agent Systems**

OpenClaw Dashboard -- a custom observability interface for the OpenClaw autonomous AI agent framework. Provides real-time visibility into agent configuration, sessions, security posture, and system resources.

- **Architecture:** Single-file SPA with zero build dependencies -- no bundler, no node_modules. FastAPI backend + Tailwind CSS (CDN) + Alpine.js
- **9 Core Views:** Session Status, Active Sessions, Configuration, Memory Files, Skills, Workspace, Channels, Security Audit, System Info
- **Features:** Smart data filtering (auto-hides irrelevant noise), glassmorphism card design, skeleton loading states, bound to localhost for security

### 9. [Architecture & Reference](https://github.com/adityonugrohoid/ai-system-architecture-landscape)
**System-Level Architectural Thinking for AI Systems**

A comprehensive reference architecture landscape covering **15 component layers** from data ingestion to user interfaces, across local, hybrid, and cloud deployments. Captures the design rationale backing engineering decisions across all project groups.

- **15 Layers:** Data Sources & Ingestion, Storage, Structured DBs, Vector DBs, Embedding Models, LLM Inference, Prompting & RAG, Agent Orchestration, Workflow Automation, Evaluation & Safety, Observability, API Gateways, Chat & UI, Developer Productivity, Deployment & Infrastructure
- **Per-Layer Documentation:** Architectural role, problem solved, layer characteristics, common tools, deployment considerations

### 10. [Client Work](https://github.com/adityonugrohoid/maven-prime-solution) LIVE
**Production Client Website: Interior Design Portfolio**

Portfolio website built for Maven Prime Solution, an interior design studio in Surabaya, Indonesia. Deployed on Vercel as a pure static site with zero backend dependencies.

- **Features:** Portfolio gallery organized by space type with lightbox viewer, dark and gold premium color scheme, fully responsive, lazy loading, SEO configured
- **Architecture:** Pure static site -- HTML5, Tailwind CSS (CDN), Alpine.js, vanilla JavaScript. No backend, no build step
- **Live:** [maven-prime-solution.vercel.app](https://maven-prime-solution.vercel.app/)

### 11. [Trading & Fintech](https://github.com/search?q=user%3Aadityonugrohoid+trailing-edge+OR+ratu-fix-bot+OR+ratu-rest-api+OR+ratu-onchain-monitor+OR+ratu-moon-radar+OR+binance-colo-research&type=repositories)
**Production Trading Infrastructure: Algorithmic Bot + Multi-Chain Analytics + Latency Research**

Three tracks of production trading infrastructure: an algorithmic trading bot, a 4-component crypto trading suite, and latency research for exchange co-location.

- **[Trailing Edge](https://github.com/adityonugrohoid/trailing-edge):** High-performance async Python trading bot for Binance with **dynamic trailing take-profit** (exponential decay), **regime detection** (BASE/QUOTE auto-switch with all-in compounding), **Donchian channel hard stop** with smart re-entry gating, Ed25519 authentication. 24/7 systemd deployment with Telegram alerts
- **[RATU Suite](https://github.com/search?q=user%3Aadityonugrohoid+ratu-fix-bot+OR+ratu-rest-api+OR+ratu-onchain-monitor+OR+ratu-moon-radar&type=repositories):** **FIX Bot** (FIX 4.4, 3 concurrent sessions, spread market making), **REST API** (7 Binance endpoints, multi-timeframe klines), **On-Chain Monitor** (6 chains, whale tracking, known wallet labels), **Moon Radar** (4 chains, DEX pair scanning, early token detection)
- **[Binance Colo Research](https://github.com/adityonugrohoid/binance-colo-research):** Latency testing and co-location detection comparing Singapore vs Tokyo endpoints. **4.4x latency improvement** from Tokyo VPS (307ms avg vs 1,344ms), 80 concurrent workers, interactive HTML reports with color-coded results

&nbsp;

![Technical Stack](https://img.shields.io/badge/Technical_Stack-2d3436?style=for-the-badge)

| Domain | Technologies |
| :--- | :--- |
| **Programming & Frameworks** | Python, Python Async (asyncio), Streamlit, FastAPI, LangChain, Pandas |
| **AI & Machine Learning** | Google Gemini 2.0 (Flash/Lite/Pro), Vertex AI, RAG, XGBoost, LightGBM, scikit-learn, SHAP, Agentic Patterns, Function Calling, Prompt Engineering |
| **MLOps & Data Engineering** | Reproducible Pipelines, Schema Validation, Model Evaluation, Parquet, Synthetic Data (SDV), Text Embeddings, Batch Prediction, CLI Automation, SQL |
| **Cloud & Infrastructure** | Google Cloud Run, Docker, Artifact Registry, Linux VPS, Systemd, CI/CD |
| **Protocols & APIs** | REST, WebSockets, FIX 4.4, JSON-RPC, GraphQL |
| **Tools** | UV Manager, Pytest, Ruff, Git/GitHub, Tableau |

&nbsp;

![Domain Expertise](https://img.shields.io/badge/Domain_Expertise-2d3436?style=for-the-badge)

* **Telecom/Industrial AI Specialist:** 18+ years domain expertise in large-scale network optimization (10M+ subscribers) combined with hands-on AI/ML engineering
* **Production Systems Focus:** Building AI/ML solutions that solve real operational problems in telecom and industrial domains
* **Transferable Expertise:** Network optimization -> Industrial AI, Observability, Infrastructure systems

&nbsp;

![Available For](https://img.shields.io/badge/Available_For-2d3436?style=for-the-badge)

* **Telecom/Industrial AI:** Domain-specific AI/ML solutions leveraging network optimization expertise
* **Observability & APM:** Automated remediation and log analysis.
* **Fintech & Trading:** Low-latency decision systems.
* **Location:** Remote Preferred | Based in Indonesia (UTC+7)

&nbsp;

![Connect](https://img.shields.io/badge/Connect-2d3436?style=for-the-badge)

* **Website:** [adityonugrohoid.github.io](https://adityonugrohoid.github.io)
* **LinkedIn:** [linkedin.com/in/adityonugrohoid](https://linkedin.com/in/adityonugrohoid)
* **Email:** [adityo.nugroho.id@gmail.com](mailto:adityo.nugroho.id@gmail.com)
