---
layout: page
title: Context Management (Claude Code)
permalink: /guides/context-management/
---

# Context Management (Claude Code)

**Skill level: Practitioner**

## Why it matters
Claude Code's context window fills with every prompt, tool call, file read, and terminal output during a session. Quality degrades before you hit the hard limit, not just at it.

## The real commands
- **`/context`** — shows what's actually occupying your context window right now.
- **`/compact [focus]`** — summarizes older conversation history to free up space, optionally focused on a topic.
- **`/clear`** — wipes history completely and starts fresh (project memory in CLAUDE.md still loads back in).
- **`.claude/rules/*.md`** with a `paths:` frontmatter glob — rules load only when Claude is working with matching files.

## Practical habit
Re-seed a cleared session with a short markdown plan file rather than re-explaining context from memory — plain text as the interface, applied within a single session.

## Subagents for large reads
Delegate large log/file reads to a subagent running in its own context, which returns a synthesized summary — keeps the main session's context focused on decisions, not raw data.

## Sources
- Anthropic, Claude Code documentation: [docs.claude.com/en/docs/claude-code/overview](https://docs.claude.com/en/docs/claude-code/overview) and [code.claude.com/docs/en/slash-commands](https://code.claude.com/docs/en/slash-commands)
- Verified directly against current docs on 2026-07-05.
