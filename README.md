# Agentic Delivery Skills

Reusable skills for builders using agent harnesses, coding agents, and multi-agent software delivery workflows.

These skills capture practical operating patterns for:

- turning vague work into safe, reviewable slices;
- coordinating orchestrators, builders, reviewers, and reviewer-fix passes;
- proving that tests cover production-shaped behaviour, not just hand-built fixtures;
- deploying safely;
- keeping agent work visible;
- validating model/provider claims before swapping production agents.

They are designed to be portable across Claude Code, Codex, Hermes Agent, OpenClaw, Cursor-style agents, custom harnesses, and subagent systems.

## Skills

### Core delivery lane

| Skill | Use when |
|---|---|
| `agentic-engineering` | You need to clarify scope, write a build plan, break work into vertical slices, design interfaces, use TDD tracer bullets, or turn QA into a durable brief. |
| `orchestrated-agentic-delivery` | You are coordinating an orchestrator, builder, reviewer, reviewer-fix pass, and final signoff across one or more agents. |
| `bulletproof-building-and-review` | You need adversarial review or production-bound build signoff where green tests are not enough. |

### Operational guardrails

| Skill | Use when |
|---|---|
| `sandbox-to-production-gates` | You are promoting sandbox/local work to production and need source, build, service, runtime, log, and rollback proof. |
| `visible-agent-work` | Agent or subagent work must be visible, task-local, inspectable, streamed, or tied to run IDs. |
| `model-capability-proof` | You are changing models/providers or validating context, reasoning, tool use, streaming, media support, or fallback behaviour. |
| `context-continuity-handoff` | Long sessions, context compaction, restarts, or agent handoffs need durable state without dragging everything forward. |
| `design-before-build-gate` | UI, UX, API, architecture, or product direction needs signoff before production implementation. |
| `dirty-worktree-discipline` | The repo is messy and you must preserve unrelated work while committing only the intended slice. |
| `security-intake-before-import` | You are importing external repos, scripts, packages, skills, MCP servers, or tools. |
| `qa-to-engineering-brief` | You need to turn screenshots, bug reports, QA notes, or user panic into a builder-ready brief. |
| `reviewer-fix-mode` | A reviewer is allowed to fix issues after documenting findings, without drifting into stealth co-builder mode. |

## Recommended loading patterns

For simple planning:

```text
Load agentic-engineering.
```

For multi-agent delivery:

```text
Load orchestrated-agentic-delivery.
Load bulletproof-building-and-review for review, reviewer-fix, and final signoff.
```

For production promotion:

```text
Load sandbox-to-production-gates.
Load dirty-worktree-discipline if the repo is not clean.
```

For model swaps:

```text
Load model-capability-proof.
```

For visible agent products:

```text
Load visible-agent-work.
Load context-continuity-handoff for long-running work.
```

For strict code review verdicts:

```text
Load bulletproof-building-and-review.
Return PASS, HOLD, or REQUEST CHANGES with evidence.
```

## Installation

Copy any skill directory under `skills/` into your agent's skill directory.

Example:

```bash
cp -R skills/agentic-engineering ~/.your-agent/skills/
```

Each skill is plain Markdown with YAML frontmatter, so you can adapt it for systems that use `.md` rules, custom prompts, slash commands, or skill loaders.

## Design philosophy

- Role separation beats vague collaboration.
- One slice, one primary builder.
- Reviewers can fix, but only in explicit reviewer-fix mode.
- Final signoff belongs to the orchestrator.
- Tests are necessary, not sufficient.
- Production-shaped data beats constructed fixtures.
- If no test catches the regression, severity is at least medium.
- Model listings are not capability proof.
- Invisible agent work is not trustworthy agent work.
- Deployment evidence must prove the live runtime, not just the repo.

## Skill naming updates

Some initial roadmap names were tightened before publication:

| Initial name | Published name |
|---|---|
| `production-promotion-gates` | `sandbox-to-production-gates` |
| `model-provider-capability-proof` | `model-capability-proof` |
| `design-gate-before-build` | `design-before-build-gate` |
| `qa-to-brief` | `qa-to-engineering-brief` |

## Roadmap

See [`docs/ROADMAP.md`](docs/ROADMAP.md) for extraction criteria and future skill ideas.

## Licence

MIT. See [`LICENSE`](LICENSE).
