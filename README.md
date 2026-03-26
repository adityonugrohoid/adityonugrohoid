# Hi, I'm Adityo Nugroho

**AI Solutions Engineer | Telecom & Industrial AI | Agentic RAG, Multi-Agent Systems, LLM Observability**

> Led network optimization at Huawei for 18 years. Pivoted. Now I design and deploy AI systems shaped by decades of knowing what breaks on live networks, from multi-agent RAG pipelines to LLM observability platforms and telecom-domain ML at scale.

&nbsp;

![Featured Projects](https://img.shields.io/badge/Featured_Projects-2d3436?style=for-the-badge)

### 1. [CV Pipeline - Construction Blueprint Analysis](https://github.com/adityonugrohoid/cv-pipeline)
**4-Phase Progressive Detection: Shape → OCR → YOLO → Orchestrator**

Four independent detection phases feeding a fault-tolerant orchestrator for construction blueprint analysis. Classical CV (contour + color segmentation), OCR (Tesseract with preprocessing), and YOLOv8n fine-tuned on synthetic data - each phase runs independently with graceful failure isolation so partial results are preserved even when one detector fails.

- 66 tests, mAP@50 0.992 (5 construction symbol classes), 200 synthetic training images, per-stage timing and error capture, FastAPI async upload server, Docker support

### 2. [Edge MCP Caller - SLM Specialist Fine Tuning](https://github.com/search?q=user%3Aadityonugrohoid+edge-mcp-caller+OR+nim-explorer&type=repositories)
**270M Model Beats 120B on Tool Calling at 32x Fewer Tokens**

Specialist fine-tuning that bakes tool definitions into model weights via LoRA r=128 on Gemma 3 270M, achieving 99.5% accuracy across 14 tools while using 32x fewer prompt tokens than schema-in-prompt baselines. The 291 MB model (Q8_0 GGUF) runs at 153ms avg latency on consumer hardware, including phones and Raspberry Pi.

- **[Edge MCP Caller](https://github.com/adityonugrohoid/edge-mcp-caller):** 418/420 eval accuracy, 14,033 training examples, 14 tools across 2 MCP servers, trained on single RTX 4060 (8GB VRAM), no accuracy degradation scaling from 3 to 14 tools
- **[NIM Explorer](https://github.com/adityonugrohoid/nim-explorer):** Machine-readable catalog of 107 Nvidia NIM models with automated capability probing (tool calling, JSON mode, thinking) via live endpoint testing


### 3. [K8s FinOps Explore](https://github.com/search?q=user%3Aadityonugrohoid+gpu-autoscale-inference+OR+vllm-explorer&type=repositories)
**Scale-to-Zero GPU Inference on GKE**

Production GPU inference platform that costs $0 when idle. Two-layer autoscaling: KEDA watches Redis queue depth for pod-level 0-to-N scaling, while GKE Cluster Autoscaler provisions GPU VMs on pending pod scheduling. Cold start optimized from ~9m20s to ~5m9s (45% reduction) with PVC model weight caching and Secondary Boot Disk for container images.

- **[GPU Autoscale Inference](https://github.com/adityonugrohoid/gpu-autoscale-inference):** vLLM with continuous batching, TTFT p95 ~140-200ms warm, 12-panel Grafana dashboard (Prometheus + NVIDIA DCGM), Locust load testing, $0 cost when idle
- **[vLLM Explorer](https://github.com/adityonugrohoid/vllm-explorer):** Systematic API surface probing that drove model selection (Qwen2.5-1.5B) and parameter tuning via TTFT + tokens/sec benchmarks


### 4. [AgentLens - Agentic RAG Portfolio](https://agentlens.adityonugroho.com/) LIVE
**Multi-Agent RAG Built From First Principles**

Progressive RAG evolution across 6 phases: from standalone Docker Compose to multi-agent orchestration to AWS serverless, with the same 4-layer token-budgeted PromptAssembler preserved identically across every deployment. No LangGraph, LlamaIndex, CrewAI, or AutoGen. The final phase features two autonomous agents coordinating via retry feedback loops with a 98 KB zero-dependency pipeline debugger.

- **Multi-Agent Pipeline:** ReAct reasoning loop with hybrid retrieval (vector + BM25), Quality Judge that evaluates chunks and retries with targeted feedback, per-role model selection across 4 pipeline stages
- **Evolution:** v0 (25 tests, Docker Compose, 7 services) -> v1 (section-aware chunking) -> v2 (69 tests, agentic ReAct) -> v3 (multi-agent with inter-agent feedback) -> AgentLens (263 tests, 5-service microservices, NDJSON streaming debugger)
- **Infrastructure:** 7 containers on a single EC2 t3.small via Terraform IaC, Cloudflare SSL, nginx routing — consolidated from 21 containers after retiring v1/v2/v3 stacks
- **Live:** [agentlens.adityonugroho.com](https://agentlens.adityonugroho.com/)

### 5. [Telecom ML](https://github.com/adityonugrohoid/telecom-ml-portfolio)
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

&nbsp;

![Connect](https://img.shields.io/badge/Connect-2d3436?style=for-the-badge)

* **LinkedIn:** [linkedin.com/in/adityonugrohoid](https://linkedin.com/in/adityonugrohoid)
* **Email:** [adityo.nugroho.id@gmail.com](mailto:adityo.nugroho.id@gmail.com)
