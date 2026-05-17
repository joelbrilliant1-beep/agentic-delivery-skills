# Skill Roadmap

The first public batch now includes the original three skills plus the nine operational guardrail skills that came out of repeated agentic delivery failures.

## Published skill set

### Core delivery

- `agentic-engineering`
- `orchestrated-agentic-delivery`
- `bulletproof-building-and-review`

### Operational guardrails

- `sandbox-to-production-gates`
- `visible-agent-work`
- `model-capability-proof`
- `context-continuity-handoff`
- `design-before-build-gate`
- `dirty-worktree-discipline`
- `security-intake-before-import`
- `qa-to-engineering-brief`
- `reviewer-fix-mode`

## Renames from the scratch roadmap

| Scratch name | Published name | Why |
|---|---|---|
| `production-promotion-gates` | `sandbox-to-production-gates` | Names the actual transition and avoids vague release language. |
| `model-provider-capability-proof` | `model-capability-proof` | Shorter, still covers provider and account proof inside the skill. |
| `design-gate-before-build` | `design-before-build-gate` | Reads like a gate pattern rather than a process fragment. |
| `qa-to-brief` | `qa-to-engineering-brief` | Makes the output concrete and builder-ready. |

## Future extraction ideas

### agent-browser-verification

For product surfaces where tests pass but the browser can still fail. Covers real UI smoke, screenshots, auth state, console errors, network calls, and visual/customer-readiness evidence.

### artifact-promotion-and-downloads

For agent-produced files, reports, screenshots, PDFs, logs, and generated assets. Covers safe roots, file caps, served URLs, markdown path bypass prevention, and attachment UX.

### agent-platform-health

For operating agent gateways and control planes. Covers health endpoints, websocket truth, worker queues, stale state, reconnect loops, and authenticated smokes.

### prompt-to-agent-brief

For turning a user's rough idea into a precise dispatch prompt for a specialist agent, with role, scope, stop conditions, evidence, and output contract.

### live-research-to-decision

For converting web/social/model research into a bounded decision without accepting launch hype, marketing copy, or single-source claims.

## Extraction criteria

Create a skill when the workflow is:

- repeated more than twice;
- easy for agents to mess up;
- useful outside one codebase;
- expressible as role, trigger, steps, pitfalls, and verification;
- better as reusable doctrine than one-off memory.
