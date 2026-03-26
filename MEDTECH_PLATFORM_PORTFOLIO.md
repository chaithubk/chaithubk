## 🏗️ The MedTech Platform Portfolio

> A multi-repository, AI-augmented medical device platform designed to demonstrate
> **product leadership through technical excellence** by systematically de-risking
> feasibility, viability, and value across independently auditable, CI/CD-gated repositories.

### Platform Architecture

<p align="center"><b>MEDTECH PATIENT MONITORING PLATFORM</b></p>

| Stage | Purpose |
|---|---|
| Feasibility Risk | Validate vital-sign ingestion pipelines and representative clinical scenarios |
| Intelligence Risk | Validate edge AI accuracy, performance, and inference latency |
| Value Risk | Validate bedside UX quality and alarm-design effectiveness |
| Viability Risk | Validate deployable OS-level integration on target architecture |
| Scale Risk | Validate cloud aggregation, interoperability, and growth readiness |
| Integration | Converge validated capabilities into a single orchestrated platform |
| Knowledge | Capture reusable guidance, patterns, and decision rationale |

Flow: Feasibility + Intelligence + Value + Viability + Scale -> Integration -> Knowledge.

Repository links and implementation details are listed in the [Repository Map](#-repository-map) below.

### The Integration Milestone

> **`medtech-device-os` integrates the full platform into a single bootable Linux image.**

All four application services run as a systemd-orchestrated chain on QEMU ARM64:

```
mosquitto.service (IPC)
  └── medtech-vitals-publisher.service   (Python · MQTT)
    └── medtech-edge-analytics.service   (Python · TensorFlow Lite · sepsis detection)
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

## 🔑 Key Differentiators

| | |
|---|---|
| 🚀 **18 Years Across the Stack** | Hands-on execution across hardware, OS, applications, and cloud systems. |
| 🤖 **AI-Augmented Solo Delivery** | The platform is being built end-to-end by a single builder using AI coding agents. |
| 🔭 **Evidence Through Execution** | Capabilities are validated by building and operating real, testable systems. |
| 🛡️ **Compliance by Design** | Security, traceability, and standards alignment are integrated from the start. |
| 🎯 **Outcome-Oriented** | Each repository maps to measurable clinical or operational outcomes, not code output alone. |
---

## 🏆 What This Portfolio Proves

Each repository in this portfolio delivers three parallel outputs:

**① Technical Artifact**
Working prototypes with CI/CD quality gates, test coverage, linting enforcement,
and Docker-based reproducible builds.

**② Product Artifact**
Product Requirements Documents (PRDs aligned to the Cagan INSPIRED framework),
Architecture Decision Records (ADRs), and acceptance criteria tied to
clinical outcomes, not only technical specifications.

**③ Regulatory Artifact**
Compliance annotations, CycloneDX and SPDX SBOM generation, IEC/FDA
standard references in documentation, and audit-trail-ready CI pipelines.

> In MedTech, engineering, product, and compliance are not separate conversations.
> This portfolio treats them as one.

---

## 🌱 What I'm Building Next

- 📋 **Architecture Decision Records (ADRs)** — documenting the decision rationale behind platform choices across repositories
- 🧪 **Clinical AI Validation** — validating edge analytics on Synthea-generated synthetic patient data, benchmarked against NEWS2
  - *Planned extension: benchmark against MIMIC-III for stronger real-world grounding*
- 🔐 **CVE Tracking** — mapping SBOM dependencies to CVEs and maintaining a remediation trace
- 🌐 **FHIR Integration** — activating telemetry-cloud support for HL7 FHIR R4 Observation resources
