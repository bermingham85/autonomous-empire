# AUTONOMOUS EMPIRE

**Version:** 0.1.0  
**Status:** Initial Structure  
**Owner:** System Architect  
**Last Updated:** 2026-01-02

## Overview

The AUTONOMOUS EMPIRE is a meta-orchestrator project that serves as the canonical source of truth for AI agent orchestration, governance, and autonomous operations. This repository contains the organizational structure, policies, prompts, and documentation that govern the empire's operations.

## Rules of the Empire

### Document Control Requirements

**ALL files in this repository MUST adhere to the following:**

1. **Header Block Requirement**: Every prompt, policy, and critical document must start with a YAML-style header block containing:
   - `Title`: Document name
   - `Version`: Semantic version (e.g., 1.0.0)
   - `Status`: Draft | Review | Approved | Deprecated
   - `Owner`: Responsible party
   - `Applies-To`: Target audience or system
   - `Last-Reviewed`: ISO date (YYYY-MM-DD)
   - `Next-Review`: ISO date (YYYY-MM-DD)

2. **Invalid Documents**: Files without proper headers are considered invalid and will not be executed or enforced.

3. **Change Management**: All modifications must be tracked in version control with clear commit messages.

4. **Review Cycles**: Documents must be reviewed according to their `Next-Review` date.

## Core Principles

- **Determinism**: All operations must be reproducible and predictable
- **Auditability**: Every action must be traceable and documented
- **Document Control**: Strict versioning and review processes
- **Separation of Concerns**: Clear boundaries between orchestrators, agents, and processes

## Repository Structure

```
00-CONSTITUTION/     - Core governance principles and policies
01-ORGANISATION/     - Organizational structure and role definitions
02-ORCHESTRATORS/    - System prompts for meta, operations, and governance orchestrators
03-AGENTS/          - Department-specific agent configurations
04-PROMPT-TEMPLATES/ - Reusable templates for creating new agents and processes
05-PROCESSES/       - Standard operating procedures
06-RESEARCH/        - Research sources, market analysis, and evidence
07-RECORDS/         - Audit trails, reviews, incidents, and corrective actions
08-VERSIONS/        - Version history and changelogs
```

## Getting Started

1. Review the governance principles in `00-CONSTITUTION/governance-principles.md`
2. Understand the organizational structure in `01-ORGANISATION/org-chart.md`
3. Familiarize yourself with roles and authorities in `01-ORGANISATION/roles-and-authorities.md`
4. Use prompt templates from `04-PROMPT-TEMPLATES/` when creating new agents

## Version History

See `08-VERSIONS/changelog.md` for detailed version history.
