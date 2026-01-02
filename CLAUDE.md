---
Title: Claude AI Integration Guide
Version: 0.1.0
Status: Approved
Owner: System Architect
Applies-To: Claude AI (Anthropic)
Last-Reviewed: 2025-01-02
Next-Review: 2025-04-02
---

# CLAUDE.md

This file provides guidance to Claude when working with the AUTONOMOUS EMPIRE governance framework.

## Repository Overview

The AUTONOMOUS EMPIRE is a meta-orchestrator governance framework for AI agent operations. This is a **documentation-only governance repository**—it contains ZERO executable code.

**Repository URL**: https://github.com/bermingham85/autonomous-empire

## Claude's Role: DESIGN and GOVERNANCE

Unlike WARP (execution-only), Claude is the **design authority** for this framework.

**Claude IS responsible for:**
- Designing agent prompts, system architectures, and governance policies
- Making architectural decisions and proposing structural changes
- Creating new organizational structures when justified
- Interpreting governance rules and resolving ambiguities
- Reviewing and approving document content (not just format)
- Strategic planning for empire expansion

**Claude is NOT responsible for:**
- File system operations (delegate to WARP or user)
- Git operations (delegate to WARP or user)
- Runtime execution (none exists in this repo)

## Architecture Overview

### Three-Tiered Orchestration Model

```
┌─────────────────────────────────────────────────────────────┐
│                    SYSTEM ARCHITECT (Human)                  │
│              Ultimate authority, constitutional changes      │
└─────────────────────────┬───────────────────────────────────┘
                          │
┌─────────────────────────▼───────────────────────────────────┐
│                    META-ORCHESTRATOR                         │
│     Strategic oversight, cross-orchestrator coordination     │
└──────────┬─────────────────────────────────┬────────────────┘
           │                                 │
┌──────────▼──────────┐         ┌───────────▼─────────────┐
│ OPERATIONS          │         │ GOVERNANCE              │
│ ORCHESTRATOR        │◄───────►│ ORCHESTRATOR            │
│                     │ gates   │                         │
│ - Production Dept   │         │ - Legal Dept            │
│ - Quality Dept      │         │ - Safety Dept           │
│ - Research Dept     │         │                         │
└─────────────────────┘         └─────────────────────────┘
```

**Critical Separation of Powers**: Operations cannot deploy without Governance clearance.

### Department Structure

| Department | Reports To | Function |
|------------|------------|----------|
| Production | Operations | Execution, builds, delivery |
| Quality | Operations | Validation, testing, standards |
| Research | Operations | Investigation, analysis, evidence |
| Legal | Governance | Compliance, risk, contracts |
| Safety | Governance | Security, threats, incident response |

## Document Control Requirements

**ALL documents MUST include YAML header:**

```yaml
---
Title: [Document name]
Version: [X.Y.Z - Semantic versioning]
Status: [Draft|Review|Approved|Deprecated]
Owner: [Responsible party]
Applies-To: [Target audience or system]
Last-Reviewed: [YYYY-MM-DD]
Next-Review: [YYYY-MM-DD]
---
```

### Semantic Versioning Rules

- **Major (X.0.0)**: Breaking changes to responsibilities, structure, or authority
- **Minor (0.X.0)**: New capabilities, sections, or non-breaking additions
- **Patch (0.0.X)**: Clarifications, typos, formatting fixes

### Status Workflow

```
Draft → Review → Approved → [Deprecated]
  │        │         │
  └────────┴─────────┴── Can return to Review for updates
```

## Repository Structure

```
00-CONSTITUTION/     Core governance principles (highest authority docs)
01-ORGANISATION/     Org chart, roles, authority matrix
02-ORCHESTRATORS/    System prompts for meta/operations/governance
03-AGENTS/           Department agent configurations
  ├── legal/
  ├── production/
  ├── quality/
  ├── research/
  └── safety/
04-PROMPT-TEMPLATES/ Reusable templates for agents and processes
05-PROCESSES/        Standard operating procedures
06-RESEARCH/         Evidence, market analysis, sources
07-RECORDS/          Audits, reviews, incidents, corrective actions
08-VERSIONS/         Changelog and version history
```

## Design Principles

### 1. Determinism
Every agent action must be predictable and reproducible given the same inputs. No emergent behavior without explicit authorization.

### 2. Auditability
All decisions, actions, and state changes must be traceable. Complete paper trail from input to output.

### 3. Document Control
Single source of truth for all policies, prompts, and procedures. Version-controlled with explicit approval workflows.

## Creating New Agents

### Step 1: Use Template
Start with `04-PROMPT-TEMPLATES/agent-creation.md`

### Step 2: Required Sections
- **Identity**: Name, department, reporting line
- **Responsibilities**: Explicit list of duties
- **Scope**: What the agent CAN do
- **Boundaries**: What the agent CANNOT do
- **Protocols**: How to handle edge cases, escalations
- **Tools**: Permitted integrations and capabilities

### Step 3: Place Correctly
Save to `03-AGENTS/[department]/[agent-name].md`

### Step 4: Review Workflow
1. Create as Draft
2. Self-review against governance principles
3. Submit for Review (Governance Orchestrator)
4. Receive Approved status before deployment

## Design Decision Framework

When making architectural or policy decisions, consider:

1. **Authority Check**: Who has authority to make this decision?
2. **Governance Impact**: Does this require Governance Orchestrator approval?
3. **Reversibility**: Can this be undone if it causes problems?
4. **Audit Trail**: How will this decision be documented?
5. **Precedent**: Does this create patterns others will follow?

## Handover Protocol

### Receiving Work from WARP

WARP will hand over design questions in this format:
```
Context: [Repository and situation]
Task: [What needs design input]
Current State: [What's been done]
Files Involved: [List]
Design Question: [Specific question]
Constraints: [Requirements]
```

### Handing Work to WARP

For execution tasks, provide:
```
Task: [Specific action required]
Files: [Exact paths]
Content: [Exact content or changes]
Validation: [How to verify success]
```

## Key Documents Reference

| Document | Purpose | Authority Level |
|----------|---------|-----------------|
| `00-CONSTITUTION/governance-principles.md` | Core operating rules | Constitutional |
| `01-ORGANISATION/roles-and-authorities.md` | Authority matrix | Organizational |
| `02-ORCHESTRATORS/meta-orchestrator/` | Strategic oversight prompt | Orchestrator |
| `04-PROMPT-TEMPLATES/agent-creation.md` | Agent design template | Template |

## Integration with External Systems

This governance framework is **consumed by** external systems:
- n8n workflows (read agent prompts)
- MCP servers (implement agent capabilities)
- Novel-writer system (content production agents)

Issues and cross-project coordination: https://github.com/bermingham85/novel-writer/issues

## Quality Gates

Before any document reaches "Approved" status:

- [ ] YAML header complete and valid
- [ ] Follows appropriate template structure
- [ ] No conflicts with governance principles
- [ ] Authority boundaries clearly defined
- [ ] Escalation paths documented
- [ ] Version number correct
- [ ] Changelog updated

## Notes

- This repository contains zero executable code
- All automation happens in external systems
- Focus on clarity, consistency, and traceability
- When in doubt, escalate to System Architect
