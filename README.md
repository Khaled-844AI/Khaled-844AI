# Hi there, I'm Mouad Khaled 👋

<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=3000&pause=1000&color=6366F1&center=true&vCenter=true&width=650&lines=AI+Engineer+%26+VLM+Researcher;Specializing+in+Vision-Language+Models;Building+Production-Grade+Multimodal+AI;Author+of+ShopGuard+(Elsevier+IVC))](https://git.io/typing-svg)

<p align="center">
  <b>Bridging the gap between rigorous Vision-Language research and production-grade intelligent systems.</b>
</p>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/khaled-mouad)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Khaled-844AI)
[![Email](https://img.shields.io/badge/Email-mouadkhaled2004@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mouadkhaled2004@gmail.com)
[![CV](https://img.shields.io/badge/Download_CV-PDF-EC1C24?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)](./CV_khaled_mouad.pdf)
[![Location](https://img.shields.io/badge/Location-Sidi_Bel_Abbes,_Algeria-4CAF50?style=for-the-badge&logo=google-maps&logoColor=white)](https://maps.google.com/?q=Sidi+Bel+Abbes,+Algeria)
[![English](https://img.shields.io/badge/English-IELTS_C1_Proficient-0052CC?style=for-the-badge&logo=academia&logoColor=white)](#languages)

</div>

---

### 📊 Key Impact Metrics

<div align="center">

| **97.5%** | **+72.7%** | **1,357** | **97.0%** | **85.35%** |
| :---: | :---: | :---: | :---: | :---: |
| **Detection Accuracy**<br><sub>Surpasses X3D-S (ShopGuard)</sub> | **Extraction Improvement**<br><sub>QLoRA Fine-Tuned Qwen2.5-VL</sub> | **Curated Dataset**<br><sub>MCU Block Diagram Annotations</sub> | **JSON Validity Rate**<br><sub>Structured VLM Outputs</sub> | **Multi-Modal Re-ID**<br><sub>CLIP-ReID + ArcFace Fusion</sub> |

</div>

---

## 🔬 About Me

I am an **AI Engineer & Vision-Language Model Researcher** pursuing my degree at the **Higher School of Computer Science (ESI-SBA)** and conducting research affiliated with the **LabRI-SBA Lab**.

- 🔭 **Research Focus**: Vision-Language Models (VLMs), multimodal deep learning, temporal attention modeling, video anomaly detection, and person re-identification.
- ⚡ **Engineering Focus**: Parameter-Efficient Fine-Tuning (PEFT / QLoRA) on 7B+ VLMs, structured output extraction, high-throughput model serving (SGLang), and RAG pipelines over vector stores (Pinecone).
- 📝 **Publications**: First author of **ShopGuard**, a temporal attention-based video surveillance architecture under review at *Elsevier (Image and Vision Computing)*.
- 🎯 **Current Endeavors**: Scaling VLM document intelligence for complex engineering schemas & multi-modal agentic workflows.

---

## 📑 Research & Publications

### 📄 ShopGuard: Kinetic Saliency-Contrast Attention for CCTV Shoplifting Detection
[![Status: Active Research / Under Review](https://img.shields.io/badge/Status-Under_Review_%7C_Active_Research-yellow?style=flat-square&logo=academia)](#)
[![Journal](https://img.shields.io/badge/Target-Elsevier_IVC-orange?style=flat-square)](#)

*Under Review at **Image and Vision Computing (IVC)** · **Elsevier** (2026)*  
*Co-authored with **B. Khaldi** (LabRI-SBA Lab, Higher School of Computer Science, ESI-SBA)*

- **The Problem (Surveillance Background Shortcuts)**: In CCTV datasets, static store backgrounds (shelves, fixed lighting, floor tiles) cover >80% of pixels. Conventional video models memorize these camera appearance signatures instead of learning true theft dynamics, leading to false positives on normal customer motions.
- **Core Innovation (Kinetic Saliency-Contrast Attention)**:
  - **100% Frozen Backbone**: Freezes **EfficientNet-B3** spatial extractor (`backbone_lr = 0.0`), feeding a 2-layer **BiGRU** (hidden 512).
  - **Kinetic Action Contrast ($\mathbf{z}_{\text{kinetic}} = \mathbf{z}_{\text{sharp}} - \mathbf{z}_{\text{mean}}$)**: Computes the temporal mean feature ($\mathbf{z}_{\text{mean}}$) representing the static background and subtracts it from the temperature-sharpened peak saliency vector ($\mathbf{z}_{\text{sharp}}$ with $\tau_{\text{sharp}}=0.08$). Stationary scene noise cancels out mathematically ($9.88\times$ noise reduction on walking customers), isolating subtle reaching and concealment micro-gestures.
- **Rigorous Experimental Validation (from Research Log)**:
  - Benchmark-evaluated across **802 real-world CCTV video sequences** under a strict **5-Fold Cross-Validation** protocol across 30+ iterative research phases.
  - **Surpasses 3D CNN Baseline (X3D-S)**: Achieves **97.26% – 97.51% Out-Of-Fold Accuracy** (only 22 total errors vs. 28 errors for X3D-S) with **0.9734 F1-Score** and **0.9805 AUC**.
  - **Zero False Positives**: Delivered **100% precision (0 FP across 482 surveillance videos)** across Folds 0, 1, and 2.
- **Keywords**: `Video Classification` · `Temporal Attention` · `Kinetic Action Contrast` · `CCTV Surveillance` · `BiGRU` · `EfficientNet-B3`

---

## 🚀 Featured Engineering & Research Projects

### 1. [MCUExtract — QLoRA Fine-Tuning of Qwen2.5-VL-7B](https://github.com/Khaled-844AI)
> **Domain-Adapted Vision-Language Model for Technical Diagram Parsing & Structured Extraction**

```
   ┌──────────────────────┐      ┌─────────────────────────┐      ┌─────────────────────────┐
   │ Semiconductor MCU    │ ───► │ Fine-Tuned Qwen2.5-VL   │ ───► │ 97% Valid Schema JSON   │
   │ Architecture Diagram │      │ (QLoRA r=8, α=32, 0.28%)│      │ 30 Modules, 4 Buses...  │
   └──────────────────────┘      └─────────────────────────┘      └─────────────────────────┘
```

- **Problem**: Generalist VLMs fail to reliably parse dense electronic schematic diagrams, hallucinate connections, and fail JSON schema compliance.
- **Solution**: Curated and annotated **1,357 MCU block diagrams** across 6 global semiconductor manufacturers. Fine-tuned **Qwen2.5-VL-7B** using **QLoRA** (rank 8, $\alpha=32$), updating just **0.28%** of model parameters.
- **Results**:
  - **+72.7% average entity extraction gain** over base model.
  - Successfully extracted **30 modules, 4 buses, and 35 connections** (baseline model identified only 16, 3, and 15).
  - **97.0% JSON format validity** under zero-shot schema enforcement prompts.
- **Tech Stack**: `Qwen2.5-VL-7B` · `PEFT / QLoRA` · `Gemini Vision` · `SGLang` · `PyTorch` · `Hugging Face`

---

### 2. [Intelligent Retail Surveillance Platform](https://github.com/Khaled-844AI)
> **Multi-Camera AI Platform: Anomaly Detection, Person Re-ID, and Conversational RAG Analytics**

- **Deployment**: Engineered full 3-subsystem pipeline deployed and benchmarked on **dual Kaggle T4 GPUs**.
- **Subsystems**:
  1. **Temporal Anomaly Engine**: ShopGuard architecture yielding **97.3% – 97.5% accuracy / 0.973 F1** with 100% frozen EfficientNet-B3, outperforming 3D CNN baselines (X3D-S) and delivering 0 false positives across 482 test videos.
  2. **Multi-Modal Person Re-ID**: Fused **CLIP-ReID** body embeddings (1280-D) with **InsightFace / ArcFace** facial embeddings (512-D) and DBSCAN clustering, reaching **85.35% cross-camera search accuracy**.
  3. **Conversational Intelligence**: Orchestrated **Qwen3.5-2B** with **RAG over a Pinecone vector index** to allow store operators to query incident timelines via natural language (e.g., *"Summarize suspicious activity near aisle 4 between 2 PM and 3 PM"*).
- **Tech Stack**: `PyTorch` · `RT-DETR` · `CLIP-ReID` · `ArcFace` · `EfficientNet-B3` · `BiGRU` · `Qwen3.5-2B` · `Pinecone` · `DBSCAN`

---

### 3. [Smart Cars Marketplace & Quality Gating](https://github.com/Khaled-844AI/Cars-MP)
> **Full-Stack Marketplace with Automated Computer Vision Quality Enforcement**

- Built a full-stack luxury vehicle platform with automated CV quality gating.
- Integrated a custom **TensorFlow / Transfer Learning** image classification model that automatically scans user-uploaded vehicle photos and rejects low-quality or damaged image submissions in real-time.
- **Repositories**: [Khaled-844AI/Cars-MP](https://github.com/Khaled-844AI/Cars-MP) · [Khaled-844AI/CarsClassifier](https://github.com/Khaled-844AI/CarsClassifier)
- **Tech Stack**: `TensorFlow` · `Transfer Learning` · `Computer Vision` · `Full-Stack Web`

---

## 🛠️ Technical Arsenal

<div align="center">

### Vision-Language & Multimodal AI
![Qwen](https://img.shields.io/badge/Qwen_2.5--VL_%2F_3.5-5B5BF5?style=flat-square&logo=huggingface&logoColor=white)
![QLoRA](https://img.shields.io/badge/QLoRA_%2F_PEFT-FF6F00?style=flat-square&logo=pytorch&logoColor=white)
![CLIP](https://img.shields.io/badge/CLIP_%2F_CLIP--ReID-000000?style=flat-square&logo=openai&logoColor=white)
![SGLang](https://img.shields.io/badge/SGLang_Serving-FF4081?style=flat-square&logo=fastapi&logoColor=white)
![RAG](https://img.shields.io/badge/RAG_%26_Vector_Search-00ADD8?style=flat-square&logo=google&logoColor=white)
![Structured JSON](https://img.shields.io/badge/Structured_JSON_Prompting-4B0082?style=flat-square&logo=json&logoColor=white)

### Deep Learning & Computer Vision
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![EfficientNet](https://img.shields.io/badge/EfficientNet--B3-02569B?style=flat-square&logo=google&logoColor=white)
![Vision Transformers](https://img.shields.io/badge/ViT-412991?style=flat-square&logo=meta&logoColor=white)
![RT-DETR](https://img.shields.io/badge/RT--DETR-FFD700?style=flat-square&logo=target&logoColor=black)
![ArcFace](https://img.shields.io/badge/ArcFace_%2F_InsightFace-2E7D32?style=flat-square&logo=opencv&logoColor=white)
![BiGRU](https://img.shields.io/badge/BiGRU_%2F_BiLSTM-607D8B?style=flat-square&logo=scikitlearn&logoColor=white)
![Temporal Attention](https://img.shields.io/badge/Temporal_Attention-7B1FA2?style=flat-square&logo=deepnote&logoColor=white)

### MLOps, Databases & Cloud
![Pinecone](https://img.shields.io/badge/Pinecone_Vector_DB-000000?style=flat-square&logo=pinecone&logoColor=white)
![MongoDB Atlas](https://img.shields.io/badge/MongoDB_Atlas-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Kaggle GPU](https://img.shields.io/badge/Kaggle_Dual_T4-20BEFF?style=flat-square&logo=kaggle&logoColor=white)
![Git](https://img.shields.io/badge/Git_%26_GitHub-F05032?style=flat-square&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux_Environments-FCC624?style=flat-square&logo=linux&logoColor=black)

</div>

---

## 🎓 Education & Background

- **Higher School of Computer Science (ESI-SBA)** | Sidi Bel Abbes, Algeria
  - *Engineering Degree in Computer Science* (2023 – Present)
  - Research focus on Vision-Language Models & Computer Vision with **LabRI-SBA**
- **Université Djillali Liabès** | Sidi Bel Abbes, Algeria
  - *Computer Science Preparatory Studies* (2022 – 2023)

### 🌐 Languages
- **Arabic**: Native
- **English**: Professional Working Proficiency (**IELTS C1**)
- **French**: Professional Working Proficiency

---

## 📈 GitHub Statistics & Activity

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=Khaled-844AI&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" width="48%" />
<img src="https://github-readme-streak-stats.herokuapp.com/?user=Khaled-844AI&theme=tokyonight&hide_border=true" width="48%" />

<br/>

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Khaled-844AI&layout=compact&theme=tokyonight&hide_border=true" width="55%" />

</div>

---

## 🤝 Let's Connect & Collaborate!

I am actively seeking research collaborations, industry R&D opportunities, and exciting projects in **Multimodal AI, Vision-Language Fine-Tuning, and Applied Deep Learning**.

- 💼 Connect with me on [LinkedIn](https://linkedin.com/in/khaled-mouad)
- 📬 Reach out directly via [mouadkhaled2004@gmail.com](mailto:mouadkhaled2004@gmail.com)
- 💬 Discuss research ideas or open-source initiatives on [GitHub](https://github.com/Khaled-844AI)

<div align="center">
  <sub>Designed with precision for <b>Mouad Khaled</b> · Built for impactful AI research & engineering.</sub>
</div>
