# plan-before-code

A Claude Code skill that plans nontrivial work as epics and stories in a
local plan file, and confirms scope before any code gets written.

## What it does

When invoked, Claude will:

1. Draft one or more epics (Goal / Status / Stories / Testing / Demo) in a
   `.plan/` folder at your repo root, instead of jumping straight into
   code.
2. Confirm scope and any non-obvious design decisions with you before
   implementing.
3. Once the work is done, mark the epic complete and record any deviations
   or judgment calls in an "Implementation notes" section — so the *why*
   behind a decision survives, not just the diff.

Small, unambiguous fixes (typos, one-line bug fixes, config tweaks) are
skipped automatically — this is for real feature work, not every commit.

## Installation

Add this marketplace:

```
/plugin marketplace add rijosimon/preflight
```

Install the plugin:

```
/plugin install plan-before-code@preflight
```

Reload:

```
/reload-plugins
```

## Usage

The skill is written to auto-invoke when Claude judges it relevant (any
nontrivial feature request). You can also invoke it explicitly:

```
/plan-before-code:plan
```
