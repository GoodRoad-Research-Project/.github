# 🚦 GoodRoad – Citizen-Powered Traffic Violation Reporting System

Welcome to **GoodRoad**, a pioneering **AI-driven traffic enforcement platform** that empowers citizens to contribute to road safety. By integrating **dashcam footage**, **computer vision**, and **blockchain-inspired reward mechanisms**, GoodRoad shifts traffic management from a purely punitive model to a balanced, adaptive framework that incentivizes safe driving while ensuring fair, transparent, and evidence-based enforcement.

---

## 🧭 Table of Contents

1. [Project Overview](https://www.google.com/search?q=%23-project-overview)
2. [Key Functions](https://www.google.com/search?q=%23-key-functions)
3. [Technologies Used](https://www.google.com/search?q=%23%EF%B8%8F-technologies-used)
4. [Objectives](https://www.google.com/search?q=%23-objectives)
5. [System Architecture](https://www.google.com/search?q=%23-system-architecture)
6. [Team Members](https://www.google.com/search?q=%23-team-members)
7. [Research Gap](https://www.google.com/search?q=%23-research-gap)
8. [Commercialization & Impact](https://www.google.com/search?q=%23-commercialization--impact)
9. [References](https://www.google.com/search?q=%23-references)

---

## 📋 Project Overview

Traffic violations are a leading cause of global road accidents, yet traditional enforcement is limited by resource constraints and coverage gaps. **GoodRoad** bridges this gap by creating a unified ecosystem where:

* **Citizens** upload dashcam footage of violations.
* **AI Models** validate authenticity, detect specific infractions, and identify vehicles under challenging conditions.
* **Reporters** earn rewards for valid submissions, and **Drivers** earn bonuses for consistent compliant behavior.

The system ensures legal admissibility through deep fake detection and provides human-readable explanations for every AI decision.

---

## 🚀 Key Functions

The core functionality of GoodRoad is divided into four specialized components, executed in the following order:

### 1. ENHANCING VIDEO AUTHENTICITY WITH DEEP FAKE DETECTION FRAMEWORK

**Goal:** Ensure the integrity and legal admissibility of citizen-submitted evidence.

* **Deep Fake Detection:** Analyzes video streams for signs of manipulation (e.g., face swapping, scene alteration) using advanced CNNs.
* **Metadata Verification:** Validates GPS, timestamps, and device signatures to prevent tampering.
* **Outcome:** Filters out malicious submissions and guarantees that only authentic footage reaches law enforcement.

### 2. Hybrid ANPR System for Robust Number Plate Detection Under Diverse Environmental Challenges

**Goal:** Accurately identify vehicles in non-ideal real-world conditions.

* **Adverse Condition Handling:** Optimized for high-speed vehicles (>100 km/h), low-light/nighttime environments, and motion blur.
* **Hybrid Architecture:** Synergizes **YOLOv9/YOLOv8n** for detection with **EasyOCR** and specialized deblurring (LPDGAN)/enhancement (Retinex) pipelines.
* **Outcome:** Achieves high-accuracy vehicle identification where traditional ANPR fails.

### 3. VISION LANGUAGE FRAMEWORK FOR FAIR AND TRANSPARENT MULTI-CLASS TRAFFIC VIOLATION DETECTION

**Goal:** Detect violations with transparency and fairness, moving away from "black-box" AI.

* **Multimodal Analysis:** Uses a **Dual-Pathway Architecture** (Visual + Language Encoders) based on CLIP/ViT foundations to understand complex scenes.
* **Multi-Class Detection:** Simultaneously identifies speeding, red-light running, illegal lane changes, etc.
* **Explainable AI (XAI):** Generates natural language explanations citing specific traffic rules for every detected violation.
* **Fairness:** Implements adversarial debiasing to ensure equitable detection across different vehicle types and demographics.

### 4. INTELLIGENT TRAFFIC REWARD AND BEHAVIOURAL REINFORCEMENT MANAGEMENT FRAMEWORK

**Goal:** Promote disciplined driving through dynamic incentives.

* **Reinforcement Learning (RL):** An AI engine dynamically calibrates rewards for reporters and penalties for offenders based on behavioral trends.
* **Mock Banking API:** Simulates real-world transaction handling for reward distribution and fine processing.
* **Gamification:** Dashboards for drivers to track compliance scores and earn bonuses for safe driving streaks.

---

## 🛠️ Technologies Used

| Category | Technology Stack |
| --- | --- |
| **Frontend** | **React.js** (Web Dashboards for Citizens & Authorities) |
| **Backend** | **Python**, **FastAPI** (High-performance API layer) |
| **Computer Vision** | **YOLOv9 / YOLOv8**, **OpenCV**, **ResNet-50**, **Vision Transformers (ViT)** |
| **OCR & Text** | **EasyOCR**, **BERT**, **CLIP** (Multimodal embeddings) |
| **AI/ML Core** | **PyTorch**, **TensorFlow**, **Reinforcement Learning (RL)**, **GANs** |
| **Data & Storage** | **Firebase** / **Cloud Storage** (Video Data), **SQL/NoSQL Databases** |
| **Integration** | **REST APIs**, **Mock Banking APIs**, **OAuth 2.0** |

---

## 🎯 Objectives

### Main Objective:

To develop a comprehensive, citizen-powered traffic enforcement ecosystem that ensures evidence authenticity, robust detection in all environments, transparent decision-making, and positive behavioral reinforcement.

### Specific Objectives:

* **Validation:** Achieve >90% success rate in detecting deep fake manipulations in uploaded video.
* **Robustness:** Maintain >95% ANPR accuracy for vehicles moving >100km/h and in low-light conditions.
* **Transparency:** Generate legally precise natural language explanations for 100% of reported violations.
* **Fairness:** Reduce demographic/vehicle-type bias in detection to <5% variance.
* **Engagement:** Create a sustainable economic model where valid reporting is rewarded and safe driving is incentivized.

---

## 🏗️ System Architecture

The GoodRoad system follows a sequential data pipeline:

1. **Input:** User uploads dashcam footage via React Frontend.
2. **Validation Layer:** Deep Fake Detection Framework verifies integrity.
3. **Processing Layer:**
* **VLF:** Detects violation type and generates XAI explanation.
* **Hybrid ANPR:** Identifies vehicle license plate under challenging conditions.


4. **Decision Layer:** Data is aggregated to profile driver behavior.
5. **Output:**
* **RL Engine:** Calculates Reward (for reporter) or Penalty (for driver).
* **Enforcement Portal:** Law enforcement reviews the generated evidence package.



---

## 👥 Team Members

| Student ID | Name | Role / Component |
| --- | --- | --- |
| **IT22148872** | **Wijerathna P. G. S. P.** | Video Authenticity & Deep Fake Detection |
| **IT22174444** | **Rathnayake W.K.D** | Hybrid ANPR System (Robust Detection) |
| **IT22151438** | **Liyanage R. L. N. L.** | Vision-Language Framework (Violation Detection) |
| **IT22219466** | **Hendawitharana H. W. K. P.** | Reward & Behavioural Reinforcement Manager |

---

## 🔬 Research Gap

While existing Automated Traffic Enforcement Systems (ATES) exist, GoodRoad addresses critical shortcomings:

| Feature | Traditional Systems | GoodRoad Solution |
| --- | --- | --- |
| **Evidence Source** | Fixed Cameras Only | **Crowdsourced Dashcams (Scalable)** |
| **Trust/Integrity** | Vulnerable to manipulation | **Integrated Deep Fake Detection** |
| **Environmental Limits** | Fails in rain/night/high-speed | **Hybrid ANPR with Deblurring/Enhancement** |
| **Interpretability** | "Black Box" (No reasoning) | **Vision-Language Model (Natural Language Explanations)** |
| **Enforcement Model** | Punitive Only (Fines) | **Hybrid (Rewards for Good Drivers + Fines)** |

---

## 🛡️ Commercialization & Impact

* **B2G (Business-to-Government):** Licensing the platform to Traffic Police and Ministries of Transport for scalable, cost-effective enforcement (estimated 70% cost reduction vs. manual patrols).
* **B2C (Business-to-Consumer):** Commission-based model where citizens earn income for valid reports, democratizing traffic safety.
* **Target Audience:** Law Enforcement Agencies, Insurance Companies, Dashcam Owners, Urban Planners.

---

## 📚 References

1. World Health Organization (WHO): Global Status Report on Road Safety.
2. Department of Police, Sri Lanka: Annual Traffic Accident Reports.
3. Recent studies on YOLOv8, Vision Transformers, and Reinforcement Learning in ITS (Intelligent Transportation Systems).

---

*Project ID: 25-26J-265*
