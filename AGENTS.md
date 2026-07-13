# Vibe Code Safely

> Build quickly without losing control of scope, understanding, or evidence.

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

Project owners: add the stack, test commands, architecture constraints, security
boundaries, and delivery rules for this repository below this line.

<!-- Add project-specific rules here. -->
