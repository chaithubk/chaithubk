<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=667EEA&center=true&vCenter=true&width=850&lines=Hi%2C+I'm+Krishna+Chaithanya+%F0%9F%91%8B;Clinical+Systems+Architect+%E2%86%92+Technical+Product+Leader;18%2B+Years+Philips+Healthcare+%7C+MedTech+Domain+Expert;Building+AI-Augmented+Medical+Device+Platforms" alt="Typing SVG" />
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/krishnachaithanyab/">
    <img src="https://img.shields.io/badge/LinkedIn-Krishna%20Chaithanya-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="mailto:chaithanya.balakavi@gmail.com">
    <img src="https://img.shields.io/badge/Email-chaithanya.balakavi%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
  <a href="https://www.google.com/maps/place/Bangalore">
    <img src="https://img.shields.io/badge/📍_Bangalore-India-667EEA?style=for-the-badge" alt="Location" />
  </a>
</p>

---

## 🧠 About Me

I am a **Software Architect II at Philips Healthcare** with 18+ years of deep specialisation in
safety-critical patient monitoring systems — the bedside devices that track vital signs, escalate
alarms, and support clinical decisions in ICUs and cardiac care units.

My work spans the full stack:

- ⚙️ **Hardware & OS** — Yocto BSP, embedded Linux hardening, bare-metal firmware
- 💻 **Middleware** — C++17, MQTT, AMQP, HL7, real-time data pipelines
- 🎨 **Clinical UI** — Qt6/QML, IEC 60601-1-8 alarm design, bedside UX
- 🛡️ **Regulatory** — IEC 62304, SBOM, FDA cybersecurity guidance, DHF traceability
- 🤖 **AI/Edge** — TensorFlow Lite, on-device inference, clinical AI validation

I am now deliberately expanding from **"how to build"** to **"what and why to build"** —
transitioning into **Technical Product Management**, building hands-on fluency through an
independent portfolio that stress-tests real MedTech regulatory and architectural decisions.

---

## 🏗️ The MedTech Platform Portfolio

> A 7-repository, AI-augmented medical device platform built to demonstrate
> **Product Leadership through Technical Excellence** — de-risking Feasibility,
> Viability, and Value across independently-auditable, CI/CD-gated repositories.

### Platform Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                  MEDTECH PATIENT MONITORING PLATFORM                │
├──────────────────────┬──────────────────────┬───────────────────────┤
│   FEASIBILITY RISK   │  INTELLIGENCE RISK   │     VALUE RISK        │
│                      │                      │                       │
│  medtech-vitals-     │  medtech-edge-       │  medtech-clinician-   │
│  publisher           │  analytics           │  ui                   │
│                      │                      │                       │
│  MQTT vital signs    │  TFLite sepsis       │  IEC 60601-1-8        │
│  3 clinical          │  prediction          │  alarm dashboard      │
│  scenarios           │  <100ms on-device    │  Qt6 / QML / C++17    │
├──────────────────────┴──────────────────────┴───────────────────────┤
│  VIABILITY RISK                    │  SCALE RISK                    │
│                                    │                                │
│  medtech-device-os                 │  medtech-telemetry-cloud       │
│                                    │                                │
│  Yocto kirkstone · meta-medtech    │  HIPAA-ready · FastAPI         │
│  Systemd service chain             │  Multi-hospital aggregation    │
│  QEMU ARM64 · SBOM · CI→GHCR       │  FHIR-ready · docker-compose   │
├────────────────────────────────────┴────────────────────────────────┤
│  INTEGRATION                        KNOWLEDGE                       │
│                                                                     │
│  medtech-platform                   medtech-embedded-systems-       │
│  Git submodules + docker-compose    handbook                        │
│  Full-stack orchestration           16-chapter field guide          │
└─────────────────────────────────────────────────────────────────────┘
```

### The Integration Milestone

> **`medtech-device-os` integrates the entire platform as a single bootable Linux image.**

All four application services run as a systemd-orchestrated chain on QEMU ARM64:

```
mosquitto.service
  └── medtech-vitals-publisher.service   (Python · MQTT)
              └── medtech-clinician-ui.service   (Qt6 · alarm dashboard)
```

---

## 📦 Repository Map

| Repository | Risk De-Risked | Core Technology | Status |
|---|---|---|---|
| [medtech-device-os](https://github.com/chaithubk/medtech-device-os) | Viability — OS + Integration | Yocto · BitBake · systemd · QEMU | ✅ Stage 1 Live |
| [medtech-platform](https://github.com/chaithubk/medtech-platform) | Integration — Full Platform | Git submodules · docker-compose | ✅ Live |
| [medtech-vitals-publisher](https://github.com/chaithubk/medtech-vitals-publisher) | Feasibility — Data Ingestion | Python · paho-mqtt · Mosquitto | ✅ Complete |
| [medtech-clinician-ui](https://github.com/chaithubk/medtech-clinician-ui) | Value — Safety-Critical UX | Qt6 · QML · C++17 · CMake | 🔄 Active |
| [medtech-edge-analytics](https://github.com/chaithubk/medtech-edge-analytics) | Intelligence — Predictive AI | TFLite · Python · ARM edge | 🔄 Active |
| [medtech-telemetry-cloud](https://github.com/chaithubk/medtech-telemetry-cloud) | Scale — HIPAA Aggregation | FastAPI · FHIR · docker-compose | 🔄 Active |
| [medtech-embedded-systems-handbook](https://github.com/chaithubk/medtech-embedded-systems-handbook) | Knowledge — TPM Reference | 16 chapters · Markdown | 🔄 Expanding |

---

## 🏆 What This Portfolio Proves

Every repository in this portfolio is built with three parallel outputs:

**① Technical Artifact**
Working prototype with CI/CD gates, test coverage, linting enforcement,
and Docker-based reproducible builds.

**② Product Artifact**
Product Requirements Documents (PRDs using Cagan INSPIRED framework),
Architecture Decision Records (ADRs), acceptance criteria tied to
clinical outcomes — not just technical specs.

**③ Regulatory Artifact**
Compliance annotations, CycloneDX + SPDX SBOM generation, IEC/FDA
standard references in documentation, and audit-trail-ready CI pipelines.

> In MedTech, engineering, product, and compliance are not separate conversations.
> This portfolio treats them as one.

---

## 🛠️ Full Tech Stack

**Embedded & OS**

![Yocto](https://img.shields.io/badge/Yocto-kirkstone-339933?style=flat-square&logo=linux&logoColor=white)
![Embedded Linux](https://img.shields.io/badge/Embedded%20Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![QEMU](https://img.shields.io/badge/QEMU-ARM64-FF6600?style=flat-square)
![systemd](https://img.shields.io/badge/systemd-Service%20Orchestration-black?style=flat-square)
![BitBake](https://img.shields.io/badge/BitBake-Recipes-339933?style=flat-square)

**Languages & Middleware**

![C++](https://img.shields.io/badge/C++-17-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python&logoColor=white)
![MQTT](https://img.shields.io/badge/MQTT-paho-660066?style=flat-square&logo=mqtt&logoColor=white)
![AMQP](https://img.shields.io/badge/AMQP-FF6600?style=flat-square&logo=rabbitmq&logoColor=white)
![HL7](https://img.shields.io/badge/HL7-FHIR-E53935?style=flat-square)

**UI & Frontend**

![Qt6](https://img.shields.io/badge/Qt6-QML-41CD52?style=flat-square&logo=qt&logoColor=white)
![CMake](https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white)

**AI & Edge**

![TFLite](https://img.shields.io/badge/TensorFlow%20Lite-Edge%20AI-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![TinyML](https://img.shields.io/badge/TinyML-ARM%20Cortex--A-8A2BE2?style=flat-square)

**Cloud & Platform**

![FastAPI](https://img.shields.io/badge/FastAPI-HIPAA%20Ready-009688?style=flat-square&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Compose-2496ED?style=flat-square&logo=docker&logoColor=white)
![GHCR](https://img.shields.io/badge/GHCR-Container%20Registry-181717?style=flat-square&logo=github&logoColor=white)

**Regulatory & Compliance**

![IEC 62304](https://img.shields.io/badge/IEC%2062304-Software%20Lifecycle-E53935?style=flat-square)
![IEC 60601](https://img.shields.io/badge/IEC%2060601--1--8-Alarm%20Design-E53935?style=flat-square)
![SBOM](https://img.shields.io/badge/SBOM-CycloneDX%20%7C%20SPDX-667EEA?style=flat-square)
![HIPAA](https://img.shields.io/badge/HIPAA-Ready-1976D2?style=flat-square)

**DevOps & CI/CD**

![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-CI%2FCD-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

---

## 🔑 Key Differentiators

| | |
|---|---|
| **🏥 Clinical Domain Depth** | 18 years in patient monitoring — alarm fatigue, ICU workflow, field trials. |
| **🤖 AI-Augmented Leadership** | Managed GitHub Copilot as an engineering squad — directing rapid prototyping without sacrificing architectural rigour. |
| **🛡️ Compliance as Architecture** | SBOM, IEC 62304 lifecycle, FDA cybersecurity guidance |
| **🔭 Full-Stack Authority** | Bare metal → Yocto OS → C++ middleware → Qt6 UI → Edge AI → HIPAA cloud — can speak to every layer. |
| **📐 Product Thinking** | Every repo has a PRD, ADRs, and acceptance criteria tied to clinical outcomes. Engineering decisions are product decisions. |

---

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=chaithubk&theme=tokyonight" alt="GitHub Profile Summary" />
</p>
<p align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=chaithubk&theme=tokyonight" alt="Top Languages by Repo" />
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=chaithubk&theme=tokyonight" alt="Top Languages by Commit" />
</p>
<p align="center">
  <img src="https://streak-stats.demolab.com?user=chaithubk&theme=tokyonight&hide_border=true&ring=667EEA&fire=764BA2&currStreakLabel=667EEA" alt="GitHub Streak" />
</p>

---

## 🌱 What I'm Building Next

- 📋 **Architecture Decision Records (ADRs)** — documenting the "why" behind every platform decision across all repos
- 🧪 **Clinical AI Validation** — running edge analytics against MIMIC-III dataset, benchmarking against NEWS2 baseline
- 🔐 **CVE Tracking** — mapping SBOM dependencies to CVEs, documenting remediation trail
- 🌐 **FHIR Integration** — activating telemetry-cloud with HL7 FHIR R4 Observation resources
- ✍️ **Thought Leadership** — LinkedIn articles on edge-vs-cloud trade-offs and compliance-as-architecture

---

## 📫 Let's Connect

💬 I love talking about **Patient Safety · MedTech Architecture · Clinical AI · Regulatory Strategy · Technical Product Management**

<p align="center">
  <a href="https://www.linkedin.com/in/krishnachaithanyab/">
    <img src="https://img.shields.io/badge/Connect%20on%20LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="mailto:chaithanya.balakavi@gmail.com">
    <img src="https://img.shields.io/badge/Send%20an%20Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
</p>

> _"I am not learning TPM. I am already practising it."_

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=chaithubk&color=667EEA&style=flat-square&label=Profile+Views" alt="Profile Views" />
</p>