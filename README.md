# Adityo Nugroho

**AI Engineer shipping production systems, on 18 years of telecom network performance at Huawei**

> Multi-agent systems on Google Cloud. Scale-to-zero GPU inference on Kubernetes. Terraform on AWS. Fine-tuned specialist models for edge devices.

&nbsp;

![Featured Projects](https://img.shields.io/badge/Featured_Projects-2d3436?style=for-the-badge)

### 1. [NetPulse AI - Multi-Agent Telecom Ops](https://github.com/adityonugrohoid/hackathon-telecom-ops) LIVE
**Four ADK agents turn a customer complaint into a triaged NOC incident ticket in under 30 seconds**

A Google ADK `SequentialAgent` orchestrates four `LlmAgent` sub-agents on Gemini (Vertex AI), collapsing the manual NOC workflow of correlating network events, call detail records, and ticketing into one natural-language step. Every LLM call routes through a 4-attempt model-failover ladder shown live in the UI, so a rate-limited model is swapped for the next one on screen instead of failing the request.

- **Top 100 of thousands** at the Google Cloud Gen AI Academy APAC 2026 (Cohort 1), live on Cloud Run at [netpulse-ui.run.app](https://netpulse-ui-670100779564.asia-southeast2.run.app/)
- **Substrate-swappable by design**: the BigQuery + AlloyDB pilot now runs zero-idle-cost on bundled SQLite, swappable back through one MCP Toolbox `tools.yaml` line

### 2. [Scale-to-Zero GPU Inference](https://github.com/adityonugrohoid/gpu-autoscale-inference)
**Production GPU inference on Kubernetes that costs $0 when idle**

Two-layer autoscaling: KEDA watches Redis queue depth for 0-to-N pod scaling while the GKE Cluster Autoscaler provisions and deprovisions GPU VMs on pending pod scheduling. vLLM serves with continuous batching; model weights persist on a PVC and image layers pre-cache via Secondary Boot Disk, cutting cold start 48% (11 to 5.6 min).

- **True scale-to-zero** at both the pod and node level, $0/hr when idle
- **Full observability**: 12-panel Grafana dashboard (Prometheus + NVIDIA DCGM) plus Locust load testing

### 3. [Edge MCP Caller - 270M Tool-Calling Specialist](https://github.com/adityonugrohoid/edge-mcp-caller)
**A 270M model that beats generalist function-callers by baking tool knowledge into its weights**

LoRA (r=128) fine-tuning on Gemma 3 270M moves all 14 tool definitions out of the prompt and into the weights: a ~20-token query goes in, a JSON tool call comes out, regardless of tool count. The result is 99.5% accuracy at 32x fewer prompt tokens than schema-in-prompt baselines, in a 291 MB Q8_0 GGUF that runs on phones, laptops, and Raspberry Pi.

- **Trained on a single consumer GPU** (RTX 4060, 8GB VRAM): 418/420 eval accuracy from 14,033 training examples
- **Fully local, zero API cost**: 14 tools across 2 MCP servers at 153ms average latency

### 4. [AgentLens on AWS - Infrastructure-as-Code](https://github.com/adityonugrohoid/agentlens-infrastructure)
**The public Terraform and Docker deployment behind a framework-free multi-agent RAG system**

AgentLens is a streaming pipeline debugger for multi-agent RAG, coordinating four roles (Retrieval Agent, Grader, Quality Judge, Fallback) across a 4-service FastAPI stack. This repo is the infrastructure-as-code only (app source stays private), so an infra reviewer can verify the full production architecture without app-repo access: Terraform provisions VPC, EC2 t3.small, and Elastic IP in us-east-1, behind a 7-container Docker Compose stack, path-based nginx, and Cloudflare edge SSL.

- **One-command deploy and teardown** over SSH, with systemd boot automation re-creating the full stack across reboots
- **Offloaded inference**: Ollama Cloud API (no GPU on EC2) plus a ChromaDB vector store; redeployable on demand to [agentlens.adityonugroho.com](https://agentlens.adityonugroho.com/) (demo currently offline)

### 5. [CV Pipeline - Construction Blueprint Analysis](https://github.com/adityonugrohoid/cv-pipeline)
**Three independent detection phases feeding a fault-tolerant orchestrator**

Automates construction blueprint takeoffs by composing three independent CV modules (contour-based shape detection, Tesseract OCR with preprocessing, and a YOLOv8n model fine-tuned on synthetic symbols) into a multi-stage orchestrator. Each phase returns a typed failure object instead of aborting, so a first-run user without trained YOLO weights still gets shape and OCR results. Multi-page PDFs go in, structured JSON takeoff reports come out over a FastAPI endpoint.

- **mAP@50 0.992** on 5 synthetic construction symbol classes, YOLOv8n fine-tuned 20 epochs
- **66 passing tests across 4 phases**, served over FastAPI `POST /analyze` plus a CLI

### 6. [Telecom ML Portfolio](https://github.com/adityonugrohoid/telecom-ml-portfolio)
**Six end-to-end telecom ML projects, each on synthetic data with embedded network physics**

Six self-contained projects spanning classification, regression, time-series, and reinforcement learning. Most ML demos treat telecom as generic tabular data; here each project hand-crafts synthetic data with embedded telecom physics (temporal correlation, spatial clustering, equipment failure signatures), then runs the full paradigm end-to-end from data generation through feature engineering, training, evaluation, and business-insight translation. The repo is an index; source lives in six child repos.

- **Supervised**: Churn AUROC 0.86, RCA Acc@1 0.91, QoE RMSE 0.45, Capacity MAPE 14.5%
- **Unsupervised + RL**: Anomaly F1 0.70, Network Optimization +61% vs random

&nbsp;

![Connect](https://img.shields.io/badge/Connect-2d3436?style=for-the-badge)

* **Location:** Jakarta, Indonesia (UTC+7), open to remote
* **LinkedIn:** [linkedin.com/in/adityonugrohoid](https://linkedin.com/in/adityonugrohoid)
* **Email:** [adityo.nugroho.id@gmail.com](mailto:adityo.nugroho.id@gmail.com)
