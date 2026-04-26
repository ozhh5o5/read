**Title:** TenderEval AI — Anti-Cartel Forensic Tender Evaluation for Government Procurement

**Theme:** Theme 3 — AI-Based Tender Evaluation and Eligibility Analysis for Government Procurement (CRPF)

**The Problem**

Government tender evaluation in India is manual, opaque, and vulnerable to fraud. Officers spend weeks reading thousands of scanned pages. Genuine bidders get disqualified for minor formatting issues. Cartels submit coordinated bids through shell companies and win uncontested. According to the [CVC Annual Report](https://cvc.gov.in/), procurement irregularities constitute the largest category of corruption complaints. The [Government e-Marketplace (GeM)](https://gem.gov.in/) automates listing but performs zero AI-based eligibility extraction or forensic cartel detection.

**What TenderEval AI Does**

TenderEval AI ingests the tender document and all bidder submissions — *typed PDFs, scanned affidavits, Word files, photographed certificates* — extracts every eligibility criterion, evaluates each bidder against every criterion, and outputs an **explainable verdict** (Eligible / Not Eligible / Needs Review). Every verdict links directly to the exact page and paragraph in the source document. Simultaneously, a forensic graph engine scans for hidden bid-rigging patterns across historical tenders.

**Core Features**

**1. Multi-Format Document Intelligence** — Processes every document format: machine-typed PDFs, handwritten affidavits via OCR, scanned certificates via [Vision-Language Models](https://arxiv.org/abs/2304.08485), and Word/Excel files natively. Handles stamped, tilted, and low-resolution scans. No document is rejected for format incompatibility. Standard OCR tools like [ABBYY](https://www.abbyy.com/) extract text but do not map extracted data to eligibility criteria or generate per-criterion verdicts.

**2. Per-Criterion Explainable Verdicts with PDF Anchoring** — For every eligibility criterion (turnover threshold, experience years, license validity), the AI produces a verdict with a confidence score. Each verdict hyperlinks to the *exact bounding box* in the original bidder PDF. Officers verify in seconds, not hours. No bidder is silently disqualified. [GeM](https://gem.gov.in/) and manual evaluation provide no explainable, document-anchored verdicts.

**3. Bid-Rigging Detection via Temporal Graph Neural Networks** — Builds a continuously growing knowledge graph of all bidding entities: their registered directors, addresses, IP submission metadata, historical bid amounts, and win/loss patterns. A [Temporal GNN](https://arxiv.org/abs/2006.10637) detects shell company clusters, round-robin bidding rings, and coordinated price inflation across multiple tenders. Outputs a **forensic risk score** for every bidder. No Indian procurement platform builds a temporal graph of bidding entities to detect collusion — a capability that even [CBI](https://cbi.gov.in/) anti-corruption units currently lack in automated form.

**4. Statutory Cross-Compliance Check** — Cross-references bidder claims against live government databases: [GST registration status](https://www.gst.gov.in/), [MSME Udyam registration](https://udyamregistration.gov.in/), blacklisting records on [GeM](https://gem.gov.in/), and labour law compliance. Discrepancies are flagged automatically with the exact conflicting data source cited.

**5. Comparative Bid Analytics Dashboard** — Officers see a side-by-side comparison matrix of all bidders across all criteria — color-coded pass/fail — with drill-down into every supporting document. Replaces the manual paper-shuffling process entirely.

**Who Benefits**

**CRPF and Defense procurement** get tamper-proof, explainable evaluations for every tender. **All central and state procurement bodies** achieve 10x faster evaluation with zero silent disqualifications. **Anti-corruption agencies (CBI, CVC)** get automated cartel and shell company detection. **Genuine MSME bidders** receive fair evaluation regardless of document formatting quality. **RTI applicants and investigative journalists** get a full audit trail for every procurement decision.

**Key References**

- [Central Vigilance Commission — Annual Reports](https://cvc.gov.in/)
- [Government e-Marketplace (GeM)](https://gem.gov.in/)
- [MSME Udyam Registration Portal](https://udyamregistration.gov.in/)
- [GST Taxpayer Search](https://www.gst.gov.in/)
- [Temporal Graph Networks — Research Paper](https://arxiv.org/abs/2006.10637)
- [LLaVA Vision-Language Model — Research Paper](https://arxiv.org/abs/2304.08485)
