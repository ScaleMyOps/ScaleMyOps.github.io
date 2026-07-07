---
layout: page
title: Interpretable Context Methodology (ICM)
permalink: /guides/icm-architecture/
---

# Interpretable Context Methodology (ICM)

**Skill level: Practitioner**

## Core idea
For sequential, human-reviewed AI workflows, numbered folders and markdown files can replace a multi-agent coordination framework: one agent reads the right files at the right stage instead of a framework managing multiple specialized agents.

## Five-layer context hierarchy
- Layer 0: workspace identity (a root CLAUDE.md)
- Layer 1: workspace-level task routing
- Layer 2: stage-specific contract (what a stage reads, does, and writes)
- Layer 3: reference material — stable rules that persist across runs
- Layer 4: working artifacts — content that changes each run

## When this fits, and when it doesn't
**Good fit:** sequential, reviewable, repeatable work — content pipelines, reporting, research-to-brief workflows, a knowledge base like this one.
**Poor fit:** real-time multi-agent collaboration, high-concurrency systems serving many simultaneous users, or automated (non-human) branching mid-pipeline.

## Evidence caveat
The architecture is well-grounded in established software-engineering principles (Unix philosophy, separation of concerns). The paper's own effectiveness numbers, however, come from a small, self-selected practitioner community with no controlled comparison — treat those specific figures as illustrative, not proven.

## Sources
- Van Clief, J. & McDermott, D., "Interpretable Context Methodology: Folder Structure as Agent Architecture," arXiv:2603.16021, 2026. [arxiv.org/abs/2603.16021](https://arxiv.org/abs/2603.16021)
- Reference implementation: [github.com/RinDig/Interpreted-Context-Methdology](https://github.com/RinDig/Interpreted-Context-Methdology)
- *Note: this is an arXiv preprint, not peer-reviewed. The author's consultancy and paid community mean this doubles as thought-leadership marketing — the architecture is sound, the performance claims are anecdotal.*
