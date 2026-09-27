---
name: pull-ticket
description: Pull a GitLab ticket into your queue — view it, assign it to whoever runs the skill, and move it to "doing". Use whenever the user runs `/pull-ticket <number>` or `/pull-ticket <issue-url>`, or says "pull ticket <n>".
---

Automates the recurring "pull a ticket" step on the <redacted> GitLab project: view the issue, assign it to **whoever runs the skill**, and move it to the board's `doing` column. Run from the repository root (or a worktree of it) so `glab` has the repo context.

Given a ticket reference in the arguments — a bare number (`123`), a `#123`, or a GitLab issue / work-item URL (take the trailing number):

1. `glab issue view <number>` — fetch and show the ticket so its title, labels, and acceptance criteria are visible.
2. Resolve the current GitLab user: run `glab api user` and read the `username` field. Do NOT hard-code a username — this is what makes the skill assign to whoever pulled, not to a fixed person.
3. `glab issue update <number> --assignee <username> --label doing` — assign it to that user and move it onto the `doing` column.
4. Confirm back: the ticket is assigned to that user and in `doing`, with a one-line summary of what it is.

Notes:

- Keep each `glab` call a single non-composite command (no `&&`, pipes, or `;`) so it doesn't trip a permission prompt. Run the `glab api user` lookup and the `glab issue update` as two separate commands rather than piping one into the other.
- This skill only **views, assigns, and labels**. It does NOT create a worktree or start the dev cycle — that stays a separate, explicit decision. Offer it as a next step; don't do it automatically.
- If the ticket is already assigned or already in `doing`, the update is a harmless no-op; still report the current state.
- `doing` is an existing project label. If the label or assignee is rejected, surface the error rather than guessing an alternative.
