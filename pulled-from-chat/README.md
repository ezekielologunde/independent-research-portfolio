# Pulled from chat (2026-11-22)

These papers were pulled from a long claude.ai conversation (shared link). That same
conversation was originally used to extract the LaTeX figure-sizing guidance already in
this repo at `conventions/acm-ieee-tikz-figures.md`.

## Status: UNREVIEWED

**Nothing in this folder has been reviewed.** No one has checked these papers for
factual accuracy, fabricated results/citations, methodological soundness, or general
quality. They have **not** been added to `RESEARCHGATE.md` or any other tracker. None of
this has been checked against the no-fabrication standard this researcher holds his real
(published/in-progress) work to. Treat every claim, number, and citation in these drafts
as unverified until someone goes through them individually.

## Deliberately dropped (fabrication-risk audit, 2026-11-23)

A fact-check audit (see `AUDIT-FABRICATION-RISK.md`) found 14 of the systems papers claimed
real-world access that is implausible for a solo chat-drafted paper — real human-subjects
studies with no IRB, real partner-enterprise datasets, or real hardware builds/testbeds —
with no disclaimer that any of it was hypothetical. These were removed outright rather than
patched with a disclaimer, since the claimed access itself (not just the numbers) was the
problem:

- `causalrw` — claimed a real corpus of "287 confirmed ransomware incidents"
- `cryptoids` — claimed real "partner enterprise TLS telemetry" (4.7B handshakes)
- `cryptolens` — claimed real "partner enterprise" network captures (2.1B connections)
- `exsoc_acm` — described a real 64-participant human-subjects user study, no IRB
- `fusionleak` — claimed a real 50-subject, 12-week human-subjects testbed, no IRB
- `harvestsense` — claimed real partner-enterprise telemetry and "23 confirmed real exfiltration incidents"
- `linewire` — described a fully built real hardware testbed (BlueField-3, Xilinx Alveo FPGA)
- `lmgraph` — fabricated a "250-host enterprise testbed with red-team exercises"
- `oran-shield` — claimed a real O-RAN hardware testbed (Colosseum/OAI) with measured results
- `privcollapse` — claimed a real 100-subject, 16-week human-subjects study, no IRB
- `sidequant` — claimed real side-channel measurements on real hardware (ChipWhisperer/FPGA/ASIC)
- `socinject` — claimed real red-team attacks run against live commercial LLM APIs
- `swarmaudit` — claimed a real 16-node hardware-in-the-loop test (NVIDIA Jetson)
- `trimodal` — claimed a real "1,800 hours of authentic business meetings recorded with consent" dataset

These are gone from the repo entirely (both `.tex` and `.pdf`), not just untracked —
removed in a reversible git commit, not deleted from disk-history.

## Deliberately excluded (duplicates of existing work)

Two papers pulled from the same chat were found to duplicate content already in this
researcher's body of work and were **not** filed here (they remain, untouched, in the
original pull staging folder):

- `ai_agent_decommissioning.tex` — exact source of RG-015, an already-published
  ResearchGate preprint ("Security Verification of AI Agent Decommissioning: An
  AgentTrap-Informed Local Microbenchmark").
- `remediation_case_study.tex` — matches existing content in
  `Research/digital-twin-remediation/` ("When Successful Checks Outlive Their Evidence:
  A Reproducible Case Study of Remediation Approval in Microservices").

## Coursework (assignment/coursework-style conversions)

| File | Title |
|---|---|
| cyber_killchain | Aligning Threat Actor TTPs to the Cyber Kill Chain: Anticipating Future Cyber Threats with the MITRE ATT&CK Framework |
| pqc_ztiam | Post-Quantum Cryptography, Decentralised Identity, and Modern Zero Trust IAM: Standards, Compliance, Attacker Adaptation, and Resilience |
| blockchain_gov | Governance Models and Hard Forks in Decentralized Blockchains: A Comparative Analysis of On-Chain and Off-Chain Coordination Mechanisms |
| cyber_resilience | Compensating Controls and Architecting for Cyber Resilience: Bridging the Gap Between Compliance Requirements and Operational Reality |
| threat_model | Threat Modeling Nation-State Attacks on Defense Contractors: A DREAD-Based Risk Assessment Framework for Controlled Unclassified Information Protection |
| iot_privacy | Beyond Personal Data: Redefining Privacy in the Era of IoT, Operational Technology, and Infrastructure-Level Data Protection |
| zt_paper | Zero Trust Architecture in Practice: Security Fatigue, Software-Defined Perimeters, and the Ethics of Vendor Compliance Claims |
| zkp_paper | Analyzing the Role of Zero-Knowledge Proofs in Trust and Security for Verifiable Computation Systems: From Theory to Practice |
| sa_paper_fig1_fixed | Software Assurance Beyond Secure Coding: Lessons from the 2024 CrowdStrike Global Outage |
| zt_ieee | Identity-Centric Zero Trust Architecture: A Comprehensive Framework for Modern Enterprise Security Governance |
| robot_paper | Robot Zombie Apocalypse: Security Implications of Wormable Exploits in Autonomous Robotics and IoT Infrastructure |
| riskbridge | Risk Management as a Strategic Bridge: Aligning Cybersecurity Architecture with Business Objectives in Modern Organizations |
| cisa_paper | The CISA 2015 Expiration and the Future of Information Sharing and Analysis Centers: Implications for National Cybersecurity Architecture |
| doge_acm | Government Efficiency vs. Cybersecurity: A CIA Triad Analysis of the DOGE Social Security Data Incident |
| ransomware_acm | Ransomware in the Age of Social Engineering: Attack Vectors, High-Profile Breaches, and a Zero-Trust Defense Framework |
| evote_acm | Cryptographic Protocols for Electronic Voting Systems: A Comprehensive Framework for Secure Democratic Processes |
| ipsec_sa | IPsec Security Associations: Architecture, Lifetime Management, and the Security Benefits of Periodic Rekeying |
| reveal_seal | RevEAL: Methodology, Security Implications, and Defenses for the First Single-Trace Side-Channel Attack on a Homomorphic Encryption Library |
| crowdstrike_2026 | AI as Weapon, Target, and Arbiter: A Structured Analysis of the CrowdStrike 2026 Global Threat Report |
| eap_8021x | From Wire to Air: Security Limitations of EAP in Wireless 802.11 Environments and the Role of Outer Authentication via TLS Tunneling |
| secure_memory_deletion | When Deleted Agent Memories Return: A Controlled Study of Durable Scope Revocation |
| security_twin_protocol | Decision Validity of Security-Twin Remediation: A Research Protocol for Stale Telemetry and Missing Dependencies |

## Systems ("System name:"-style novel-systems papers)

| File | Title |
|---|---|
| sbomguard | SBOMGuard: Supply Chain Attack Detection via Software Bill of Materials Analysis, Dependency Graph Embedding, and Commit-Level NLP Anomaly Detection |
| adv_robustness_detectors | Adversarial Robustness of Cyber Detection Models: A Systematic Cross-Domain Evaluation and Unified Defense Framework |
| fedthreat_acm | Federated Learning for Cross-Organization Threat Intelligence: A Privacy-Preserving Framework Under Non-IID Data and Adversarial Participants |
| agilityrl | Reinforcement Learning for Cryptographic Agility: An MDP Framework with Causal Migration-Timing Analysis Under Evolving Threats |
| latticeprobe | AI-Accelerated Cryptanalysis of Lattice-Based Schemes: A Stress-Test of NIST PQC Parameter Choices via Transformer and Graph Neural Network Distinguishers |
| quantumfed | Quantum-Safe Federated Learning: PQC-Protected Secure Aggregation with ML-KEM and ML-DSA |
| thzprint | THzPrint: Deep Learning Physical-Layer Authentication at Terahertz Frequencies with Environment-Disentanglement Constraints |
| nftrust | NFTrust: Detecting Compromised Network-Function Agents in Disaggregated 6G Cores via Byzantine-Aware Graph Neural Networks |
| isacguard | ISACGuard: Cross-Layer Attack Detection in Integrated Sensing and Communication via Multi-Modal Consistency Learning |
| agenttrust | AgentTrust: Behavioural Trust Establishment in Open Agent Marketplaces with Causal Inference and Game-Theoretic Adversary Modelling |
| intenttrace | IntentTrace: Detecting Collusion and Market Manipulation in Agent-to-Agent Transactions via Causal Counterfactual Analysis and Active Market Disruption |
| culpatrace | CulpaTrace: Forensic Reconstruction and Responsibility Attribution for Multi-Agent Incidents via Tamper-Evident Logging, Causal DAGs, and Shapley-Value Contribution Scoring |
| neuroshield | NeuroShield: Securing Brain-Computer Interface Telemetry Streams via Real-Time Anomaly Detection, Control-Context Coherence Validation, and Differentially-Private Mental-State Protection |
| spikeshield | SpikeShield: Adversarial Robustness in Neuromorphic Computing for Edge Security via Temporal Attack Taxonomy and Hardware-Aware Defence |
| qfedbench | QFedBench: Where Does Quantum Networking Actually Help Federated Learning? A Calibrated Comparison of PQC, QKD-Assisted, and Quantum Secret Sharing Approaches Under Realistic Noise |
| twinalign | TwinAlign: Cross-Domain Consistency Detection of Reality-Drift and Adversarial Synchronisation Attacks in Digital Twin Cyber-Physical Systems |

14 papers that were in this table have been dropped — see "Deliberately dropped" above.

## Compile status

All `.tex` files that did not already ship with a `.pdf` were compiled with `pdflatex`
(MiKTeX, two passes each, for `\ref`/`\label` resolution). Eight systems papers shared the
same recurring TikZ bug (`pgfkeys` error: "The key '/tikz/out' requires a value") in a
figure's node definitions; the style name was renamed and all eight recompiled clean
(`cryptoids`, `swarmaudit`, and `socinject` were later dropped entirely — see "Deliberately
dropped" above — so only `latticeprobe`, `thzprint`, `nftrust`, `isacguard`, `spikeshield`
remain from that original list of 8).

Everything else compiled cleanly (no fatal errors, no overfull/underfull boxes beyond
the small warnings this project's own LaTeX conventions treat as normal).

## Not yet done

- Not added to `RESEARCHGATE.md` or any other tracker.
- Fact-check audit done (`AUDIT-FABRICATION-RISK.md`); 14 worst offenders dropped; the
  remaining 11 MEDIUM-risk papers (undisclosed-at-the-headline-claim simulation results)
  still need disclaimers added — not done yet.
- One extra file pulled from the same chat, `memsentinel.tex`/`.pdf` ("MemSentinel:
  Detecting Memory Poisoning and Latent Backdoors in Long-Lived Autonomous Agents via
  Temporal Trajectory and Causal Influence Analysis"), was not on the filing list used to
  build this folder and was left unfiled in the original scratch pull folder pending a
  decision on where it belongs.
