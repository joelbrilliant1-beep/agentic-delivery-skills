# Skill Roadmap

Additional workflow skills worth extracting from mature agentic delivery teams.

## High-value next skills

### production-promotion-gates

For sandbox-to-production promotion. Covers source commit, build artefact, runtime surface, smoke checks, rollback, logs, and post-promotion proof.

### visible-agent-work

For platforms with hidden background workers. Requires visible run IDs, task records, streamed progress, final artefacts, and parent-thread summaries so users are not gaslit by invisible work.

### model-provider-capability-proof

For model swaps and provider claims. Separates model listing, account entitlement, context window, reasoning modes, tool use, streaming, media support, and actual runtime proof.

### context-continuity-handoff

For long sessions and context compaction. Requires human-readable handoffs, current state, decisions, active blockers, evidence, and what not to repeat.

### design-gate-before-build

For product/UI work. Separates prototype/spec exploration from production implementation, requires approval before build, and handles design changes after signoff.

### dirty-worktree-discipline

For agents working in messy repos. Requires preflight dirty-state inventory, isolated staging, no drive-by cleanup, exact commit surfaces, and unrelated work preservation.

### security-intake-before-import

For importing scripts, tools, MCP servers, skills, or repos. Requires pinning commits, static scans, install-surface audit, secret/network checks, and minimal import.

### qa-to-brief

For turning bug reports, screenshots, and user panic into durable engineering briefs with repro steps, expected behaviour, evidence, severity, owner, and acceptance tests.

### reviewer-fix-mode

A stricter companion to orchestrated delivery. Focuses only on review-then-fix authority boundaries, documented findings, limited diffs, rerun evidence, and final judgement.

## Extraction criteria

Create a skill when the workflow is:

- repeated more than twice;
- easy for agents to mess up;
- useful outside one codebase;
- expressible as role, trigger, steps, pitfalls, and verification;
- better as reusable doctrine than one-off memory.
