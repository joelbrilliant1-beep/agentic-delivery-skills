# Agentic Delivery Skills

Reusable skills for builders using agent harnesses, coding agents, and multi-agent software delivery workflows.

These skills capture practical operating patterns for:

- turning vague work into safe, reviewable slices;
- coordinating orchestrators, builders, reviewers, and reviewer-fix passes;
- proving that tests cover production-shaped behaviour, not just hand-built fixtures.

They are designed to be portable across Claude Code, Codex, Hermes Agent, OpenClaw, Cursor-style agents, custom harnesses, and subagent systems.

## Skills

| Skill | Use when |
|---|---|
| `agentic-engineering` | You need to clarify scope, write a build plan, break work into vertical slices, design interfaces, use TDD tracer bullets, or turn QA into a durable brief. |
| `orchestrated-agentic-delivery` | You are coordinating an orchestrator, builder, reviewer, reviewer-fix pass, and final signoff across one or more agents. |
| `bulletproof-building-and-review` | You need adversarial review or production-bound build signoff where green tests are not enough. |

## Recommended loading pattern

For simple planning:

```text
Load agentic-engineering.
```

For multi-agent delivery:

```text
Load orchestrated-agentic-delivery.
Load bulletproof-building-and-review for review, reviewer-fix, and final signoff.
```

For a strict code review verdict:

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

## Roadmap

See [`docs/ROADMAP.md`](docs/ROADMAP.md) for other workflow skills worth extracting.

## Licence

MIT. See [`LICENSE`](LICENSE).
