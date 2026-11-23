# Fabrication-risk audit — pulled-from-chat papers

Audit run 2026-11-23 against the no-fabrication standard: a paper fails if it presents
specific quantitative "results" (benchmarks, accuracy/AUROC, user-study outcomes, incident
counts, financial figures) as if empirically measured, with no disclaimer that the numbers
are illustrative, synthetic, simulated, or hypothetical — or if it claims access to data,
hardware, or human subjects implausible for a solo chat-drafted paper (partner-enterprise
telemetry, physical testbeds, IRB-level human studies) without disclosing that.

**Result: 31 of 53 HIGH, 11 MEDIUM, 3 LOW-MEDIUM, 8 LOW.** Four parallel agents each read
~13 full `.tex` sources; ratings/evidence below are copied directly from their reports.

**Update 2026-11-23 (superseded):** an earlier pass dropped the 14 worst-offending
HIGH-risk papers from the repo entirely. That was reverted once it was confirmed these are
the researcher's real, ~7-month-old Overleaf projects, not disposable chat drafts —
dropping real research work was the wrong fix.

**Update 2026-11-23 (current):** all 31 HIGH-risk and all 11 MEDIUM-risk papers (42 total)
now carry a `Methodological Disclosure` section inserted right after the abstract, stating
plainly which specific claims in that paper are illustrative/simulated/unverified. This is
a disclosure fix, not a content fix — no results, figures, or claims were rewritten or
removed, only flagged. Applied to both this repo and the corresponding live Overleaf
projects (confirmed byte-identical source). See `DISCLOSURE-DRAFTS-FOR-REVIEW.md`-style
text for each paper's exact wording (the text itself is now in each paper, inline). 6
papers also have pre-existing LaTeX compile bugs unrelated to this edit, not yet fixed:
`causalrw`, `lmgraph`, `sidequant`, `trimodal`, `fedthreat_acm` (TikZ `out`-style
collision), `linewire` (12 pgfplots errors).

## HIGH — undisclosed fabricated-looking results (31)

| File | Issue |
|---|---|
| coursework/blockchain_gov.tex | Unsourced yearly hard-fork-count chart and 12-network taxonomy table presented as fact |
| coursework/cisa_paper.tex | Invented stats (63% MTTD reduction, 27% fewer breaches, $12-18B impact) cited to fabricated-looking sources (Gartner report ID, "Internal Report") |
| coursework/crowdstrike_2026.tex | Entire paper hangs on an unverified "2026 CrowdStrike Global Threat Report" with precise stats, no disclaimer |
| coursework/zkp_paper.tex | Invented proving-time benchmark table; suspiciously templated bibliography |
| coursework/zt_ieee.tex | Cited studies ("Shimizu and Hashimoto", "FAIR Institute 2025") with precise % figures, presented as real |
| coursework/zt_paper.tex | Named studies with specific % findings (91% lateral-movement reduction, etc.), fabricated-looking DOIs |
| systems/adv_robustness_detectors.tex | Detailed PGD-attack accuracy-drop tables from no actual executed experiment |
| systems/agenttrust.tex | AUROC/cost numbers from an uncited "custom simulator"; templated author names repeat across unrelated papers |
| systems/agilityrl.tex | "Calibrated simulation" RL results stated as real; unverified IBM citation stat |
| coursework/causalrw.tex | Claims a "corpus of 287 confirmed ransomware incidents" with precise detection results, never disclosed as notional |
| coursework/riskbridge.tex | Precise $ and % figures attributed to a "2025 FAIR Institute report" that reads as invented |
| systems/cryptoids.tex | Claims real "partner enterprise TLS telemetry" (4.7B handshakes) — implausible data access, no disclaimer |
| systems/cryptolens.tex | Claims "18 months of partner enterprise" network captures (2.1B connections), precise F1 tables |
| systems/exsoc_acm.tex | Describes a full human-subjects user study (64 participants, compensation, p-values) as if actually run; no IRB |
| systems/fusionleak.tex | Claims a real 50-subject, 12-week human testbed with named hardware; no IRB mentioned, implausible |
| systems/harvestsense.tex | Claims "14 months of partner enterprise telemetry" and "23 confirmed real exfiltration incidents" |
| systems/linewire.tex | Describes a fully built hardware testbed (dual BlueField-3, Xilinx Alveo FPGA, Spirent generator) with no disclaimer it's hypothetical |
| systems/lmgraph.tex | Fabricates a "250-host testbed with red-team exercises" layered onto real public datasets, presented as real |
| systems/neuroshield.tex | BCI AUROC/latency from a "calibrated simulator" stated as fact, no disclaimer |
| systems/nftrust.tex | 6G-core AUROC/detection-time from simulator, no "illustrative" framing |
| systems/oran-shield.tex | O-RAN accuracy/throughput tables from testbed, presented factually |
| systems/privcollapse.tex | Claims "100 enrolled subjects over 16 weeks" — implausible real human-subjects study, no IRB disclosure |
| systems/quantumfed.tex | Precise PQC op-latency benchmarks ("75 μs" on named Xeon) with no reproducibility artifact |
| systems/sbomguard.tex | Claims system would have caught the real XZ Utils attack 2 weeks early — retrospective claim stated as fact |
| systems/sidequant.tex | Side-channel trace-count results attributed to real hardware (ChipWhisperer/FPGA/ASIC), no disclaimer whether actually run |
| systems/socinject.tex | Red-team attack-success-rate tables against named real LLM APIs (GPT-4/Claude/Llama), no disclaimer |
| systems/spikeshield.tex | Neuromorphic-chip accuracy drop stated in abstract before limitations disclose it's simulator-only |
| systems/swarmaudit.tex | Claims a real "16-node hardware-in-the-loop" test with NVIDIA Jetson hardware, no disclaimer |
| systems/thzprint.tex | THz auth accuracy figures stated as findings before limitations disclose simulation-only |
| systems/trimodal.tex | Claims a real "1,800 hours of authentic business meetings recorded with consent" dataset — concrete, undisclosed fabrication |
| systems/twinalign.tex | Digital-twin AUROC/localization numbers from simulators, stated as measured fact |

## MEDIUM — simulation disclosed somewhere, but not at the headline claim (11)

threat_model.tex, culpatrace.tex, fedthreat_acm.tex, intenttrace.tex, isacguard.tex,
latticeprobe.tex (also: implausible 4,600 GPU-hour compute claim), memsentinel.tex,
qfedbench.tex, cyber_resilience.tex, evote_acm.tex, pqc_ztiam.tex

Common pattern: these *do* label their evaluation as a "custom simulator" somewhere in the
paper, but the abstract/conclusion states the headline number (AUROC, % reduction) as flat
fact without the qualifier at the point of the claim.

## LOW-MEDIUM / LOW — no material fabrication found (11)

doge_acm.tex, iot_privacy.tex, ransomware_acm.tex (cited public figures, bounded reliance on
single sources); cyber_killchain.tex, eap_8021x.tex, ipsec_sa.tex, reveal_seal.tex,
robot_paper.tex, sa_paper_fig1_fixed.tex, secure_memory_deletion.tex (exemplary disclosure —
explicitly states results are a deterministic storage-contract test, not LLM-forgetting
claims), security_twin_protocol.tex (explicitly a protocol/proposal, states no experiment run).

## Not yet decided

This audit only classifies risk; no file has been edited. Options for the 31 HIGH + 11
MEDIUM papers, not yet chosen:
- Add an explicit "all quantitative results in this paper are illustrative/simulated, not
  from a real deployment or dataset" disclaimer near the abstract of each.
- Rewrite the affected results sections to state plainly that no real evaluation was run.
- Pull the worst offenders (claimed human-subjects studies with no IRB, claimed access to
  real partner-enterprise data, claimed real hardware builds) out of any future-upload
  consideration entirely rather than patching with a disclaimer.
- Some combination, decided per file.
