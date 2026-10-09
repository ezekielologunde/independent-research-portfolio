# Applied AI portfolio build queue

Planning scaffolds added October 8, 2026. No deployed demo, evaluated model, user adoption or measured improvement is claimed. Repository names below are proposals, not created GitHub repositories. Existing product homes should be reused after checking their architecture and ownership.

| Order | Project | Home / proposed name | First demonstrable outcome |
|---|---|---|---|
| 1 | [AI SOC analyst](ai-soc-analyst.md) | Proposed: ai-soc-triage | Replay an alert, inspect cited evidence, approve or reject a draft |
| 2 | [Agent security evaluation](agent-security-eval.md) | Proposed: agent-security-eval | Run sandboxed injection cases and compare task success with boundary failures |
| 3 | [Rowmio mastery diagnosis](rowmio-mastery.md) | Existing Rowmio project; exact application to confirm | Diagnose a misconception and assess independent transfer |
| 4 | [Cyntraix GRC copilot](cyntraix-grc.md) | Existing Cyntraix project | Produce reviewable policy-to-control mappings with exact citations |

## Two evidence standards

Engineering delivery requires a working system, reproducible setup, justified design, evaluation, and honest limitations. Research originality is a separate claim requiring the standing literature-first contribution gate. Engineering work need not manufacture novelty to demonstrate competence. A topic can be replaced when the evidence or intended user need does not justify it.

Each eventual project release needs a quick demo, architecture diagram, one-command local setup with synthetic defaults, versioned evaluation inputs, baseline comparison, failure analysis and a reproducible results table. Public demos must not expose customer, student or homelab secrets. Mock data and simulation must be visibly labelled. Preserve third-party notices; original work remains unlicensed until the owner chooses otherwise.

## Measurement and release discipline

- Record input provenance, permitted redistribution, labels, split strategy, model/version, prompts, retrieval configuration, code revision, costs and latency.
- Separate development examples from a frozen evaluation set. Do not tune repeatedly on held-out cases or count near-duplicates as independent samples.
- Report denominators, uncertainty, excluded cases, abstentions and failures. Publish negative outcomes too.
- Distinguish replay performance, controlled user evaluation and live usage. Time saved requires timed human comparison, not an estimate from token counts.
- Resume templates become claims only after the corresponding measurement is reproduced. Never turn targets into results.

## Next implementation boundary

Begin with a local, replay-only SOC vertical slice. Real Wazuh/Splunk access, existing alert labels and telemetry suitability have not been verified. Synthetic fixtures are sufficient to develop the interface, but cannot support real-world precision or time-saving claims. Build the security harness initially as a reusable evaluation component for this agent. Extend existing Rowmio and Cyntraix applications rather than creating duplicate products.

Local development is adequate for these initial slices. Consider ASA-X only for approved, compatible batch inference or model training after confirming resources, model licenses and data handling. HPC usage is not itself a portfolio metric.
