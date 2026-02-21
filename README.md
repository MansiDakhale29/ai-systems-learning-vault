
#  AI Systems Learning Vault

> **Building production-grade AI systems — LLMs, MLOps pipelines, Computer Vision & Medical AI — with evaluation and deployment at the core.**

---

##  About This Repository

This repository documents my structured learning and hands-on implementations across LLM engineering, MLOps, Computer Vision, and Medical AI.

The focus is **not** on isolated model training or tutorial reproduction.  
The focus **is** on engineering decisions, system design, evaluation pipelines, and production awareness.

Every section answers one question:  
**"What engineering problem does this demonstrate — and how would it behave at scale?"**

---

## 🗂 Repository Structure

```
ai-systems-learning-vault/
│
├── 01_llm_engineering/          # Prompt design, RAG systems, guardrails, evaluation
├── 02_mlops_and_deployment/     # Experiment tracking, Dockerized APIs, CI/CD
├── 03_computer_vision/          # ViT vs CNN, diffusion models, grounding
├── 04_medical_ai/               # 3D MRI pipelines, GAN training, clinical evaluation
└── assets/                      # Architecture diagrams, charts, visuals
```

---

##  Phase 1 — LLM Engineering [`01_llm_engineering/`]

> *This section explores scalable LLM systems with structured prompt design, retrieval-augmented generation, and production-grade fallback logic.*

### What's inside:
- **Prompt Engineering** — Systematic before/after comparisons with evaluation scoring. Documents what failed, what improved, and why — not just the final output.
- **RAG System** — End-to-end retrieval-augmented generation: document ingestion → embedding → retrieval → answer generation → basic evaluation. Includes architecture diagram.
- **Guardrails & Fallback Logic** — Input validation, output format enforcement, and fallback model routing. Demonstrates defensive LLM system design.

### Key engineering questions answered:
- How do you make prompt changes measurable, not just subjective?
- How do you build a RAG pipeline that degrades gracefully under poor retrieval?
- How do you prevent an LLM API from silently failing in production?

---

##  Phase 2 — MLOps & Deployment [`02_mlops_and_deployment/`]

> *This section demonstrates production maturity: experiment tracking, containerization, logging, and deployment patterns for ML systems.*

### What's inside:
- **Dockerized LLM API** — Containerized FastAPI service wrapping an LLM endpoint. Includes health checks and environment config.
- **MLflow Experiment Tracking** — Structured experiment logging with parameter tracking, metric comparison, and model registry basics.
- **Logging & Observability Setup** — Structured logging patterns for ML services. What to log, when, and how to make it queryable.
- **CI/CD Notes** — GitHub Actions YAML examples for automated testing and model validation pipelines.

### Key engineering questions answered:
- How do you ensure your model experiments are reproducible six months later?
- How do you make an LLM API observable in production?
- What does a basic ML deployment pipeline look like end-to-end?

---

##  Phase 3 — Computer Vision [`03_computer_vision/`]

> *This section compares architectural choices in vision models and explores generative approaches — with a focus on when and why to use each.*

### What's inside:
- **ViT vs CNN Comparison** — Structured comparison of Vision Transformers and CNNs on the same task. Evaluation goes beyond accuracy: inference speed, data efficiency, failure cases.
- **Diffusion Model Experiments** — Notes and minimal implementation exploring diffusion-based generation. Focuses on the denoising process conceptually and practically.
- **Visual Grounding** — Connecting language queries to spatial image regions. Architecture explanation with use-case motivation.

### Key engineering questions answered:
- When does a ViT outperform a CNN — and when does it not?
- What makes diffusion models slow, and how is that being addressed?

---

##  Phase 4 — Medical AI [`04_medical_ai/`]

> *This section documents real challenges in applying AI to medical imaging: 3D data pipelines, generative modeling for augmentation, and clinically-motivated evaluation.*

### What's inside:
- **3D MRI Pipeline Architecture** — End-to-end pipeline design for volumetric medical data. Covers preprocessing, patch extraction, and inference strategies.
- **GAN Training for Medical Augmentation** — Generative adversarial training applied to limited medical datasets. Covers training instability, evaluation with FID & clinical metrics, and lessons learned.
- **Evaluation Metrics Deep Dive** — Why accuracy is insufficient for medical AI. Covers Dice, Hausdorff distance, sensitivity/specificity trade-offs, and clinical validation thinking.
- **Lessons from Real Constraints** — CUDA OOM debugging, handling class imbalance in 3D data, working with anonymized datasets. Real problems, real fixes.

### Key engineering questions answered:
- How do you build a data pipeline for 3D medical images that doesn't blow up memory?
- How do you evaluate a GAN when you can't crowdsource labels?
- What makes a medical AI model trustworthy enough to present to clinicians?

---

##  Design Philosophy

Every module in this repo follows a consistent structure:

```
feature_name/
│
├── README.md              ← What problem this solves, design decisions, lessons
├── implementation.py      ← Minimal, clean, well-commented working code
├── experiments/           ← What was tried, what failed, what worked
└── architecture.png       ← Visual of the system or approach
```

**Code volume is not the goal. Engineering clarity is.**

---

##  Tech Stack

| Area | Tools |
|---|---|
| LLM APIs | OpenAI, Anthropic, HuggingFace |
| RAG | LangChain / LlamaIndex, FAISS, ChromaDB |
| MLOps | MLflow, Docker, GitHub Actions |
| CV | PyTorch, timm, OpenCV, Diffusers |
| Medical AI | MONAI, nibabel, SimpleITK |
| Evaluation | RAGAS, sklearn metrics, custom scripts |

---

##  Maintenance Cadence

This repository is actively maintained on a weekly basis:

-  1 small improvement or new experiment added
-  1 module refactored for clarity
-  README updated to reflect current understanding

Last updated: **June 2025**

---

##  Connect

**Mansi** — AI/ML Engineer focused on production LLM systems and Medical AI  
📍 [LinkedIn](#) · 📧 [Email](#) · 🐦 [Twitter/X](#)

> *"The goal isn't to train the best model. The goal is to build a system that works reliably in the real world."*

---
