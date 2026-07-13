# Vibe Code Safely

> Your AI coding assistant is fast. Make it accountable without slowing it down.

Vibe Code Safely is a compact operating agreement for AI-assisted development:
understand the work, agree the boundary, make the smallest sufficient change,
and report real evidence.

## Install one file

### Claude Code

```bash
curl -fsSL https://raw.githubusercontent.com/Enesevki/vibe-code-safely/main/CLAUDE.md -o CLAUDE.md
```

### Codex

```bash
curl -fsSL https://raw.githubusercontent.com/Enesevki/vibe-code-safely/main/AGENTS.md -o AGENTS.md
```

Add the matching file to a project. No CLI, package manager, account, or
framework is required.

## Also available as a Codex skill

The reusable skill lives at
[`skills/vibe-code-safely/SKILL.md`](skills/vibe-code-safely/SKILL.md). Install
or copy that folder into your Codex skills directory when you want these rules
available across projects.

## What changes

- The agent surfaces assumptions and asks when ambiguity matters.
- Non-trivial work gets a clear goal, acceptance criteria, non-goals, and
  verification before implementation.
- Scope creep, speculative complexity, and drive-by refactors are resisted.
- Risky changes trigger an explicit pause instead of silent execution.
- Handoffs contain actual verification evidence and visible limitations.

The guideline also requires a short preflight before substantial implementation
and a structured handoff afterwards. Append your project’s stack, test commands,
architecture constraints, and security boundaries to the `Project-specific
rules` section in the same file—no additional framework required.

## Examples

See [EXAMPLES.md](EXAMPLES.md) for examples of turning vague prompts into
bounded, verifiable requests.

## How to know it is working

These guidelines are working when you see:

- Fewer unnecessary lines in diffs: requested changes, not drive-by cleanup.
- Clarifying questions and a preflight before substantial implementation.
- Smaller rewrites because the first solution matches explicit success criteria.
- Real commands, test output, and unverified limits in handoffs—not just
  “it works”.
- Explicit pauses before risky or scope-expanding work.

## License

MIT
