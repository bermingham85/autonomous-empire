---
Title: WARP AI Integration Guide
Version: 0.1.0
Status: Approved
Owner: System Architect
Applies-To: Warp AI Terminal
Last-Reviewed: 2025-01-02
Next-Review: 2025-04-02
---

# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Repository Overview

The AUTONOMOUS EMPIRE is a meta-orchestrator governance framework for AI agent operations. This is a **documentation-only governance repository**—it contains ZERO executable code.

**What this repository IS:**
- System prompts for AI orchestrators and agents
- Organizational policies and governance documents
- Document control and audit records
- Markdown files with strict YAML header requirements

**What this repository IS NOT:**
- A software codebase with runtime or dependencies
- An executable system (no package.json, no scripts, no builds)
- A programming project requiring compilation or testing

## Document Control Requirements

**CRITICAL**: ALL documents in this repository MUST include a YAML header block:

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

**Documents without proper headers are considered invalid and will not be executed or enforced.**

## Repository Structure

```
00-CONSTITUTION/     - Core governance principles and constitutional policies
01-ORGANISATION/     - Org chart, roles, authorities matrix
02-ORCHESTRATORS/    - System prompts for meta, operations, governance orchestrators
03-AGENTS/          - Department-specific agent configurations (production, quality, legal, safety, research)
04-PROMPT-TEMPLATES/ - Reusable templates for creating agents and processes
05-PROCESSES/       - Standard operating procedures (currently empty)
06-RESEARCH/        - Research sources, market analysis, evidence gathering
07-RECORDS/         - Audit trails, reviews, incidents, corrective actions
08-VERSIONS/        - Version history and changelog
```

## Architecture Concepts

### Three-Tiered Orchestration Model

1. **Meta-Orchestrator** - Strategic oversight, cross-orchestrator coordination, architecture decisions
2. **Operations Orchestrator** - Execution coordination, delivery management, agent task assignment
3. **Governance Orchestrator** - Compliance gates, quality validation, blocking authority

**Critical Separation of Powers**: No single orchestrator can unilaterally deploy. Operations requires Governance clearance for all deployments.

### Department Structure

Five functional departments report to orchestrators:
- **Production Department** → Operations (execution and builds)
- **Quality Department** → Operations (validation and testing)
- **Research Department** → Operations (investigation and analysis)
- **Legal Department** → Governance (compliance and risk)
- **Safety Department** → Governance (security and threat assessment)

### Authority Hierarchy

- **System Architect** (human): Ultimate authority, constitutional changes only
- **Meta-Orchestrator**: Strategic decisions, architecture proposals
- **Governance Orchestrator**: Can BLOCK any build/deployment; enforces quality gates
- **Operations Orchestrator**: Executes approved work but CANNOT bypass governance
- **Department Agents**: Execute tasks within defined scope; no blocking authority

## Document Management Operations

### Creating a New Agent Prompt

1. Use the template: `04-PROMPT-TEMPLATES/agent-creation.md`
2. Fill all required sections (identity, responsibilities, scope, boundaries, protocols)
3. Include complete YAML header with Status: Draft
4. Save to appropriate department in `03-AGENTS/[department]/`
5. Follow approval workflow: Draft → Review → Approved

### Creating a New Policy/Process Document

1. Start with appropriate template from `04-PROMPT-TEMPLATES/`
2. Include mandatory YAML header
3. Set Status to "Draft" initially
4. Document owner and review dates (typically 90 days)
5. Follow approval chain per `01-ORGANISATION/roles-and-authorities.md`

### Reviewing/Updating Documents

1. Check `Next-Review` dates in YAML headers
2. Update version number according to semantic versioning:
   - **Major (X.0.0)**: Breaking changes to responsibilities/structure
   - **Minor (0.X.0)**: New capabilities or sections added
   - **Patch (0.0.X)**: Clarifications, typo fixes, non-breaking updates
3. Update `Last-Reviewed` and `Next-Review` dates
4. Document changes in `08-VERSIONS/changelog.md`

### Version Control Commands

```powershell
# View repository status
git status

# View commit history
git --no-pager log --oneline -20

# View changes to specific document
git --no-pager diff HEAD~1 00-CONSTITUTION/governance-principles.md

# Commit changes (always include co-author for AI contributions)
git commit -m "feat: add new safety agent prompt

Co-Authored-By: Warp <agent@warp.dev>"
```

## Document Validation

### YAML Header Validation Checklist

Before any document can be considered valid:
- [ ] YAML header block present with all required fields
- [ ] Version number follows semantic versioning (X.Y.Z)
- [ ] Status is set correctly (Draft|Review|Approved|Deprecated)
- [ ] Owner is clearly identified
- [ ] Last-Reviewed date is in YYYY-MM-DD format
- [ ] Next-Review date is set (typically 90 days from Last-Reviewed)
- [ ] Applies-To field specifies target audience
- [ ] Title matches document purpose

### Document Structure Validation

Verify document follows appropriate template:
- [ ] Agent prompts use `04-PROMPT-TEMPLATES/agent-creation.md` structure
- [ ] Policy documents include all required sections
- [ ] Content is clear, unambiguous, and actionable
- [ ] File is placed in correct directory (00-08)

**Note**: Governance compliance gates (approval workflows) are policy matters handled by orchestrators, not Warp's execution role.

## Key Files to Review

- `README.md` - Empire rules and overview
- `00-CONSTITUTION/governance-principles.md` - Core operating principles (determinism, auditability, document control)
- `01-ORGANISATION/org-chart.md` - Command structure and departments
- `01-ORGANISATION/roles-and-authorities.md` - Authority matrix and approval workflows
- `04-PROMPT-TEMPLATES/agent-creation.md` - Standard template for new agent prompts
- `08-VERSIONS/changelog.md` - Version history and release notes

## Warp AI Integration

### CRITICAL: Warp's Execution-Only Role

**This is NOT a software codebase. There is NO runtime, NO package.json, NO executable code.**

**Warp's STRICT Role: EXECUTION and DOCUMENT CONTROL ONLY**

You may ONLY:
- Edit files when explicitly instructed by the user
- Validate YAML headers and required metadata
- Enforce folder placement rules (proper directories)
- Check semantic versioning compliance
- Perform git operations when asked (commit, diff, log, status)
- Verify document structure matches templates

**Warp MUST NOT:**
- Infer runtimes, frameworks, or package managers (NONE EXIST HERE)
- Design or modify agent logic, system prompts, or governance rules
- Create new organizational structures without explicit instruction
- Make policy or architectural decisions
- Assume any "development" workflow beyond document editing

### Mandatory Stop Condition

**IF any instruction requires:**
- Design judgment or policy decisions
- Creating/modifying agent logic or system prompts
- Architectural changes or new organizational structures
- Governance rule interpretation

**THEN:**
1. **STOP immediately**
2. **Do NOT attempt the task**
3. **Request handover to Claude** using the format below

### Handover Format for Design/Policy Decisions

When transferring work to Claude for design review:
```
Context: Working in AUTONOMOUS-EMPIRE repository
Task: [Specific task requiring design input]
Current State: [What has been done]
Files Involved: [List of files]
Design Question: [Specific question for Claude]
Constraints: [Governance requirements, existing architecture]
```

## Working with This Repository

### When Adding New Content
1. Always use templates from `04-PROMPT-TEMPLATES/`
2. Follow strict YAML header requirements
3. Default Status to "Draft" for new documents
4. Set Next-Review to 90 days from Last-Reviewed

### When Modifying Existing Content
1. Check current Status (don't edit "Approved" without changing to "Review")
2. Update version number appropriately
3. Update Last-Reviewed date
4. Add entry to `08-VERSIONS/changelog.md`

### When Reviewing Documents
1. Verify header completeness and validity
2. Check for expired Next-Review dates
3. Ensure content matches template structure
4. Validate semantic versioning is correct

## Notes

- This repository contains zero executable code—only Markdown documentation
- All automation and execution happens in EXTERNAL systems that consume these documents
- Version control and document control are the primary technical activities
- Focus on clarity, consistency, and traceability in all changes
