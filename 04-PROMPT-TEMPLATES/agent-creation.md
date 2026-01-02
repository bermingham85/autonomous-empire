---
Title: Agent Creation Template
Version: 0.1.0
Status: Approved
Owner: System Architect
Applies-To: All Agent Prompts
Last-Reviewed: 2026-01-02
Next-Review: 2026-04-02
---

# Agent Creation Template

Use this template when creating new agent system prompts. All fields are required unless marked optional.

---

## Document Header (Required)

```yaml
---
Title: [Descriptive name of the agent]
Version: [X.Y.Z - Start with 1.0.0 for new agents]
Status: [Draft|Review|Approved|Deprecated]
Owner: [Person or role responsible for this agent]
Applies-To: [Agent identifier or department]
Last-Reviewed: [YYYY-MM-DD]
Next-Review: [YYYY-MM-DD - Typically 90 days from Last-Reviewed]
---
```

## Agent Prompt Structure

### 1. Identity and Role
**Purpose**: Define who the agent is and their primary function.

```
You are [AGENT NAME], a [role/function] within the AUTONOMOUS EMPIRE.

Your primary function is to [concise statement of purpose].
```

### 2. Core Responsibilities
**Purpose**: List the agent's key duties and accountabilities.

- **Responsibility 1**: Description
- **Responsibility 2**: Description
- **Responsibility 3**: Description

### 3. Scope and Boundaries
**Purpose**: Define what the agent CAN and CANNOT do.

**Within Scope:**
- [Action/capability 1]
- [Action/capability 2]
- [Action/capability 3]

**Out of Scope:**
- [Prohibited action 1]
- [Prohibited action 2]
- [Prohibited action 3]

### 4. Operating Principles
**Purpose**: Define the guiding principles for decision-making.

- **Principle 1**: Explanation
- **Principle 2**: Explanation
- **Principle 3**: Explanation

### 5. Interaction Protocols
**Purpose**: Define how the agent communicates with other agents/orchestrators.

**Reports To**: [Orchestrator or supervisor]

**Coordinates With**:
- **[Agent/Orchestrator Name]**: Purpose of coordination
- **[Agent/Orchestrator Name]**: Purpose of coordination

**Escalates To**: [Authority for unresolved issues]

### 6. Input/Output Specifications
**Purpose**: Define expected inputs and deliverable outputs.

**Expected Inputs**:
- Input type 1: Description
- Input type 2: Description

**Deliverable Outputs**:
- Output type 1: Format and location
- Output type 2: Format and location

### 7. Quality Standards
**Purpose**: Define acceptance criteria for agent outputs.

All outputs must:
- [Quality criterion 1]
- [Quality criterion 2]
- [Quality criterion 3]

### 8. Error Handling
**Purpose**: Define how the agent should handle errors and exceptions.

**When encountering [error type]**:
1. [Action step 1]
2. [Action step 2]
3. [Escalation path]

### 9. Success Metrics (Optional)
**Purpose**: Define how the agent's effectiveness is measured.

This agent is successful when:
- [Metric 1]
- [Metric 2]
- [Metric 3]

### 10. Special Instructions (Optional)
**Purpose**: Any unique or critical instructions specific to this agent.

---

## Approval Workflow

1. **Draft**: Creator completes template and sets Status to "Draft"
2. **Review**: Submit to relevant Department Lead and Governance Orchestrator
3. **Approval**: Operations Orchestrator approves for execution after governance clearance
4. **Deployment**: Add to `03-AGENTS/[department]/` with Status "Approved"

## Maintenance

- **Review Cycle**: Every 90 days or when agent scope changes
- **Version Updates**: 
  - Major (X.0.0): Breaking changes to agent responsibilities
  - Minor (0.X.0): New capabilities added
  - Patch (0.0.X): Clarifications or bug fixes

## Notes

- Keep prompts focused and concise
- Use clear, imperative language
- Avoid ambiguity in scope and responsibilities
- Test agent behavior before marking "Approved"
- Document any known limitations or issues
