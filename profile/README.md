# 🚦 GoodRoad – Citizen-Powered Traffic Violation Reporting System

**GoodRoad** is an integrated Intelligent Transportation System (ITS) designed to democratize traffic enforcement. By leveraging **crowdsourced dashcam footage**, **Deep Learning**, **Computer Vision**, and **Reinforcement Learning**, GoodRoad creates a transparent, scalable, and fair ecosystem for traffic violation reporting. [cite_start]The system ensures evidence authenticity, robust detection under adverse conditions, explainable AI (XAI) for legal transparency, and a dynamic reward mechanism to incentivize positive driving behavior[cite: 1, 1313].

---

## 🧭 Table of Contents

1. [Project Overview](#-project-overview)
2. [Core Components](#-core-components)
3. [Technologies Used](#️-technologies-used)
4. [Objectives](#-objectives)
5. [System Architecture](#-system-architecture)
6. [Team Members](#-team-members)
7. [Research Gap](#-research-gap)
8. [Security & Privacy](#-security--privacy)

---

## 📋 Project Overview

[cite_start]GoodRoad addresses the limitations of traditional traffic enforcement—such as limited coverage and resource constraints—by integrating citizen-submitted video evidence into a rigorous automated pipeline[cite: 58]. The system processes uploaded footage to detect violations, validate evidence integrity against deep fakes, provide legally admissible explanations, and manage a reward/penalty system.

The solution is built on four pillars:
1.  [cite_start]**Authenticity:** Deep fake detection to ensure evidence integrity[cite: 509].
2.  [cite_start]**Robustness:** Hybrid ANPR for high-speed, low-light, and motion-blurred scenarios[cite: 31].
3.  [cite_start]**Transparency:** Vision-Language models to explain *why* a violation occurred[cite: 751].
4.  [cite_start]**Reinforcement:** AI-driven rewards for reporters and compliant drivers[cite: 1291].

---

## 🧩 Core Components

The project is divided into four integrated frameworks, executed in the following order:

### 1. Enhancing Video Authenticity with Deep Fake Detection Framework
* **Focus:** Ensures legal admissibility of citizen-submitted footage.
* [cite_start]**Functionality:** The module acts as the gatekeeper, validating footage to support reliable evidence use[cite: 412]. [cite_start]It employs deep learning to analyze video streams for temporal inconsistencies and visual artifacts, filtering out manipulated content (Deep Fakes) before any violation analysis occurs[cite: 413, 509].

### 2. Hybrid ANPR System for Robust Number Plate Detection
* **Focus:** Handling diverse environmental challenges (Low-light, Motion Blur, High Speed).
* [cite_start]**Functionality:** A hybrid architecture combining **YOLOv9/YOLOv8n** with **EasyOCR** and specialized preprocessing pipelines (Blind Deconvolution, Retinex theory)[cite: 31, 160]. [cite_start]It specifically targets vehicles moving at speeds $>100~km/h$ and utilizes **LPDGAN** (License Plate Deblurring GAN) to resolve motion blur and environmental degradation[cite: 106, 161].

### 3. Vision Language Framework (VLF) for Fair & Transparent Detection
* **Focus:** Multi-class violation detection with natural language explanations (XAI).
* [cite_start]**Functionality:** Uses a dual-pathway transformer architecture (CLIP-based visual encoder + BERT-based language encoder) to detect violations (e.g., illegal lane changes, red light running)[cite: 753, 754]. [cite_start]Crucially, it generates human-readable, legally precise explanations for *why* the action constitutes a violation, addressing the "black box" issue of traditional AI[cite: 752, 756].

### 4. Intelligent Traffic Reward and Behavioural Reinforcement (RDBR)
* **Focus:** Dynamic incentive management and behavioral profiling.
* [cite_start]**Functionality:** An **RL (Reinforcement Learning)** engine that builds longitudinal driver profiles using multi-camera tracking[cite: 1292]. [cite_start]It dynamically calculates rewards for citizens providing valid reports and manages sanctions for violators, utilizing mock banking/government APIs to simulate real-world transactions and ensure transparency[cite: 1293, 1294].

---

## 🛠️ Technologies Used

| Category | Technology | Purpose |
| :--- | :--- | :--- |
| **Frontend** | **React.js** | [cite_start]User dashboard for video upload, reward tracking, and violation review[cite: 925]. |
| **Backend** | **Python / Fast API** | [cite_start]High-performance API handling model inference and system logic[cite: 280]. |
| **AI / ML** | **PyTorch / TensorFlow** | [cite_start]Core deep learning frameworks for YOLO, CLIP, and RL models[cite: 281, 924]. |
| **Computer Vision** | **YOLOv9, YOLOv8n** | [cite_start]Object detection and license plate localization[cite: 31]. |
| **OCR** | **EasyOCR** | [cite_start]Text extraction from license plates[cite: 31]. |
| **Generative AI** | **GANs (LPDGAN)** | [cite_start]Motion deblurring for high-speed vehicle capture[cite: 106]. |
| **NLP** | **BERT, Transformers** | [cite_start]Generating natural language explanations for violations[cite: 754]. |
| **Infrastructure** | **NVIDIA A100 GPUs** | [cite_start]Training and inference hardware[cite: 213]. |

---

## 🎯 Objectives

### Main Objective:
[cite_start]To develop a resilient, integrated, and legally compliant framework for processing citizen-submitted traffic evidence, ensuring high accuracy in detection, robust protection against media manipulation, and effective behavioral modification through incentives[cite: 153, 507, 871, 1355].

### Specific Objectives:
-   [cite_start]**Authenticity:** Achieve high accuracy in detecting deep fake manipulations to maintain evidence integrity[cite: 509].
-   [cite_start]**Robustness:** Attain >95% detection rate for vehicles moving $>100~km/h$ and in low-light conditions[cite: 164].
-   [cite_start]**Explainability:** Generate natural language explanations for violations with >85% accuracy compared to expert assessments[cite: 761].
-   [cite_start]**Reinforcement:** Implement an RL policy to optimize reward distribution and reduce repeat offenses[cite: 1377].

---

## 🏗️ System Architecture

The GoodRoad system follows a sequential pipeline to ensure data integrity and processing efficiency:

1.  [cite_start]**Input Acquisition:** Citizen uploads dashcam video via the Web Portal[cite: 174].
2.  [cite_start]**Validation Module:** Deep fake algorithms verify video authenticity and metadata[cite: 175, 528].
3.  [cite_start]**Preprocessing:** De-blurring and low-light enhancement (Retinex/GANs)[cite: 31, 199].
4.  [cite_start]**VLF Analysis:** Simultaneous violation detection and natural language explanation generation[cite: 177, 756].
5.  [cite_start]**Vehicle ID:** Hybrid ANPR extracts license plate data and classifies vehicles[cite: 181].
6.  [cite_start]**RDBR Engine:** RL model updates driver profiles, calculates rewards, and reinforces behavior[cite: 183, 1293].
7.  [cite_start]**Output:** Automated report generation for Law Enforcement and banking API triggers[cite: 184, 1294].

---

## 👥 Team Members

| Student ID | Name | Component Responsibility |
| :--- | :--- | :--- |
| **IT22148872** | **Wijerathna P. G. S. P.** | [cite_start]Enhancing Video Authenticity with Deep Fake Detection Framework [cite: 405] |
| **IT22174444** | **Rathnayake W.K.D** | [cite_start]Hybrid ANPR System for Robust Number Plate Detection [cite: 21] |
| **IT22151438** | **Liyanage R. L. N. L.** | [cite_start]Vision Language Framework for Fair and Transparent Violation Detection [cite: 745] |
| **IT22219466** | **Hendawitharana H. W. K. P.** | [cite_start]Intelligent Traffic Reward and Behavioural Reinforcement Management [cite: 1286] |

---

## 🔬 Research Gap

Existing systems often operate in silos—focusing solely on ANPR or violation detection—without addressing the chain of custody or "black box" AI issues. GoodRoad fills these gaps by:
1.  [cite_start]**Addressing Evidence Integrity:** Unlike standard systems, we integrate deep fake detection as a prerequisite for processing citizen-submitted footage[cite: 412].
2.  [cite_start]**Environmental Generalization:** We move beyond static datasets to handle real-world motion blur (vehicles $>100~km/h$) and low light simultaneously[cite: 126, 130].
3.  [cite_start]**Explainability (XAI):** We replace opaque output labels with natural language reasoning, essential for legal admissibility[cite: 752].
4.  [cite_start]**Positive Reinforcement:** We shift from a purely punitive model to one that rewards compliance using Reinforcement Learning[cite: 1355].

---

## 🛡️ Security & Privacy

* [cite_start]**Data Anonymization:** Automatic blurring of faces and non-violating license plates to comply with privacy regulations[cite: 196, 969].
* [cite_start]**Encryption:** End-to-end encryption (AES-256) for video transmission and storage[cite: 265, 1539].
* [cite_start]**Access Control:** Role-based access for Law Enforcement and System Admins[cite: 265].
* [cite_start]**Audit Trails:** Tamper-evident logs for all automated decisions and banking simulations[cite: 1457].
