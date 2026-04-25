# wsk-builds

OpenAI Agents SDK contributor and developer tooling builder.

I focus on upstream maintenance work for [openai/openai-agents-js](https://github.com/openai/openai-agents-js): runtime correctness, streaming behavior, tool/schema compatibility, test reliability, documentation accuracy, and contributor workflow quality.

## Application Snapshot

- `9` merged upstream PRs to [openai/openai-agents-js](https://github.com/openai/openai-agents-js).
- `15` authored upstream PRs total: `9` merged, `1` active, `5` closed after maintainer feedback or scope changes.
- Active validation work on [#1178](https://github.com/openai/openai-agents-js/pull/1178): preserving streaming usage after `AbortSignal` cancellation.
- Supporting tooling: [agents-pr-tools](https://github.com/wsk-builds/agents-pr-tools), a zero-dependency CLI for reproducible GitHub PR reporting.
- Evidence archive: [upstream-contributions](https://github.com/wsk-builds/upstream-contributions).
- Current upstream scale: [openai/openai-agents-js](https://github.com/openai/openai-agents-js) has `2,833` stars and `708` forks as of April 25, 2026.

## Why This Matters for OpenAI

My public work is concentrated where SDK reliability matters to developers building with OpenAI:

- Runtime compatibility: preserving behavior across schema changes, tool input shapes, and package boundaries.
- Streaming correctness: validating cancellation, retries, usage accounting, and partial-stream state.
- Test reliability: adding regression coverage and stabilizing harness behavior before changes merge.
- Documentation accuracy: keeping examples and install paths aligned with actual package behavior.
- Contributor workflow quality: making local validation and reporting easier to reproduce.

## Recent Upstream Impact

| Area | Evidence | Impact |
| --- | --- | --- |
| Runtime compatibility | [#1172](https://github.com/openai/openai-agents-js/pull/1172), [#1171](https://github.com/openai/openai-agents-js/pull/1171), [#1170](https://github.com/openai/openai-agents-js/pull/1170) | Restored discriminated union tool schemas, preserved nested audio config, and failed fast on unsupported SIP VAD fields. |
| Reliability and tests | [#1169](https://github.com/openai/openai-agents-js/pull/1169), [#1162](https://github.com/openai/openai-agents-js/pull/1162) | Stabilized leak detection and added AI SDK UI boundary coverage. |
| Docs and workflow | [#1166](https://github.com/openai/openai-agents-js/pull/1166), [#1165](https://github.com/openai/openai-agents-js/pull/1165), [#1160](https://github.com/openai/openai-agents-js/pull/1160), [#1158](https://github.com/openai/openai-agents-js/pull/1158) | Fixed contributor tooling, corrected example paths, synced AI SDK docs/examples, and repaired docs commands. |

## Current Focus

[#1178](https://github.com/openai/openai-agents-js/pull/1178) is an active runtime-validation thread for preserving streaming usage after `AbortSignal` cancellation. The public thread includes:

- retry-adjusted usage accounting follow-up in `packages/agents-core/src/usage.ts`
- regression coverage for retry plus early-abort streaming behavior
- runtime-behavior-probe analysis comparing `main` against the candidate branch
- ready-to-run live probe instructions for maintainers with `OPENAI_API_KEY`
- follow-up for multi-entry usage detail replacement

## What 6 Months of Pro/Codex Would Unlock

If selected for OpenAI's developer Pro access, I would apply it directly to public OpenAI ecosystem work:

- Expand runtime regression coverage for streaming, retries, aborts, and usage accounting in `openai/openai-agents-js`.
- Use larger-context Codex sessions for focused issue reproduction, failing test minimization, and review-ready patches.
- Run deeper documentation and examples drift audits across Agents SDK packages.
- Improve `agents-pr-tools` into a stronger reporting layer for upstream contribution summaries, release notes, and maintainer-facing evidence.
- Convert review feedback into faster validation loops: probe design, scenario matrices, and concise maintainer handoff notes.

## Key Verification Links

- [Merged upstream PRs](https://github.com/openai/openai-agents-js/pulls?q=is%3Apr+author%3Awsk-builds+is%3Amerged)
- [Active upstream PRs](https://github.com/openai/openai-agents-js/pulls?q=is%3Apr+author%3Awsk-builds+is%3Aopen)
- [Runtime validation thread #1178](https://github.com/openai/openai-agents-js/pull/1178)
- [Issue-to-fix flow: #1163 -> #1171](https://github.com/openai/openai-agents-js/issues/1163)
- [Evidence archive](https://github.com/wsk-builds/upstream-contributions)
- [Contribution reporting tool](https://github.com/wsk-builds/agents-pr-tools)
