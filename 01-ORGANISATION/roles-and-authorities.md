---
Title: Roles and Authorities Matrix
Version: 0.1.0
Status: Approved
Owner: System Architect
Applies-To: All Empire Personnel and Systems
Last-Reviewed: 2026-01-02
Next-Review: 2026-04-02
---

# Roles and Authorities

## Authority Levels

| Role | Prompt Approval | Build Blocking | Deployment | Policy Changes | Architecture |
|------|----------------|----------------|------------|----------------|--------------|
| **System Architect** | ✓ Final | ✓ Final | ✓ Final | ✓ Final | ✓ Final |
| **Meta-Orchestrator** | ✓ Strategic | ✓ Yes | ✓ Yes | ✓ Recommend | ✓ Propose |
| **Governance Orchestrator** | ✓ Required | ✓ Yes | ✓ Gate | ✓ Enforce | - Review |
| **Operations Orchestrator** | ✓ Tactical | - No | ✓ Execute | - No | - No |
| **Department Agents** | - Request | - No | - No | - No | - No |

## Detailed Authorities

### System Architect (Human)
- **Scope**: Ultimate authority over all empire operations
- **Can Approve**: Constitutional changes, structural modifications, final escalations
- **Can Block**: Any operation at any time
- **Requires**: N/A (top authority)

### Meta-Orchestrator
- **Scope**: Strategic coordination across all orchestrators and departments
- **Can Approve**: System architecture proposals, cross-orchestrator initiatives, agent creation
- **Can Block**: Operations that conflict with strategic direction
- **Requires**: System Architect approval for constitutional changes

### Governance Orchestrator
- **Scope**: Compliance, risk, quality, and security gates
- **Can Approve**: Deployments after validation, policy enforcement actions, audit requests
- **Can Block**: Any build or deployment that fails governance checks
- **Requires**: Cannot be bypassed by Operations Orchestrator

### Operations Orchestrator
- **Scope**: Execution coordination and delivery management
- **Can Approve**: Agent task assignments, resource allocation, build initiation
- **Can Block**: Agent tasks that exceed scope or resources
- **Requires**: Governance Orchestrator clearance for deployments

### Department Agents
- **Scope**: Execute assigned tasks within department mandate
- **Can Approve**: Work item completion within defined parameters
- **Can Block**: Nothing (must escalate to department oversight)
- **Requires**: Valid prompt with proper authorization

## Approval Workflows

### Prompt Approval
1. Author creates prompt using template (with header block)
2. Department reviews for technical feasibility
3. Governance Orchestrator reviews for compliance
4. Operations Orchestrator approves for execution
5. Meta-Orchestrator notified (no action required unless flagged)

### Build Approval
1. Operations Orchestrator initiates build request
2. Governance Orchestrator pre-validation (can block)
3. Agent executes build
4. Quality Department validates output
5. Governance Orchestrator post-validation (can block)
6. Operations Orchestrator approves deployment (if governance clears)

### Policy Changes
1. Proposer submits policy change with rationale
2. Governance Orchestrator impact assessment
3. Meta-Orchestrator strategic review
4. System Architect final approval
5. Governance Orchestrator enforces new policy

## Blocking Authority

### Who Can Block What

- **Governance Orchestrator**: Can block ANY build, deployment, or operation
- **Meta-Orchestrator**: Can block strategic initiatives and architecture changes
- **Operations Orchestrator**: Can block individual agent tasks (resource/scope issues)
- **System Architect**: Can override any block

### Block Resolution

1. Blocking party documents reason in `07-RECORDS/reviews/`
2. Submitter addresses concerns or escalates
3. If unresolved, escalates up chain to Meta-Orchestrator
4. Meta-Orchestrator mediates or escalates to System Architect
5. System Architect decision is final

## Audit Rights

- **System Architect**: Full audit access, any time
- **Governance Orchestrator**: Full audit access to all operations and records
- **Meta-Orchestrator**: Audit access to all orchestrator activities
- **Operations Orchestrator**: Audit access to department agent activities
- **Department Agents**: Read-only access to own task records
