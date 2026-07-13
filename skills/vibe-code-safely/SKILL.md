---
name: vibe-code-safely
description: Keep AI-assisted coding scoped, simple, and evidence-based. Use when planning, implementing, reviewing, or refactoring code, especially when requirements are ambiguous, changes may expand in scope, or verification needs to be explicit.
---

# Vibe Code Safely

Follow this operating agreement for substantive coding work.

## Understand before changing

- Inspect relevant code, conventions, and constraints before proposing a change.
- Read existing project instruction files and relevant tests before editing code.
- State the goal, assumptions, and material tradeoffs. Ask when ambiguity could
  change scope, architecture, or safety.
- Surface conflicting constraints instead of silently choosing one.
- For multi-step work, give a short plan and state how each step will be checked.

## Agree the boundary

Before non-trivial implementation, make the goal, acceptance criteria,
non-goals, and verification explicit. Keep changes inside that boundary; pause
and propose a separate task when the request grows.

For trivial, reversible work, use judgment: state the goal and a direct check
without creating unnecessary process overhead.

For other implementation work, provide this preflight before editing:

```text
Goal:
Assumptions / open questions:
Plan:
Verification:
```

Treat auth, payments, secrets, personal data, production infrastructure,
destructive operations, and irreversible migrations as escalation triggers.
Explain the risk and seek explicit direction before proceeding.

## Prefer the smallest sufficient change

- Use the least code and fewest moving parts that solve the requested problem.
- Do not add speculative features, abstractions, configuration, dependencies,
  error handling for impossible scenarios, or unrelated cleanup.
- Match existing conventions unless a change is part of the request.
- Ensure every changed line traces directly to the approved goal.

## Verify honestly

- Run focused tests or reproducible checks that prove acceptance criteria.
- Report only checks actually performed and their real result.
- Do not turn a passing test into a claim of security, correctness, production
  readiness, or completeness without supporting evidence.
- State what could not be verified and the resulting risk.

## Hand off clearly

End substantive work with this format:

```text
Changes:
Evidence:
Limitations:
Next bounded action:
```

## Project-specific rules

Read and follow the target repository's instruction files, including any
project-specific rules appended to its `AGENTS.md` or `CLAUDE.md`. Surface a
conflict instead of silently choosing between general and project rules.
