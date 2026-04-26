**Title:** Verdict→Action — Legal Entailment Engine for Court Judgment Compliance

**Theme:** Theme 11 — Court Judgment Action Tracker

**The Problem**

Indian courts issue thousands of judgments annually directing government departments to act — build infrastructure, compensate victims, shut down polluting factories. These orders are buried in dense 50–200 page PDFs written in complex legal prose. Departments miss deadlines, misinterpret obligations, and face contempt of court proceedings. According to [National Judicial Data Grid](https://njdg.ecourts.gov.in/) statistics, lakhs of cases involve pending compliance. There is no system that converts a judgment into a trackable, verifiable action plan or detects when a court order contradicts existing legislation.

**What Verdict→Action Does**

Verdict→Action ingests court judgment PDFs (typed and scanned), extracts every specific obligation, deadline, and responsible party using **Legal-BERT with Chain-of-Thought reasoning**. Every extracted task is hyperlinked to the *exact paragraph* in the original PDF. Before execution, the platform cross-references obligations against existing state laws and departmental SOPs to **flag statutory contradictions**. Officers verify, assign, and track compliance through a structured escalation workflow with real-time contempt risk scoring.

**Core Features**

**1. Legal-BERT + Chain-of-Thought Obligation Extraction** — Indian court orders contain layered, conditional directives (*"if the State fails to comply within 90 days, the Commissioner shall..."*). Uses fine-tuned [Legal-BERT](https://arxiv.org/abs/2010.02559) with explicit Chain-of-Thought prompting. The AI traces its reasoning step-by-step: identifying the condition, trigger, obligated party, and deadline. Every extraction ships with the reasoning chain as an auditable artifact. [Indian Kanoon](https://indiankanoon.org/) and [SCC Online](https://www.scconline.com/) store judgment text but perform zero obligation extraction or compliance tracking.

**2. Statutory Contradiction Detection** — Before a department executes a court-ordered action, the platform cross-references it against a vector database of existing state legislative acts, departmental circulars, and SOPs. If the court order directs an action that contradicts an existing statute (e.g., *"demolish structure X"* vs. heritage protection act), the system flags the *exact conflicting provisions* with citations. No Indian legal-tech platform does this.

**3. Verbatim PDF Anchoring with Bounding Box Links** — Every generated task hyperlinks to the exact bounding box on the exact page of the original scanned judgment PDF. If a secretary disputes an assigned obligation, they click through to the verbatim judicial text that generated it. Zero room for misinterpretation.

**4. Multi-Party Compliance Tracker with Escalation** — Each judgment spawns a compliance project. Every obligation becomes a task card assigned to a specific officer with a hard deadline. Overdue tasks trigger automated escalation: *assigned officer → department secretary → chief secretary → Advocate General's office*. The escalation chain is configurable per department.

**5. Contempt Risk Scoring** — Continuously calculates a real-time **Contempt Risk Score** for every active judgment based on: (a) number of overdue obligations, (b) days past deadline, (c) historical compliance rate of the assigned department. Departments with rising contempt risk scores are surfaced on a priority dashboard for the Chief Secretary's office.

**Who Benefits**

**State law departments and the Advocate General** get automated extraction that eliminates manual reading of thousands of pages. **Department secretaries** receive clear, deadline-bound task assignments from every judgment. **The Chief Secretary's office** gets a real-time contempt risk dashboard across all departments. **High Court and Supreme Court registries** receive structured compliance reporting from the executive branch. **Citizens and PIL petitioners** get verifiable tracking of whether court-ordered relief is executed.

**Key References**

- [National Judicial Data Grid (NJDG)](https://njdg.ecourts.gov.in/)
- [Indian Kanoon — Free Indian Law](https://indiankanoon.org/)
- [SCC Online — Supreme Court Cases](https://www.scconline.com/)
- [Legal-BERT — Research Paper](https://arxiv.org/abs/2010.02559)
- [e-Courts Services Portal](https://ecourts.gov.in/)
