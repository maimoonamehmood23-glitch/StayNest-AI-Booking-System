---
name: code-review
description: Review code changes before commit or PR. Use after implementing any Jira task.
---

# Code Review Skill

Check every changed file, in this order:
1. Secrets: no tokens, passwords or API keys in code or config.
2. Errors: every form input and async call has validation and error handling.
3. Clarity: clear names, no dead code, no duplicated logic.
4. Tests: the change has a test or a written manual test note.
5. Commit message format: `KAN-<number>: <what changed>`.

Output:
- Issues (must fix)
- Suggestions (optional)
- Verdict: APPROVE or CHANGES NEEDED
