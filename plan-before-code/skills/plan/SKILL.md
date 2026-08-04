---
description: Use before implementing any nontrivial feature or code change — writes the work up as epics and stories in a local plan file and confirms scope with the user before any code is written. Skip for small, unambiguous fixes (typos, one-line bug fixes, config tweaks).
---

# Plan before you code

Before implementing a nontrivial feature or change, write it up as one or
more epics with stories in a local plan file, then get the user's
confirmation before writing any code.

## Where the plan lives

- Store plan docs in a `.plan/` folder at the repo root. Check whether one
  already exists before creating a new plan doc — reuse and extend it
  rather than starting fresh elsewhere.
- If `.plan/` isn't gitignored yet, add it to `.gitignore` first. These are
  working documents, not something to commit to shared history.

## Epic format

Each epic in the plan doc should have:

- **Goal** — what this epic accomplishes and why
- **Status** — `[ ]` Not started · `[~]` In progress · `[x]` Done
- **Stories** — specific enough to implement from directly: name the actual
  files, functions, routes, or components involved, not just a vague
  description
- **Testing** — what will be verified, and how (unit vs. integration,
  specific scenarios)
- **Demo** — a concrete way to see the finished feature working

## Process

1. Draft the epic(s) and stories, and present them to the user before
   writing any code.
2. Confirm scope and any non-obvious design decisions — especially
   anything with more than one reasonable approach. Don't guess silently
   on a real design fork; ask.
3. Only after confirmation, implement.
4. Once implemented: mark the epic/stories done, and add an
   "Implementation notes" section documenting any deviations or judgment
   calls made along the way — this is for future reference (by a human or
   another agent picking this up later), not a changelog of what changed.

## When to skip this

Small, unambiguous fixes — typos, one-line bug fixes, config tweaks —
don't need this. Planning overhead should be proportional to the size and
ambiguity of the change.
