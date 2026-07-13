# Examples

## Turn a vague feature into a bounded task

**Weak**

```text
Add authentication.
```

**Better**

```text
Add email/password login. Success means an incorrect password is rejected and
the existing session flow still passes its tests. OAuth and password reset are
out of scope. Explain any assumption before coding.
```

## Fix a bug without drive-by refactoring

**Weak**

```text
Clean up the checkout code while fixing the total bug.
```

**Better**

```text
Reproduce the rounding bug with a focused test, then fix it with the smallest
change. Do not refactor checkout code unless the fix requires it. Report the
test result and any unrelated issue you notice.
```

## Escalate a risky change

**Weak**

```text
Move production secrets to the new provider.
```

**Better**

```text
Before changing anything, identify secret handling, rollback, and production
impact. Propose a plan and verification steps. Wait for explicit approval before
performing an irreversible or production-affecting action.
```
