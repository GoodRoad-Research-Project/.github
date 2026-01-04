# 🚦 GoodRoad – Citizen-Powered Intelligent Traffic Violation Reporting System

**GoodRoad** is a comprehensive, AI-driven ecosystem designed to democratize traffic enforcement. It bridges the gap between limited law enforcement resources and road safety needs by enabling citizens to submit dashcam footage, which is then validated, analyzed, and operationalized through a transparent, reward-based framework.

![GoodRoad Banner](https://example.com/link-to-goodroad-banner.png) ---

## 🧭 Table of Contents

1. [Project Overview](#-project-overview)
2. [Core Architecture & Modules](#-core-architecture--modules)
3. [Technologies Used](#️-technologies-used)
4. [System Architecture](#-system-architecture)
5. [Key Objectives](#-key-objectives)
6. [Team Members](#-team-members)
7. [Research Gap](#-research-gap)
8. [Commercialization Strategy](#-commercialization-strategy)
9. [References](#-references)

---

## 📋 Project Overview

Traffic violations are a leading cause of global fatalities, yet traditional enforcement is constrained by infrastructure gaps and human resource limitations. **GoodRoad** introduces a paradigm shift by integrating **Deep Learning**, **Computer Vision**, and **Reinforcement Learning** into a unified pipeline.

The system ingests non-real-time video data from citizen dashcams, validates authenticity (Deep Fake Detection), detects violations under adverse conditions (Hybrid ANPR), explains decisions transparently (Vision-Language Framework), and manages a behavioral economy (Intelligent Rewards).

---

## 🧩 Core Architecture & Modules

The system is composed of four integrated components, executed in the following logical order:

### 1. Enhancing Video Authenticity with Deep Fake Detection Framework
**Focus:** Legal Admissibility & Data Integrity
* **Function:** Validates citizen-submitted dashcam footage to ensure it has not been manipulated.
* **Mechanism:** utilizes a multi-frame analysis approach to detect temporal inconsistencies and visual artifacts typical of deep fake generation (GANs).
* **Outcome:** Filters out manipulated content before processing, ensuring evidence integrity for law enforcement.

### 2. Hybrid ANPR System for Robust Number Plate Detection
**Focus:** Adverse Environmental Robustness
* **Function:** Identifies number plates in challenging scenarios: high speeds (>100 km/h), low light (nighttime/mining sites), and motion blur.
* **Mechanism:** Synergistic integration of **YOLOv9/YOLOv8n** for detection with **EasyOCR**, augmented by **Blind Deconvolution** and **Retinex-based** preprocessing pipelines.
* **Performance:** Targets >98% mAP for detection and >95% recognition accuracy in non-real-time batch processing.

### 3. Vision Language Framework (VLF) for Fair Multi-Class Detection
**Focus:** Explainable AI (XAI) & Fairness
* **Function:** Detects multiple violation types (speeding, lane violations, red lights) and generates natural language explanations for *why* a violation occurred.
* **Mechanism:** A dual-pathway architecture combining Visual Encoders (**ViT/CLIP**) with Language Encoders (**BERT**) to map visual features to traffic rule embeddings.
* **Outcome:** Provides transparent, legally admissible "reasoning chains" and mitigates demographic bias via adversarial debiasing.

### 4. Intelligent Traffic Reward and Behavioural Reinforcement (RDBR)
**Focus:** Behavioral Economics & Reinforcement Learning
* **Function:** Manages the incentive structure for reporters and sanctions for violators.
* **Mechanism:** Uses **Reinforcement Learning (RL)** to dynamically optimize reward distribution based on report accuracy and violation severity. Integrates with mock banking and government APIs to simulate fine issuance and reward payouts.
* **Outcome:** Shifts enforcement from purely punitive to a behavior-reinforcement model, building longitudinal driver profiles.

---

## 🛠️ Technologies Used

| Category | Stack / Tools |
| :--- | :--- |
| **Deep Learning Models** | YOLOv9, YOLOv8n, CLIP, BERT, ViT, EasyOCR, GANs (for debiasing) |
| **Frameworks** | PyTorch 2.x, TensorFlow 2.x, CUDA 11.x |
| **Image Processing** | OpenCV, Blind Deconvolution, Retinex Theory, Motion Deblurring |
| **Reinforcement Learning** | Deep Q-Networks (DQN), Markov Decision Processes (MDP) |
| **Backend & API** | Python 3.9+, Node.js, RESTful APIs, Mock Banking Integrations |
| **Infrastructure** | NVIDIA A100 GPUs, Docker, Cloud Storage (AWS/GCP) |
| **Frontend** | React / React Native (for User Dashboards) |

---

## 🏗️ System Architecture

![System Diagram](https://example.com/system-architecture.png) **Data Flow:**
1.  **Ingestion:** User uploads video -> **Module 1 (Validation)** verifies authenticity.
2.  **Processing:** Validated video -> **Module 2 (ANPR)** extracts vehicle ID -> **Module 3 (VLF)** classifies violation & generates explanation.
3.  **Action:** Analysis Results -> **Module 4 (RDBR)** calculates reward/penalty -> Updates Central Database & Law Enforcement Portal.

---

## 🎯 Key Objectives

* **Authentication:** Achieve >90% accuracy in detecting deep fake manipulations in video evidence.
* **Robustness:** Maintain >95% ANPR accuracy under high-speed (>100 km/h) and low-light conditions.
* **Explainability:** Generate natural language explanations for violations with >85% alignment to human expert assessments.
* **Fairness:** Reduce demographic bias in violation detection to <5% variance across vehicle types.
* **Scalability:** Process 1-minute video segments in <30 seconds for efficient non-real-time batch analysis.

---

## 👥 Team Members

| Student ID | Name | Role / Component |
| :--- | :--- | :--- |
| **IT22148872** | **Wijerathna P. G. S. P.** | Video Authenticity & Deep Fake Detection |
| **IT22174444** | **Rathnayake W.K.D** | Hybrid ANPR & Image Preprocessing |
| **IT22151438** | **Liyanage R. L. N. L.** | Vision-Language Framework (VLF) & XAI |
| **IT22219466** | **Hendawitharana H. W. K. P.** | Reinforcement Learning & Reward Management |

---

## 🔬 Research Gap

Existing Intelligent Transportation Systems (ITS) operate as "black boxes," lacking transparency and failing to leverage citizen participation effectively.

| Feature | Legacy Systems | **GoodRoad Solution** |
| :--- | :--- | :--- |
| **Input Source** | Crowdsourced Dashcam |
| **Adverse Weather** | High Failure Rate | Hybrid Enhancement (De-blur/Low-light) |
| **Legal Transparency** | None (Binary Output) | Natural Language Explanations (XAI) |
| **Evidence Integrity** | Vulnerable to Tampering | Deep Fake Detection Pipeline |
| **Incentive Model** | Punitive Only | RL-Optimized Rewards + Sanctions |

---

## 💰 Commercialization Strategy

**GoodRoad** operates on a B2G (Business-to-Government) and B2C model:
1.  **Government Licensing:** Annual fees for VLF deployment and law enforcement dashboards.
2.  **Transaction Fees:** Commission on citizen rewards processed through the platform.
3.  **Data Intelligence:** Aggregated traffic pattern insights sold to urban planners and insurance firms.
4.  **Cost Reduction:** Estimated **70% reduction** in traditional enforcement costs by automating evidence analysis.

---

## 📚 References

1.  *World Health Organization (WHO)*: Global Status Report on Road Safety.
2.  *YOLO & EasyOCR Literature*: Advances in object detection and optical character recognition.
3.  *Deep Fake Detection*: Temporal inconsistency analysis in video forensics.
4.  *Explainable AI (XAI)*: Multimodal transformers for legal compliance.

---
