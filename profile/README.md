Here is the modified `README.md` file tailored to the **GoodRoad** project specifications, incorporating the technical details, architecture, and specific components outlined in your provided documents.

---

# 🚦 GoodRoad – Citizen-Powered Traffic Violation Reporting System

Welcome to **GoodRoad**, a comprehensive Intelligent Transportation System (ITS) designed to democratize traffic enforcement. By leveraging **crowdsourced dashcam footage**, **Deep Learning**, **Computer Vision**, and **Reinforcement Learning**, GoodRoad creates a transparent, scalable, and fair ecosystem for traffic violation reporting. The system ensures evidence authenticity, robust detection under adverse conditions, explainable AI (XAI) for legal transparency, and a dynamic reward mechanism to incentivize positive driving behavior.

---

## 🧭 Table of Contents

1. [Project Overview](https://www.google.com/search?q=%23-project-overview)
2. [Core Components](https://www.google.com/search?q=%23-core-components)
3. [Technologies Used](https://www.google.com/search?q=%23%EF%B8%8F-technologies-used)
4. [Objectives](https://www.google.com/search?q=%23-objectives)
5. [System Architecture](https://www.google.com/search?q=%23-system-architecture)
6. [Team Members](https://www.google.com/search?q=%23-team-members)
7. [Research Gap](https://www.google.com/search?q=%23-research-gap)
8. [Security & Privacy](https://www.google.com/search?q=%23-security--privacy)
9. [References](https://www.google.com/search?q=%23-references)

---

## 📋 Project Overview

GoodRoad addresses the limitations of traditional traffic enforcement (limited coverage, resource constraints) by integrating citizen-submitted video evidence into a rigorous automated pipeline. The system processes uploaded footage to detect violations, validate evidence integrity against deep fakes, provide legally admissible explanations, and manage a reward/penalty system.

The solution is built on four pillars:

1. **Authenticity:** Deep fake detection to ensure evidence integrity.
2. **Robustness:** Hybrid ANPR for high-speed, low-light, and motion-blurred scenarios.
3. **Transparency:** Vision-Language models to explain *why* a violation occurred.
4. **Reinforcement:** AI-driven rewards for reporters and compliant drivers.

---

## 🧩 Core Components

The project is divided into four integrated frameworks, executed in the following order:

### 1. Enhancing Video Authenticity with Deep Fake Detection Framework

* **Focus:** Ensures legal admissibility of citizen-submitted footage.
* **Functionality:** Analyzes video streams for temporal inconsistencies and visual artifacts to detect manipulation. It filters out deep fakes before any violation analysis occurs, utilizing multi-frame analysis and metadata validation.



### 2. Hybrid ANPR System for Robust Number Plate Detection

* **Focus:** Handling diverse environmental challenges (Low-light, Motion Blur, High Speed).
* **Functionality:** A hybrid architecture combining **YOLOv9/YOLOv8n** with **EasyOCR** and **LPDGAN** (License Plate Deblurring GAN). It utilizes Retinex theory for low-light enhancement and blind deconvolution for motion blur caused by vehicles speeds .



### 3. Vision Language Framework (VLF) for Fair & Transparent Detection

* **Focus:** Multi-class violation detection with natural language explanations (XAI).
* 
**Functionality:** Uses a dual-pathway transformer architecture (CLIP-based visual encoder + BERT-based language encoder) to detect violations (e.g., illegal lane changes, red light running) and generate human-readable, legally precise explanations for *why* the action constitutes a violation.



### 4. Intelligent Traffic Reward and Behavioural Reinforcement (RDBR)

* **Focus:** Dynamic incentive management and behavioral profiling.
* **Functionality:** An **RL (Reinforcement Learning)** engine that builds longitudinal driver profiles. It dynamically calculates rewards for citizens providing valid reports and manages sanctions for violators, utilizing mock banking/government APIs for transaction simulation.



---

## 🛠️ Technologies Used

| Category | Technology | Purpose |
| --- | --- | --- |
| **Frontend** | **React.js** | User dashboard for video upload, reward tracking, and violation review.

 |
| **Backend** | **Python / Fast API** | High-performance API handling model inference and system logic. |
| **AI / ML** | **PyTorch / TensorFlow** | Core deep learning frameworks for YOLO, CLIP, and RL models.

 |
| **Computer Vision** | **YOLOv9, YOLOv8n** | Object detection and license plate localization.

 |
| **OCR** | **EasyOCR** | Text extraction from license plates.

 |
| **Generative AI** | **GANs (LPDGAN)** | Motion deblurring for high-speed vehicle capture.

 |
| **NLP** | **BERT, Transformers** | Generating natural language explanations for violations.

 |
| **Infrastructure** | **NVIDIA A100 GPUs** | Training and inference hardware.

 |

---

## 🎯 Objectives

### Main Objective:

To develop a resilient, integrated, and legally compliant framework for processing citizen-submitted traffic evidence, ensuring high accuracy in detection (>95%), robust protection against media manipulation, and effective behavioral modification through incentives.

### Specific Objectives:

* 
**Authenticity:** Achieve >90% accuracy in detecting deep fake manipulations in dashcam footage.


* 
**Robustness:** Attain >95% detection rate for vehicles moving  and in low-light conditions.


* 
**Explainability:** Generate natural language explanations for violations with >85% accuracy compared to expert assessments.


* 
**Reinforcement:** Implement an RL policy to optimize reward distribution and reduce repeat offenses.



---

## 🏗️ System Architecture

The GoodRoad system follows a sequential pipeline to ensure data integrity and processing efficiency.

Figure: High-level data flow from Citizen Upload -> Validation -> Identification -> Analysis -> Reward Distribution.

1. **Input Acquisition:** Citizen uploads dashcam video via the Web Portal.
2. **Validation Module:** Deep fake algorithms verify video authenticity.
3. **Preprocessing:** De-blurring and low-light enhancement (Retinex/GANs).
4. **VLF Analysis:** Simultaneous violation detection and text explanation generation.
5. **Vehicle ID:** Hybrid ANPR extracts license plate data.
6. **RDBR Engine:** RL model updates driver profiles and calculates rewards/penalties.
7. **Output:** Automated report generation for Law Enforcement and banking API triggers.

---

## 👥 Team Members

| Student ID | Name | Component Responsibility |
| --- | --- | --- |
| **IT22148872** | **Wijerathna P. G. S. P.** | Enhancing Video Authenticity with Deep Fake Detection Framework 

 |
| **IT22174444** | **Rathnayake W.K.D** | Hybrid ANPR System for Robust Number Plate Detection 

 |
| **IT22151438** | **Liyanage R. L. N. L.** | Vision Language Framework for Fair and Transparent Violation Detection 

 |
| **IT22219466** | **Hendawitharana H. W. K. P.** | Intelligent Traffic Reward and Behavioural Reinforcement Management 

 |

---

## 🔬 Research Gap

Existing systems often operate in silos—focusing solely on ANPR, or solely on violation detection—without addressing the chain of custody or "black box" AI issues. GoodRoad fills these gaps by:

1. 
**Addressing Evidence Integrity:** Unlike standard systems, we integrate deep fake detection as a prerequisite for processing.


2. 
**Environmental Generalization:** We move beyond static datasets (like CCPD) to handle real-world motion blur and low light simultaneously.


3. 
**Explainability (XAI):** We replace opaque output labels with natural language reasoning, essential for legal admissibility.


4. 
**Positive Reinforcement:** We shift from a purely punitive model to one that rewards compliance using Reinforcement Learning.



---

## 🛡️ Security & Privacy

* 
**Data Anonymization:** Automatic blurring of faces and non-violating license plates to comply with privacy regulations.


* 
**Encryption:** End-to-end encryption (AES-256) for video transmission and storage.


* 
**Access Control:** Role-based access for Law Enforcement and System Admins.


* 
**Audit Trails:** Tamper-evident logs for all automated decisions and banking simulations.



---

## 📚 References

* [1] Good Road - Citizen-Powered Traffic Violation Reporting System Project Proposal.


* [2] H. Gong et al., "A Dataset and Model for Realistic License Plate Deblurring," IJCAI-24.


* [3] L. Zhang et al., "Multi-task learning framework for automated traffic violation recognition," IEEE Access.


* [4] Chen, Y., & Wang, S. (2025). Optimization of dynamic incentive strategies for public transportation based on reinforcement learning.
