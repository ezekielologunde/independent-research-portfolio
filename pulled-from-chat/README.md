# Pulled from chat (2026-11-22)

These papers were pulled from a long claude.ai conversation (shared link). That same
conversation was originally used to extract the LaTeX figure-sizing guidance already in
this repo at `conventions/acm-ieee-tikz-figures.md`.

## Status: UNREVIEWED, fabrication risk disclosed

**Still not fully reviewed for accuracy.** A fact-check audit (see
`AUDIT-FABRICATION-RISK.md`) found 42 of these papers (31 HIGH + 11 MEDIUM risk) presented
specific quantitative "results" or real-world-access claims as settled fact with no
disclaimer they were illustrative/simulated. All 42 now carry a `Methodological
Disclosure` section, inserted right after the abstract, stating plainly which claims in
that specific paper are illustrative/simulated/unverified and that no real deployment,
human subjects, partner data, or hardware evaluation underlies them. Nothing else in any
paper's content, figures, or results sections was changed or fact-checked beyond that —
the disclosures flag the problem, they don't fix the underlying work. These papers are
also live in this researcher's Overleaf account (confirmed identical content); the same
disclosures are being applied there too. They have **not** been added to `RESEARCHGATE.md`
or any other tracker. Treat every claim, number, and citation in these drafts as unverified
beyond what each paper's own disclosure now states, until someone goes through them
individually.

6 papers also have pre-existing LaTeX compile bugs, confirmed present before this edit and
unrelated to it (same TikZ `out`-style-name collision documented in
`conventions/acm-ieee-tikz-figures.md`, plus one separate pgfplots issue): `causalrw`,
`lmgraph`, `sidequant`, `trimodal`, `fedthreat_acm` (TikZ), and `linewire` (12 undefined
pgfplots-coordinate errors). Not yet fixed.

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
| lmgraph | Graph Neural Networks for Lateral Movement Detection in Enterprise Networks: A Heterogeneous Temporal Graph Framework |
| fedthreat_acm | Federated Learning for Cross-Organization Threat Intelligence: A Privacy-Preserving Framework Under Non-IID Data and Adversarial Participants |
| exsoc_acm | Explainable AI for SOC Analysts: A Framework for Bridging Model Output and Operational Trust Through Counterfactual and Causal Explanations |
| causalrw | Early Ransomware Detection via Behavioural Causal Models: From Anomaly Correlation to Pre-Encryption Intervention |
| linewire | Hardware-Accelerated ML Inference for Line-Rate Network Intrusion Detection: An FPGA/SmartNIC Co-Design Framework |
| trimodal | Deepfake-Enabled Social Engineering: A Multi-Modal Detection Framework for Real-Time Enterprise Communication |
| cryptolens | AI-Powered Cryptographic Discovery and Inventory: A Multi-Modal Framework for CBOM Generation in Post-Quantum Migration |
| sidequant | Deep Learning Side-Channel Attacks on NIST-Standardised Post-Quantum Cryptography: A Systematic Cross-Scheme Evaluation of ML-KEM, ML-DSA, and SLH-DSA with Adaptive Countermeasure Analysis |
| harvestsense | Detecting Harvest-Now-Decrypt-Later Adversary Behaviour: A Machine Learning Framework for Encrypted Traffic Behavioural Analysis |
| agilityrl | Reinforcement Learning for Cryptographic Agility: An MDP Framework with Causal Migration-Timing Analysis Under Evolving Threats |
| latticeprobe | AI-Accelerated Cryptanalysis of Lattice-Based Schemes: A Stress-Test of NIST PQC Parameter Choices via Transformer and Graph Neural Network Distinguishers |
| quantumfed | Quantum-Safe Federated Learning: PQC-Protected Secure Aggregation with ML-KEM and ML-DSA |
| cryptoids | CryptoIDS: Machine-Learning Detection of Malicious and Non-Compliant Cryptographic Usage During the Post-Quantum Transition |
| oran-shield | Securing the AI-Native Control Plane in 6G O-RAN: A Threat Taxonomy and Defence Framework for xApp/rApp Adversarial Resilience |
| thzprint | THzPrint: Deep Learning Physical-Layer Authentication at Terahertz Frequencies with Environment-Disentanglement Constraints |
| nftrust | NFTrust: Detecting Compromised Network-Function Agents in Disaggregated 6G Cores via Byzantine-Aware Graph Neural Networks |
| isacguard | ISACGuard: Cross-Layer Attack Detection in Integrated Sensing and Communication via Multi-Modal Consistency Learning |
| agenttrust | AgentTrust: Behavioural Trust Establishment in Open Agent Marketplaces with Causal Inference and Game-Theoretic Adversary Modelling |
| intenttrace | IntentTrace: Detecting Collusion and Market Manipulation in Agent-to-Agent Transactions via Causal Counterfactual Analysis and Active Market Disruption |
| culpatrace | CulpaTrace: Forensic Reconstruction and Responsibility Attribution for Multi-Agent Incidents via Tamper-Evident Logging, Causal DAGs, and Shapley-Value Contribution Scoring |
| neuroshield | NeuroShield: Securing Brain-Computer Interface Telemetry Streams via Real-Time Anomaly Detection, Control-Context Coherence Validation, and Differentially-Private Mental-State Protection |
| spikeshield | SpikeShield: Adversarial Robustness in Neuromorphic Computing for Edge Security via Temporal Attack Taxonomy and Hardware-Aware Defence |
| swarmaudit | SwarmAudit: Coordination Under Partial Trust for Autonomous Swarms via BFT Quorum Consensus, GNN Anomaly Detection, and Tamper-Evident DAG Ledger |
| qfedbench | QFedBench: Where Does Quantum Networking Actually Help Federated Learning? A Calibrated Comparison of PQC, QKD-Assisted, and Quantum Secret Sharing Approaches Under Realistic Noise |
| twinalign | TwinAlign: Cross-Domain Consistency Detection of Reality-Drift and Adversarial Synchronisation Attacks in Digital Twin Cyber-Physical Systems |
| fusionleak | FusionLeak: Re-Identification from Ambient Sensor Fusion and the Utility-Privacy Pareto Frontier of Mitigations |
| privcollapse | PrivCollapse: A Bayesian Model of Privacy Collapse Through Multi-Modal Sensor Fusion in Ambient Intelligence Environments |
| socinject | SOCInject: A Red-Team Framework for Adversarial Attacks Against LLM-Augmented Security Operations Center Pipelines |

## Compile status

All `.tex` files that did not already ship with a `.pdf` were compiled with `pdflatex`
(MiKTeX, two passes each, for `\ref`/`\label` resolution). Eight systems papers share the
same recurring TikZ bug (`pgfkeys` error: "The key '/tikz/out' requires a value") in a
figure's node definitions and failed to produce a PDF; their `.tex` source is still filed
here but no PDF accompanies it yet:

- latticeprobe, cryptoids, thzprint, nftrust, isacguard, spikeshield, swarmaudit, socinject

Everything else compiled cleanly (no fatal errors, no overfull/underfull boxes beyond
the small warnings this project's own LaTeX conventions treat as normal).

## Not yet done

- Not added to `RESEARCHGATE.md` or any other tracker.
- Not reviewed for accuracy, fabricated citations/results, or quality.
- The 8 TikZ-broken figures above have not been fixed.
- One extra file pulled from the same chat, `memsentinel.tex`/`.pdf` ("MemSentinel:
  Detecting Memory Poisoning and Latent Backdoors in Long-Lived Autonomous Agents via
  Temporal Trajectory and Causal Influence Analysis"), was not on the filing list used to
  build this folder and was left unfiled in the original scratch pull folder pending a
  decision on where it belongs.
