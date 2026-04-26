**Title:** RupeeSpeak — Emotion-Adaptive Multilingual Voice Agent for Financial Inclusion

**Theme:** Theme 7 — Voice-Based AI for Social Impact

**The Problem**

Over 700 million Indians are eligible for government financial schemes but never enroll because information is trapped behind text-heavy English portals. According to [RBI Financial Inclusion data](https://www.rbi.org.in/Scripts/PublicationsView.aspx?id=21479), 190 million adults remain unbanked. Call centers are expensive and inconsistent. IVR systems follow rigid scripts and are universally abandoned mid-call. No existing voice AI handles the emotional nuance required to build trust with first-time financial users who are intimidated by formal institutions.

**What RupeeSpeak Does**

RupeeSpeak is a browser-based AI voice agent that speaks in the user's *native language*, explains financial products conversationally, detects emotional hesitation or confusion from the user's voice in real-time, and **adapts its tone, pace, and persuasion strategy accordingly**. It qualifies every interaction as Hot/Warm/Cold, cross-references the user against 200+ government welfare schemes, and hands qualified leads to human agents with full conversation context.

**Core Features**

**1. Real-Time Acoustic Emotion Recognition** — Analyzes the user's voice *prosody* — pitch contour, speech rate, pause duration, vocal energy — every 2 seconds. Classifies the user's emotional state: confident, confused, frustrated, interested, or disengaged. The agent immediately adjusts: slows down and simplifies when confusion is detected, accelerates when interest spikes. This operates directly on raw audio, not on text transcripts. [Google Duplex](https://ai.google/discover/duplex/) and [Bland AI](https://www.bland.ai/) handle appointment booking but have zero emotion-adaptive dialogue.

**2. Deep Reinforcement Learning Dialogue Policy** — The agent's conversation strategy is a [DRL policy network](https://arxiv.org/abs/1709.00103) trained to maximize a composite reward: user trust score + information delivery completeness + conversion outcome. The agent autonomously discovers which explanation sequences, analogies, and objection-handling tactics work best for different demographic profiles. Every competitor uses static decision trees — RupeeSpeak adapts every response based on the user's real-time emotional state.

**3. Semantic Episodic Memory** — When a user interrupts with an unrelated question mid-conversation, the agent resolves the tangent completely, then bridges back to the *exact point* in the financial explanation where the interruption occurred. It maintains a vectorized memory of the full conversation arc. No context is ever lost.

**4. 12-Language Zero-Latency Switching** — Speaks in Kannada, Hindi, Tamil, Telugu, Marathi, Bengali, Gujarati, Malayalam, Punjabi, Odia, Assamese, and English. If the user switches language mid-sentence, the agent follows instantly. There is no "press 2 for Hindi" — language detection and adaptation is automatic and continuous. Built on [AI4Bharat's IndicWhisper](https://ai4bharat.iitm.ac.in/) speech models.

**5. Welfare Scheme Eligibility Engine** — Cross-references the user's demographic data (age, income bracket, location, occupation) against a live database of 200+ central and state schemes from [MyScheme.gov.in](https://www.myscheme.gov.in/). Proactively informs the user of schemes they qualify for but have never applied to. No voice agent combines financial product pitching with proactive welfare scheme discovery.

**Who Benefits**

**Rural and semi-urban population (500M+)** get voice-first access to financial products and welfare schemes. **Financial institutions (banks, NBFCs)** achieve automated, empathetic lead qualification at scale. **Government welfare departments** get a direct enrollment pipeline for underutilized schemes. **SHG (Self Help Group) members** receive conversational guidance on credit, insurance, and savings. **Elderly and low-literacy citizens** gain full financial access without reading or typing.

**Key References**

- [RBI Financial Inclusion Reports](https://www.rbi.org.in/Scripts/PublicationsView.aspx?id=21479)
- [MyScheme.gov.in — Government Scheme Discovery](https://www.myscheme.gov.in/)
- [AI4Bharat — Indian Language AI Models](https://ai4bharat.iitm.ac.in/)
- [Deep RL for Dialogue Systems — Research Paper](https://arxiv.org/abs/1709.00103)
- [PMJDY — Pradhan Mantri Jan Dhan Yojana](https://pmjdy.gov.in/)
