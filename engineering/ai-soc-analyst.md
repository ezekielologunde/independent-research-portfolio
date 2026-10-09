# AI SOC triage agent

Status: design scaffold; first build candidate. No application or dedicated repository created by this brief.

## Vertical slice

Input: a redacted alert JSON fixture. Normalize fields, collect approved enrichment evidence, apply deterministic triage rules, and generate a structured draft containing severity, rationale, evidence references, uncertainties and recommended next checks. Display the raw evidence beside the draft. A reviewer records approve, edit or reject; retain both versions and an audit trail. The initial system has no containment or incident-closing authority.

Proposed architecture: fixture/Wazuh/Splunk adapter -> canonical alert schema -> allowlisted enrichment cache -> rule baseline plus model drafting -> citation/schema validator -> review queue -> versioned audit record. Treat alert text and retrieved documents as untrusted input. Enrichment failures must be visible. No executable instructions from alert content. Sensitive telemetry stays out of public fixtures.

Proposed scaffold: `src/adapters`, `src/triage`, `src/evidence`, `src/review`, `ui`, `fixtures/synthetic`, `eval`, `docs`, `tests`. Select the stack after checking existing reusable services. A model-free replay mode should support demonstrations without API credentials.

## Evaluation plan

Define the triage label and escalation threshold before annotation. Have security-qualified reviewers label redacted alerts, adjudicate disagreements, and retain uncertain cases. Split by incident/source/time to reduce leakage; synthetic fixtures remain a separate test category.

Compare deterministic rules, a simple model baseline and evidence-grounded drafting. Report escalation precision and recall, missed high-severity cases, abstention coverage, evidence correctness, unsupported statements, latency and cost per alert. Report classification and summary quality separately. Measure review time using a randomized or counterbalanced human comparison with comparable alerts; report participant count and uncertainty. Do not claim a causal time reduction from an uncontrolled before/after sample.

Acceptance: reproducible fixture replay; invalid inputs and unavailable enrichment handled; evidence links resolve; approval is enforced server-side; no unintended action from hostile alert text; evaluation includes failures and a simple baseline. Performance targets are to be chosen before collection, not invented here.

Resume template, not a result: Built a SOC triage agent evaluated on [N] independently labelled alerts, with [precision/recall], [abstention rate], and [measured review-time difference] versus [baseline].

Dependencies still unverified: actual telemetry source, access method, redistribution rights, expert labelling capacity and live-demo deployment destination.
