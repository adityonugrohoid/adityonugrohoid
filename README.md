# Hi, I'm Adityo Nugroho

**AI/ML Engineer - Telecom/Industrial Domain Expert | 18+ Years Network Optimization Leadership (Deputy GM at Huawei)**

> After leading network optimization strategy for operators serving millions, I witnessed what breaks at scale and built AI systems to fix it. I pivoted into AI/ML engineering to address these bottlenecks, architecting and deploying 12 end-to-end systems in 14 months (Nov 2024-Jan 2026), including AI/ML systems (GenAI, RAG, Agentic AI, MLOps, AI Observability) and production infrastructure.

&nbsp;

![Featured Projects](https://img.shields.io/badge/Featured_Projects-2d3436?style=for-the-badge)

### 1. [TRINITY Operations Suite](https://github.com/search?q=user%3Aadityonugrohoid+incident-commander+OR+noc-oracle+OR+net-ops-agent&type=repositories)
**AI-Powered Network Operations: Observe -> Decide -> Act**

A cohesive integrated suite solving the "Mean Time to Recovery" bottleneck with three integrated components deployed as part of NOC operations:
- **[Incident Commander](https://github.com/adityonugrohoid/incident-commander):** Event-driven log analyzer with **tumbling window batching** (5s or 100 items) and **async architecture** for non-blocking I/O. Uses semantic root cause clustering via Gemini 2.0 Flash Lite with **Pydantic-enforced structured outputs** for real-time incident detection.
- **[NOC-Oracle](https://github.com/adityonugrohoid/noc-oracle):** RAG-powered troubleshooting with **hybrid search** combining semantic vector search and keyword boosting for exact code matching. Features **context-aware chunking** preserving error-solution relationships and **strict context enforcement** preventing hallucination.
- **[Net-Ops Agent](https://github.com/adityonugrohoid/net-ops-agent):** Agentic AI with **reasoning-action separation** pattern and **human-in-the-loop approval gates**. Uses deterministic function calling from pre-defined toolbelt with **Pydantic validation** ensuring type safety. All actions require explicit authorization.

### 2. [AI Studio](https://github.com/adityonugrohoid/google-cloud-ai-studio) LIVE
**Multi-Step GenAI Workflow for Architectural Design on Google Cloud**

Cloud-native Streamlit application demonstrating advanced GenAI workflow orchestration using Google Vertex AI. Transforms simple text descriptions into photorealistic architectural renders through a **3-stage pipeline**: text enhancement -> sketch generation -> photorealistic rendering.

- **Text Enhancement Stage:** Uses Gemini 2.0 Flash Lite to expand simple user descriptions into detailed architectural specifications, preparing enriched context for downstream image generation stages
- **Sketch Generation Stage:** Gemini 2.5 Flash Image creates architectural line drawings from enhanced text descriptions, creating intermediate visual representations for rendering pipeline
- **Photorealistic Rendering Stage:** Transforms sketches into V-Ray style photorealistic renders using advanced prompting techniques for realistic architectural visualization
- **Cloud Run Deployment:** Containerized Streamlit application deployed on Google Cloud Run with Vertex AI integration and Docker containerization for scalable cloud deployment
- **Live Service**: [View App (Cloud Run)](https://google-cloud-ai-studio-1099058340933.us-central1.run.app)

### 3. [Telecom Digital Twin + MLOps Pipeline](https://github.com/search?q=user%3Aadityonugrohoid+telecom-digital-twin+OR+telecom-qoe-analytics&type=repositories)
**End-to-End MLOps: Synthetic Generation -> Model Training -> Strategic Insights**

A complete MLOps ecosystem combining deterministic data generation with ML workflows. Generates **50K users with 5.6M sessions** in reproducible fashion, then applies six-phase analytics pipeline from EDA to strategic recommendations.

- **[Digital Twin](https://github.com/adityonugrohoid/telecom-digital-twin):** Deterministic multi-table generator with bit-exact reproducibility via cascade-based seeding. Produces 4 output tables (users, cells, sessions, events) with referential integrity validation. Parquet columnar storage with embedded schema metadata for efficient storage.
- **[QoE Analytics](https://github.com/adityonugrohoid/telecom-qoe-analytics):** Six-phase analytics pipeline achieving **R²=0.7247** (XGBoost, MAE=0.3672, RMSE=0.4560) and **ROC-AUC=0.9645** (LightGBM, precision=0.46, recall=0.92). Features **SHAP interpretability** for model explainability and **Cohen's d effect size analysis** for quantifying impact magnitude of QoE drivers.

### 4. [Trailing Edge Trading Bot](https://github.com/adityonugrohoid/trailing-edge)
**High-Performance Async Trading Bot with Dynamic Trailing Take-Profit**

High-performance asynchronous Python trading bot for Binance featuring dynamic trailing take-profit strategies, regime detection, Donchian channel gating, and Ed25519 authentication. Built for 24/7 autonomous operation on low-cost infrastructure with low-latency reaction times.

- **Dynamic Trailing Take-Profit:** Exponential decay from start to min factor, automatically adjusting profit targets as gains increase, locking in profits while allowing upside
- **Regime Detection and Auto-Compounding:** Automatic switching between BASE (holding inventory) and QUOTE (holding cash) modes with all-in compounding for bull rallies
- **Donchian Channel Hard Stop:** Volatility-aware stop-loss using Donchian Channels with intelligent re-entry gating that waits for price to cross mid-channel in favorable direction after stop triggers
- **24/7 Systemd Deployment:** Deployed as systemd service for autonomous operation with auto-restart, resource limits, and journald logging

### 5. [RATU Trading Suite](https://github.com/search?q=user%3Aadityonugrohoid+ratu-moon-radar+OR+ratu-onchain-monitor+OR+ratu-rest-api+OR+ratu-fix-bot&type=repositories)
**Real-time Automated Trading Unified: Multi-Chain Crypto Infrastructure**

A comprehensive 4-component crypto trading infrastructure for multi-chain token discovery, on-chain analytics, market data, and low-latency order execution:

- **[FIX Bot](https://github.com/adityonugrohoid/ratu-fix-bot):** FIX Protocol 4.4 connector with **ED25519 authentication** and defensive message parsing. Features three FIX sessions (Market Data, Order Entry, Drop Copy) with spread market making strategy for low-latency order execution
- **[REST API](https://github.com/adityonugrohoid/ratu-rest-api):** Comprehensive market analytics using **7 Binance public endpoints** with multi-timeframe kline analysis (1h, 4h, 1d) and connection pooling. Dataclass-based response parsing ensures type safety
- **[On-Chain Monitor](https://github.com/adityonugrohoid/ratu-onchain-monitor):** Token holder analytics and whale tracking across **6 chains** (BSC, Ethereum, Polygon, Arbitrum, Base, Avalanche) with three-mode architecture (Basic Info, Top Holders, Full Snapshot) and known label identification
- **[Moon Radar](https://github.com/adityonugrohoid/ratu-moon-radar):** Multi-chain DEX pair scanner supporting **4 chains** (Ethereum, BNB Chain, Polygon, Base) with dynamic pair parsing and early token detection via 24h price gains

### 6. [Telecom ML Framework](https://github.com/adityonugrohoid/telecom-ml-framework)
**Framework for Telecom AI/ML Solutions**

A framework for building AI/ML solutions to real-world telecom challenges, emphasizing domain expertise and practical problem-solving. Provides 6 ML project templates covering the most common telecom AI/ML use cases with complete technical specifications.

- **Six Use Case Specifications:** Complete specs for Churn Prediction, Root Cause Analysis, Anomaly Detection, QoE Prediction, Capacity Forecasting, Network Optimization with problem framing and model recommendations
- **Domain-Informed Data Generators:** Hand-crafted generators embedding real telecom physics (SINR, Shannon capacity, congestion patterns) vs generic synthetic data, demonstrating domain expertise
- **SHAP-Compatible Standards:** Enforced dependency versions (numpy<2.0, xgboost<2.0) ensuring interpretability works without conflicts, critical for business adoption
- **Unified Project Structure:** Consistent template across all projects with config, data generation, features, models, notebooks, and tests enabling rapid project creation

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