---
layout: default
title: "Getting Started: Claude AI, Claude Code, and Skills Explained"
permalink: /guides/getting-started-claude-ecosystem/
category: Getting Started
last_verified: 2026-07-23
sources:
  - https://code.claude.com/docs/en/overview
  - https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview
---

# Getting Started: Claude AI, Claude Code, and Skills Explained

New to Claude and confused about the difference between "Claude AI," "Claude Code," and "Skills"? Start here.

## One Model, Three Ways to Use It

| | Claude.ai | Claude Code |
|---|---|---|
| **What it is** | A chat interface (web/app) | An agentic tool for your terminal, IDE, or desktop |
| **What it can touch** | Only the conversation | Your actual files, folders, and git repo |
| **Best for** | Writing, planning, research, one-off questions | Building software, fixing bugs, automating file/repo work |

Think of Claude.ai as a conversation with an expert. Claude Code is that same expert, given the keys to actually do the work on your computer — <cite index="9-1">it can build features from a plain-English description, debug issues by tracing them through your codebase, answer questions about any part of a project, and automate tedious tasks like fixing lint errors or writing release notes</cite>.

## What Are "Skills"?

<cite index="14-1">A Skill is a reusable instruction package — a folder containing a file called SKILL.md — that teaches Claude how to handle one specific kind of task. Install it once, and Claude uses it automatically whenever it's relevant, without you re-explaining the task each time.</cite>

The clever part: <cite index="10-1">Claude only sees a short description of each skill at first. It loads the full instructions only when your request actually matches that skill</cite> — so it stays efficient rather than trying to remember everything at once.

## How They Work Together

A typical real-world flow looks like this:

1. **Plan and write in Claude.ai** — strategy documents, guides, content drafts.
2. **Build and ship in Claude Code** — turning that plan into actual files, commits, and working systems, with Skills firing automatically for specialized sub-tasks (like formatting a specific document type or following an API's quirks).
3. **Verify against the real system** — when in doubt about current state (counts, live data, configuration), pull from the actual source system rather than trusting a past conversation's summary.

## Where to Start

1. Use Claude.ai for anything you'd normally think through in writing.
2. When a task involves real files or a codebase, move to Claude Code.
3. If you find yourself repeating the same specialized instructions often, that's a sign a custom Skill would help.
4. Keep a `CLAUDE.md` file at the root of any ongoing project — it's the standing context Claude Code reads at the start of every session, so your setup travels with the project instead of living in one conversation.

---
*Verified against official Anthropic documentation, last checked 2026-07-23.*
