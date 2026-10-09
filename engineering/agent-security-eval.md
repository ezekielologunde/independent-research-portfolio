# Agent security and prompt-injection evaluation

Status: design scaffold. Start as an evaluation component for the SOC agent; extract a separate package when reusable.

## Vertical slice

Provide a sandboxed agent with mock retrieval, ticketing and file tools. Inject controlled adversarial instructions into synthetic alerts or retrieved documents. Use canary values rather than real secrets. The runner records attempted tool calls, policy decisions, actual sandbox effects and whether the legitimate task was completed. No external targets, real accounts or production credentials are needed.

Proposed scaffold: `src/runner`, `src/adapters`, `src/mock_tools`, `cases`, `policies`, `eval`, `reports`, `tests`. Each case specifies a benign task, untrusted surface, intended boundary, deterministic success oracle and expected legitimate behavior. Do not use an LLM judge as the sole oracle for tool side effects.

## Evaluation plan

Review existing public benchmarks and their licenses before designing a purported new benchmark. Reuse established cases where appropriate and label adaptations. Test unprotected, simple input-boundary and tool-authorization baselines on the same tasks and budgets. Freeze cases and reserve held-out variations; distinguish public benchmark contamination from unseen evaluation.

Metrics: unauthorized-effect rate, attempted unauthorized calls, legitimate task success, overblocking, abstentions, cost and latency. Report model IDs, versions, sampling parameters, repetitions, case counts, uncertainty and attack-generation budget. Keep model-specific incompatibilities separate from security outcomes. A refusal-only system must not appear best merely because it completes no tasks.

Acceptance: deterministic mock effects and recorded traces; reproducible selected-case run; benign controls; no real outbound side effects; published limitations. Cross-model rankings require comparable tool access and execution budgets. Select model count after access and cost review; five models is not a promised result.

Resume template, not a result: Built a sandboxed agent-security evaluation harness covering [N] cases across [K] models, reporting [unauthorized-effect rate] alongside [legitimate task success] under [specified defenses].
