---
layout: page
title: Memory Bank Protocol
permalink: /guides/memory-bank-protocol/
---

# Memory Bank Protocol

**Skill level: Practitioner**

## Core purpose
Treats an LLM's context window as finite working memory and externalizes project state into markdown files, so a long-running agent session doesn't lose track of decisions already made.

## What Claude Code actually provides for this
- **CLAUDE.md** — read at the start of every session (and again after compaction). Use it for coding standards, architecture decisions, and review checklists.
- **Auto memory** — Claude Code also builds its own memory as it works, across sessions, separately from what you write in CLAUDE.md.
- **`.claude/rules/`** — split instructions by concern, optionally scoped to specific file paths via YAML frontmatter, so a rule only loads when Claude is touching matching files.

## The real risk worth tracking
Because CLAUDE.md and Claude Code's own auto-built memory are separate mechanisms, they can drift out of sync. Keep CLAUDE.md as the single source of truth for anything load-bearing; treat auto memory as a nice-to-have, not a guarantee.

## Sources
- Anthropic, Claude Code documentation: [docs.claude.com/en/docs/claude-code/overview](https://docs.claude.com/en/docs/claude-code/overview)
- Verified directly against current docs on 2026-07-05.
