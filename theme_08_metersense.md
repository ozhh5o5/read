**Title:** MeterSense AI — Federated Theft Detection & Autonomous Grid Topology Correction

**Theme:** Theme 8 — AI for Smart Meter Intelligence & Loss Detection (BESCOM)

**The Problem**

[BESCOM](https://bescom.karnataka.gov.in/) loses over ₹2,000 crore annually to Aggregate Technical & Commercial (AT&C) losses — a combination of power theft, meter tampering, billing errors, and outdated grid maps. According to [UDAY Dashboard data](https://www.uday.gov.in/), Karnataka's AT&C losses hover around 17%. Current detection relies on periodic physical inspections. Grid topology records (which meter connects to which transformer phase) are decades out of date, making loss localization impossible. Centralizing raw consumption data for ML analysis also raises serious consumer privacy concerns under India's [Digital Personal Data Protection Act](https://www.meity.gov.in/data-protection-framework).

**What MeterSense AI Does**

MeterSense AI is an operational intelligence platform that ingests high-frequency smart meter data, detects theft and anomalies using **AI models trained at the edge via Federated Learning** (never transmitting raw consumption data), algorithmically *reverse-engineers the physical grid topology* from electrical signal correlations, and provides investigators with explainable, evidence-backed case files for every flagged consumer.

**Core Features**

**1. Federated Learning for Privacy-Preserving Theft Detection** — Anomaly detection neural networks are trained *directly on smart meters and local data concentrators*. Only mathematical model weight updates are sent to the central server — never raw consumption data. Consumer privacy is architecturally guaranteed, not policy-promised. Compliant with [DPDP Act 2023](https://www.meity.gov.in/data-protection-framework) by design. [Itron](https://www.itron.com/) and [Landis+Gyr](https://www.landisgyr.com/) use centralized ML that transmits all raw consumption data to cloud servers.

**2. Algorithmic Grid Topology Inference** — BESCOM's GIS maps show which meter connects to which transformer. These maps are wrong for 15–30% of connections. MeterSense analyzes [voltage fluctuation correlations and phase-angle signatures](https://ieeexplore.ieee.org/document/8587547) across thousands of meters simultaneously. Meters that share identical micro-disturbances are on the same feeder. The system outputs a corrected topology map with confidence scores, replacing years of manual line-walking surveys. No Indian DISCOM platform or global competitor performs this.

**3. Seven-Type Anomaly Taxonomy with Explainable Evidence** — Does not output a generic "anomaly detected" alert. Classifies each anomaly into one of seven specific types: *meter bypass, meter slowdown, direct hooking, billing mismatch, transformer overload, phase imbalance, data communication failure*. Each classification ships with a time-series chart highlighting the exact anomalous pattern and a plain-English investigator brief.

**4. Spatio-Temporal Transformer for Sophisticated Tampering** — Experienced power thieves tamper with meters only during specific hours or rotate tampering across multiple connections to stay below threshold alerts. The platform uses [Transformer architectures](https://arxiv.org/abs/1706.03762) that model multi-day, multi-meter temporal patterns to catch these coordinated evasion strategies that rule-based systems miss entirely.

**5. Feeder-Level Reconciliation Dashboard** — Every feeder gets a live reconciliation view: energy supplied (from the transformer meter) vs. energy billed (sum of all consumer meters on that feeder). The gap is the AT&C loss for that specific feeder. Engineers drill down from *feeder → transformer → consumer* to locate exact loss nodes.

**Who Benefits**

**BESCOM and all Indian DISCOMs** recover ₹1,000+ crore annually from targeted theft detection. **Grid planning engineers** get corrected topology maps without costly physical surveys. **State electricity regulators (KERC)** receive verifiable, data-backed AT&C loss reporting. **Consumer privacy advocates** get a federated architecture that guarantees zero raw data centralization. **Field investigation teams** receive pre-built evidence packs for every flagged case.

**Key References**

- [BESCOM — Bangalore Electricity Supply Company](https://bescom.karnataka.gov.in/)
- [UDAY Dashboard — DISCOM Performance](https://www.uday.gov.in/)
- [Digital Personal Data Protection Act 2023](https://www.meity.gov.in/data-protection-framework)
- [Smart Meter Topology Identification — IEEE Paper](https://ieeexplore.ieee.org/document/8587547)
- [Attention Is All You Need — Transformer Architecture](https://arxiv.org/abs/1706.03762)
- [Federated Learning — Google AI Blog](https://ai.googleblog.com/2017/04/federated-learning-collaborative.html)
