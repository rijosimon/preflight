# preflight

**A growing marketplace of Claude Code plugins for writing better code.**

Not a single trick — a place to collect the tools that make an AI coding
agent something you can actually trust with real work: better judgment,
safer defaults, more discipline. Add the marketplace once
(`/plugin marketplace add rijosimon/preflight`) and every plugin published
here becomes installable, with no re-adding required as new ones ship.

## Available now: plan-before-code

Your AI coding agent is fast — that's exactly the problem. Left alone, it
reads a one-line request, silently decides the scope, and hands you back a
sprawling diff before you've had a chance to weigh in on a single design
choice it made along the way. By the time you're reviewing code, every
decision is already baked in — and unwinding a bad assumption now costs a
rewrite, not a sentence.

**plan-before-code** fixes this: before any nontrivial change, Claude
writes up what it's about to do — as epics and stories, in a plain file
you can actually read — and waits for you to confirm before touching a
line of code.

- **Catch bad assumptions before they're code.** Redirecting a plan takes
  one sentence. Redirecting a finished implementation takes a rewrite.
- **A paper trail that outlives the diff.** Once work is done, Claude
  records what changed, what deviated from plan, and why — the reasoning a
  commit message never captures, still there when you need it months later.
- **Zero overhead on small stuff.** Typos, one-line fixes, config tweaks
  skip the process automatically. This only kicks in when the stakes are
  high enough to matter.
- **It just works, unprompted.** No slash command required — Claude
  recognizes nontrivial work and plans it automatically, the same
  discipline on every project you install it in.

See [`plan-before-code/README.md`](plan-before-code/README.md) for the full
mechanics: the epic format, exactly when it skips planning, and how to
invoke it manually with `/plan-before-code:plan`.

## Install

```
/plugin marketplace add rijosimon/preflight
/plugin install plan-before-code@preflight
/reload-plugins
```

## What's next

preflight will grow to include more plugins — additional skills,
subagents, and MCP server integrations — all under the same marketplace,
all aimed at the same goal: code you can trust because the agent that
wrote it earned it.
