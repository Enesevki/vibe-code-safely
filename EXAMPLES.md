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

## Make surgical changes visible

**Weak**

```text
While adding the field, also modernize this component and clean up its styles.
```

**Better**

```text
Add the requested field only. Preserve existing component structure and styling.
If you notice unrelated cleanup opportunities, list them in the handoff instead
of changing them.
```

## Turn validation into a testable goal

**Weak**

```text
Add validation for the invitation form.
```

**Better**

```text
Write focused tests for an invalid email and an expired invitation, then make
them pass. Existing valid-invitation behavior must continue to pass. Do not add
new validation rules beyond those cases.
```

## Use project-specific rules

**Weak**

```text
Update the API endpoint.
```

**Better**

```text
Read the project's instruction file first. Follow its test command and API
conventions. State any conflict between this request and those rules before
editing.
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
