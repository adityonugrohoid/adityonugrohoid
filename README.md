# Hi, I'm Adityo Nugroho

**AI Solutions Engineer | Telecom & Industrial AI | Agentic RAG, Multi-Agent Systems, LLM Observability**

> Led network optimization at Huawei for 18 years. Pivoted. Now I design and deploy AI systems shaped by decades of knowing what breaks on live networks, from multi-agent RAG pipelines to LLM observability platforms and telecom-domain ML at scale.

![Python](https://img.shields.io/badge/Python-2d3436?style=flat-square&logo=python&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-2d3436?style=flat-square&logo=fastapi&logoColor=white) ![Streamlit](https://img.shields.io/badge/Streamlit-2d3436?style=flat-square&logo=streamlit&logoColor=white) ![Next.js](https://img.shields.io/badge/Next.js-2d3436?style=flat-square&logo=nextdotjs&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-2d3436?style=flat-square&logo=typescript&logoColor=white) ![LangChain](https://img.shields.io/badge/LangChain-2d3436?style=flat-square&logo=langchain&logoColor=white) ![Ollama](https://img.shields.io/badge/Ollama-2d3436?style=flat-square&logo=ollama&logoColor=white) ![Google Gemini](https://img.shields.io/badge/Gemini-2d3436?style=flat-square&logo=googlegemini&logoColor=white) ![scikit--learn](https://img.shields.io/badge/scikit--learn-2d3436?style=flat-square&logo=scikitlearn&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-2d3436?style=flat-square&logo=pytorch&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2d3436?style=flat-square&logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/Kubernetes-2d3436?style=flat-square&logo=kubernetes&logoColor=white) ![Terraform](https://img.shields.io/badge/Terraform-2d3436?style=flat-square&logo=terraform&logoColor=white) ![AWS](https://img.shields.io/badge/AWS-2d3436?style=flat-square&logo=amazonwebservices&logoColor=white) ![Google Cloud](https://img.shields.io/badge/Google_Cloud-2d3436?style=flat-square&logo=googlecloud&logoColor=white) ![Vercel](https://img.shields.io/badge/Vercel-2d3436?style=flat-square&logo=vercel&logoColor=white) ![Nginx](https://img.shields.io/badge/Nginx-2d3436?style=flat-square&logo=nginx&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2d3436?style=flat-square&logo=githubactions&logoColor=white)

&nbsp;

![Featured Projects](https://img.shields.io/badge/Featured_Projects-2d3436?style=for-the-badge)

### [Edge MCP Caller - SLM Specialist Fine Tuning](https://github.com/search?q=user%3Aadityonugrohoid+edge-mcp-caller+OR+nim-explorer&type=repositories)
**270M Model Beats 120B on Tool Calling at 32x Fewer Tokens**

Specialist fine-tuning that bakes tool definitions into model weights via LoRA r=128 on Gemma 3 270M, achieving 99.5% accuracy across 14 tools while using 32x fewer prompt tokens than schema-in-prompt baselines. The 291 MB model (Q8_0 GGUF) runs at 153ms avg latency on consumer hardware, including phones and Raspberry Pi.

- **[Edge MCP Caller](https://github.com/adityonugrohoid/edge-mcp-caller):** 418/420 eval accuracy, 14,033 training examples, 14 tools across 2 MCP servers, trained on single RTX 4060 (8GB VRAM), no accuracy degradation scaling from 3 to 14 tools
- **[NIM Explorer](https://github.com/adityonugrohoid/nim-explorer):** Machine-readable catalog of 107 Nvidia NIM models with automated capability probing (tool calling, JSON mode, thinking) via live endpoint testing

---

### [K8s FinOps Explore](https://github.com/search?q=user%3Aadityonugrohoid+gpu-autoscale-inference+OR+vllm-explorer&type=repositories)
**Scale-to-Zero GPU Inference on GKE**

Production GPU inference platform that costs $0 when idle. Two-layer autoscaling: KEDA watches Redis queue depth for pod-level 0-to-N scaling, while GKE Cluster Autoscaler provisions GPU VMs on pending pod scheduling. Cold start optimized from ~9m20s to ~5m9s (45% reduction) with PVC model weight caching and Secondary Boot Disk for container images.

- **[GPU Autoscale Inference](https://github.com/adityonugrohoid/gpu-autoscale-inference):** vLLM with continuous batching, TTFT p95 ~140-200ms warm, 12-panel Grafana dashboard (Prometheus + NVIDIA DCGM), Locust load testing, $0 cost when idle
- **[vLLM Explorer](https://github.com/adityonugrohoid/vllm-explorer):** Systematic API surface probing that drove model selection (Qwen2.5-1.5B) and parameter tuning via TTFT + tokens/sec benchmarks

---

### [AgentLens - Agentic RAG Portfolio](https://agentlens.adityonugroho.com/) LIVE
**Multi-Agent RAG Built From First Principles**

Progressive RAG evolution across 6 phases: from standalone Docker Compose to multi-agent orchestration to AWS serverless, with the same 4-layer token-budgeted PromptAssembler preserved identically across every deployment. No LangGraph, LlamaIndex, CrewAI, or AutoGen. The final phase features two autonomous agents coordinating via retry feedback loops with a 98 KB zero-dependency pipeline debugger.

- **Multi-Agent Pipeline:** ReAct reasoning loop with hybrid retrieval (vector + BM25), Quality Judge that evaluates chunks and retries with targeted feedback, per-role model selection across 4 pipeline stages
- **Evolution:** v0 (25 tests, Docker Compose, 7 services) -> v1 (section-aware chunking) -> v2 (69 tests, agentic ReAct) -> v3 (multi-agent with inter-agent feedback) -> AgentLens (263 tests, 5-service microservices, NDJSON streaming debugger)
- **Infrastructure:** 7 containers on a single EC2 t3.small via Terraform IaC, Cloudflare SSL, nginx routing — consolidated from 21 containers after retiring v1/v2/v3 stacks
- **Live:** [agentlens.adityonugroho.com](https://agentlens.adityonugroho.com/)

&nbsp;

![Fine-Tuning, RAG & Research](https://img.shields.io/badge/Fine--Tuning,_RAG_%26_Research-2d3436?style=for-the-badge)

### [Spatial LLM Fine Tuning](https://github.com/search?q=user%3Aadityonugrohoid+spatial-llm+OR+voxel-architect&type=repositories)
**+325% Spatial Accuracy via QLoRA Memorization**

Fine-tuned a 1.2B model to achieve +325% improvement on spatial coordinate tasks (avg IoU 0.139 to 0.590) using a memorization training strategy that produces 4 perfect-score letters and 18/26 above 0.5 IoU. Model selection driven by quantified thinking-loop failure rates across model families, not benchmark scores alone.

- **[Spatial LLM](https://github.com/adityonugrohoid/spatial-llm):** QLoRA r=32 on 4-bit NF4, 520 examples, 30 epochs, train loss 0.005 (99.84% accuracy), full pipeline from training to GGUF conversion to Ollama registration, 731 MB model
- **[Voxel Architect](https://github.com/adityonugrohoid/voxel-architect):** Agentic voxel builder where an LLM constructs 3D structures in a 16x16x16 grid using tool calling, with model selection and parsing strategies backed by data from 1,792 research runs across 32 models

---

### [Open Layer Standard](https://github.com/search?q=user%3Aadityonugrohoid+open-layer+OR+ollama-tool-calling-research+OR+ollama-catalog&type=repositories)
**LLM Inference I/O Standardization + Tool Calling Research**

Spec-first approach to LLM provider normalization with conformance tests proving 12/12 models pass after adapter normalization. Paired with a tool-calling benchmark across 32 models (1,792 runs) revealing that model size does not predict tool-calling quality, and a zero-download model catalog of 392 Ollama models via OCI registry blob inspection.

- **[Open Layer](https://github.com/adityonugrohoid/open-layer):** 8 JSON schemas, 66 conformance tests per model, 3 provider adapters (Nvidia, DeepSeek, Groq) normalizing thinking token formats and usage reporting into a single contract
- **[Ollama Tool Calling Research](https://github.com/adityonugrohoid/ollama-tool-calling-research):** 60 scored checks per model across 4 flag combinations; 10/32 achieve perfect scores; ministral-3:3b (3B) matches 1T+ models; key finding: streaming degrades tool calling and never improves it
- **[Ollama Catalog](https://github.com/adityonugrohoid/ollama-catalog):** 392 models from 3 sources (Cloud API, OCI Registry, Local) with capability detection (tools, vision, thinking) from template blob patterns, zero model weight downloads

---

### [pAIjo RAG](https://github.com/adityonugrohoid/pAIjo-rag)
**Islamic Knowledge Retrieval for the Indonesian Muslim Community**

Retrieval backbone for pAIjo, a WhatsApp/Telegram-based Islamic knowledge assistant. Collaboration with [Ainun Najib](https://github.com/ainunnajib). The core constraint: fabricating or misattributing Islamic quotes is a critical failure mode, so RAG grounds every response in verified scholarly content.

- 68 indexed knowledge points across 4 categories (NU traditions, Ramadan, fiqih, fatwa), sub-100ms retrieval, dual embedding backend (local MiniLM 384-dim vs. OpenAI 1536-dim)

---

### [RAG Systems & Local LLM Infrastructure](https://github.com/search?q=user%3Aadityonugrohoid+enterprise-rag-platform+OR+rag-operator-console+OR+ollama-multi-llm-server+OR+ollama-runtime&type=repositories)
**Enterprise RAG + Phased Local LLM Stack**

Enterprise RAG with multi-provider LLM support and PII redaction, plus a phased local LLM stack sharing a single Ollama runtime via a common Docker network.

- **[Enterprise RAG Platform](https://github.com/adityonugrohoid/enterprise-rag-platform):** 4-microservice architecture, 5 LLM providers (Ollama, OpenAI, Anthropic, Azure, Vertex AI), PII detection with automatic redaction, Prometheus monitoring
- **[RAG Operator Console](https://github.com/adityonugrohoid/rag-operator-console):** 4-layer PromptAssembler with token budgeting (4096 tokens), operator debugging UI for prompt assembly and chunk attribution
- **[Ollama Multi-LLM Server](https://github.com/adityonugrohoid/ollama-multi-llm-server):** Multi-model hot-swap, side-by-side comparison, 3-tier model selection
- **[Ollama Runtime](https://github.com/adityonugrohoid/ollama-runtime):** Shared GPU runtime on dedicated Docker network, centralized model storage, lifecycle-independent from downstream phases

&nbsp;

![Telecom AI/ML](https://img.shields.io/badge/Telecom_AI%2FML-2d3436?style=for-the-badge)

### [TRINITY Operations Suite](https://github.com/search?q=user%3Aadityonugrohoid+incident-commander+OR+noc-oracle+OR+net-ops-agent&type=repositories)
**AI-Powered Network Operations: Observe -> Decide -> Act**

Three-component AI system for reducing MTTR in NOC workflows, each mapping to one phase of the operational decision cycle.

- **[Incident Commander](https://github.com/adityonugrohoid/incident-commander):** Tumbling window batching (5s) with async ingestion at 500+ logs/sec, Pydantic-enforced structured outputs via Gemini 2.0 Flash Lite
- **[NOC-Oracle](https://github.com/adityonugrohoid/noc-oracle):** RAG with hybrid search (vector + regex keyword boosting) for exact error code matching, hallucination trap toggle showing ungrounded vs. RAG-verified answers
- **[Net-Ops Agent](https://github.com/adityonugrohoid/net-ops-agent):** Reasoning-action separation with human-in-the-loop approval gate, deterministic function calling from pre-defined toolbelt

---

### [Telecom ML](https://github.com/search?q=user%3Aadityonugrohoid+telecom-ml+OR+telecom-churn+OR+telecom-root-cause+OR+telecom-anomaly+OR+telecom-capacity+OR+telecom-network-optimization&type=repositories)
**6 End-to-End ML Use Cases + Framework**

Six independent implementations with domain-informed synthetic data generators embedding real telecom physics (SINR, Shannon capacity, congestion patterns), backed by 10+ years of network operations expertise. SHAP interpretability in every project.

| Use Case | ML Type | Algorithm | Result |
|:---------|:--------|:----------|:-------|
| Churn Prediction | Binary Classification | XGBoost | AUROC: 0.86 |
| Root Cause Analysis | Multi-class Classification | XGBoost | Acc@1: 0.91 |
| Anomaly Detection | Unsupervised | Isolation Forest | F1: 0.70 |
| QoE Prediction | Regression | LightGBM | RMSE: 0.45 |
| Capacity Forecasting | Time-Series | LightGBM | MAPE: 14.5% |
| Network Optimization | RL | Q-Learning | +61% vs random |

- **[Telecom ML Framework](https://github.com/adityonugrohoid/telecom-ml-framework):** 6 production-ready project templates with domain-informed data generator patterns, temporal leakage prevention, and unified standards

---

### [Telecom Digital Twin + MLOps](https://github.com/search?q=user%3Aadityonugrohoid+telecom-digital-twin+OR+telecom-qoe-analytics&type=repositories)
**Synthetic Generation -> Model Training -> Strategic Insights**

Deterministic multi-table generator (50K users, 2K cells, ~5.6M sessions) with cascade-based seeding for bit-exact reproducibility, feeding a six-phase analytics pipeline.

- **[Digital Twin](https://github.com/adityonugrohoid/telecom-digital-twin):** 7-step pipeline with referential integrity validation, Parquet columnar storage, configurable QoE noise (R-squared ~0.72-0.85)
- **[QoE Analytics](https://github.com/adityonugrohoid/telecom-qoe-analytics):** R-squared=0.7247 (XGBoost), ROC-AUC=0.9645 (LightGBM), Cohen's d=-2.12 congestion effect, Optuna + SHAP

&nbsp;

![Other Work](https://img.shields.io/badge/Other_Work-2d3436?style=for-the-badge)

### [Google GenAI Platform](https://github.com/search?q=user%3Aadityonugrohoid+google-cloud-ai-studio+OR+google-ai-studio&type=repositories) LIVE

- 3-step interior design render pipeline (text -> sketch -> render) deployed on **[Cloud Run](https://google-cloud-ai-studio-1099058340933.us-central1.run.app)** (Streamlit + Vertex AI) and **[Vercel](https://adityolab-ai-studio.vercel.app/)** (Next.js 14), comparing gemini-2.5-flash-image vs gemini-3-pro-image-preview for sketch-to-render fidelity

---

### [Observability & Agent Frameworks](https://github.com/adityonugrohoid/openclaw-dashboard)

- OpenClaw Dashboard: zero-build SPA (FastAPI + Tailwind CDN + Alpine.js) with 7 views covering agent sessions, configuration, security audit, and system resources, purpose-built with intelligent data filtering and glassmorphism UI

---

### [Trading & Fintech](https://github.com/search?q=user%3Aadityonugrohoid+polymarket-agent+OR+trailing-edge+OR+ratu+OR+binance-colo-research&type=repositories)

- 7 repos: autonomous LLM trading agent with 3-model council and 55 tests, async Binance bot with Ed25519 auth and systemd deployment, FIX 4.4 market making (3 sessions), REST analytics (7 endpoints), on-chain whale tracking (6 chains), DEX pair scanning (4 chains), co-location latency research (4.4x improvement from Tokyo VPS)

---

### [VPS Deploy Playbook](https://github.com/adityonugrohoid/vps-deploy-playbook)

- 8-chapter production playbook: 21+ containers on one VPS, 2-tier image layering (7x disk reduction), shared ChromaDB saving ~10GB RAM, 30-second selective deploys, full lifecycle from SSH hardening through CI/CD with GitHub Actions

&nbsp;

![Connect](https://img.shields.io/badge/Connect-2d3436?style=for-the-badge)

* **LinkedIn:** [linkedin.com/in/adityonugrohoid](https://linkedin.com/in/adityonugrohoid)
* **Email:** [adityo.nugroho.id@gmail.com](mailto:adityo.nugroho.id@gmail.com)
