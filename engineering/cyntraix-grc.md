# Cyntraix policy-to-control copilot

Status: extension design scaffold. Existing local Cyntraix directory found; product capabilities and customers have not been audited.

## Vertical slice

Upload an owner-authorized policy and select a versioned, publicly usable control framework. Produce suggested mappings with exact source passages, page/section references, rationale, uncertainty and missing-evidence flags. A reviewer accepts, edits or rejects each mapping. Preserve source hashes and reviewer decisions. A suggested mapping is not a compliance certification.

Proposed modules: ingestion and page-aware extraction, versioned control catalog, retrieval, structured mapping, citation verification, review UI and export. Use public sample policies for the demo. Check framework reuse terms before bundling its text. Treat document instructions as data rather than tool authority.

## Evaluation plan

Build expert-adjudicated policy/control examples, including partial coverage and no-match cases. Split by source organization/document family so near-duplicate templates do not leak across partitions. Compare keyword retrieval, retrieval-only ranking and model-assisted mapping.

Report mapping precision/recall, citation correctness, unsupported coverage claims, abstentions, reviewer edits, latency and cost. Measure reviewer time directly with comparable cases and a predefined protocol. Evaluate policy-version changes so stale citations and superseded controls are visible.

Acceptance: citations resolve to the exact uploaded version; unsupported mappings are flagged; reviewer decisions are auditable; one complete sample-document workflow and reproducible evaluation. No client deployment, time reduction or compliance result is claimed.

Resume template, not a result: Built a citation-grounded GRC copilot for [framework/version], evaluated on [N] adjudicated mappings with [precision/recall] and [citation correctness], supporting human-reviewed exports.
