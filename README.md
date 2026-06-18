# Adityo Nugroho

**AI Engineer shipping production systems and leading AI transformation, on 18 years of telecom network performance at Huawei**

> Multi-agent systems on Google Cloud. Solutions architecture across AWS, Azure, and GCP. Scale-to-zero GPU inference on Kubernetes. Fine-tuned edge models and custom MCP servers.

&nbsp;

![Featured Projects](https://img.shields.io/badge/Featured_Projects-2d3436?style=for-the-badge)

### 1. [NetPulse AI - Multi-Agent Telecom Ops](https://github.com/adityonugrohoid/hackathon-telecom-ops) LIVE
**Multi-agent system on Google Cloud that turns a customer complaint into a triaged NOC incident ticket in under 30 seconds**

A Google ADK `SequentialAgent` orchestrates four `LlmAgent` sub-agents on Gemini (Vertex AI), collapsing the manual NOC workflow of correlating network events, call detail records, and ticketing into one natural-language step. Every LLM call routes through a 4-attempt model-failover ladder shown live in the UI, so a rate-limited model is swapped for the next one on screen instead of failing the request.

- **Top 100 of thousands** at the Google Cloud Gen AI Academy APAC 2026 (Cohort 1), live on Cloud Run at [netpulse-ui.run.app](https://netpulse-ui-670100779564.asia-southeast2.run.app/)
- **Substrate-swappable by design**: the BigQuery + AlloyDB pilot now runs zero-idle-cost on bundled SQLite, swappable back through one MCP Toolbox `tools.yaml` line

### 2. [Cloud Rosetta - One Workload Across AWS, Azure, and GCP](https://github.com/adityonugrohoid/cloud-rosetta)
**Solutions architecture across AWS, Azure, and GCP: the same production workload built 1:1 on all three from a single cloud-neutral contract**

One stateless HTTPS FastAPI service over managed PostgreSQL, with autoscaling, private networking, workload identity, and observability, specified once against a cloud-neutral contract and then implemented identically on AWS, Azure, and GCP. The deliverable is the comparison itself: a defensible three-cloud Bill of Quantities with every line-item cost delta explained, plus a per-cloud evidence pack that proves each requirement on live infrastructure. Built end to end as a self-directed, hands-on study.

- **Defensible cost comparison**: a like-for-like three-cloud Bill of Quantities in one region, with every cost delta traced to a specific service line
- **Keyless by construction**: workload identity on each cloud, checked against a V1-V9 acceptance rubric run on live infra and captured as a screenshot evidence pack

### 3. [Scale-to-Zero GPU Inference](https://github.com/adityonugrohoid/gpu-autoscale-inference)
**Scale-to-zero GPU inference on Kubernetes that costs $0 when idle**

Two-layer autoscaling: KEDA watches Redis queue depth for 0-to-N pod scaling while the GKE Cluster Autoscaler provisions and deprovisions GPU VMs on pending pod scheduling. vLLM serves with continuous batching; model weights persist on a PVC and image layers pre-cache via Secondary Boot Disk, cutting cold start 48% (11 to 5.6 min).

- **True scale-to-zero** at both the pod and node level, $0/hr when idle
- **Full observability**: 12-panel Grafana dashboard (Prometheus + NVIDIA DCGM) plus Locust load testing

### 4. [Edge MCP Caller - 270M Tool-Calling Specialist](https://github.com/adityonugrohoid/edge-mcp-caller)
**A fine-tuned 270M edge model that beats generalist function-callers by baking tool knowledge into its weights**

LoRA (r=128) fine-tuning on Gemma 3 270M moves all 14 tool definitions out of the prompt and into the weights: a ~20-token query goes in, a JSON tool call comes out, regardless of tool count. The result is 99.5% accuracy at 32x fewer prompt tokens than schema-in-prompt baselines, in a 291 MB Q8_0 GGUF that runs on phones, laptops, and Raspberry Pi.

- **Trained on a single consumer GPU** (RTX 4060, 8GB VRAM): 418/420 eval accuracy from 14,033 training examples
- **Fully local, zero API cost**: 14 tools across 2 MCP servers at 153ms average latency

### 5. [Open Telegram Ops - Conversational Job-Costing](https://github.com/adityonugrohoid/open-telegram-ops)
**A custom MCP server behind a Telegram bot: snap a receipt, get live project cost accountability**

Field workers photograph receipts in Telegram; an LLM-vision agent runs OCR to pull amount, vendor, and date, confirms over inline buttons, and writes a per-submitter expense to a SQLite ledger exposed through a custom MCP server. Managers query live budget-vs-actual and get matplotlib charts back in-chat. Built for a real telecom subcontractor whose paper-and-form expense tracking kept failing.

- **Custom 6-tool MCP server** (set_budget, log_expense, query_spend, budget_status, budget_chart, export_ledger) over an async SQLite ledger, with a 37-test pytest suite
- **Self-hosted agent**: OpenClaw runtime on Azure OpenAI vision, Docker Compose deployment; the Azure pilot is archived and production has since moved to AWS

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
