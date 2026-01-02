---
Title: Corrective Action Template
Version: 0.1.0
Status: Approved
Owner: Governance Orchestrator
Applies-To: All Corrective Actions
Last-Reviewed: 2026-01-02
Next-Review: 2026-04-02
---

# Corrective Action Template

Use this template when documenting corrective actions for incidents, governance violations, or systemic issues.

---

## Corrective Action Header (Required)

```yaml
---
Title: Corrective Action - [Brief Description]
Version: 1.0.0
Status: [Draft|In-Progress|Complete|Verified]
Owner: [Person/role responsible for correction]
Applies-To: [System/agent/process affected]
Created-Date: [YYYY-MM-DD]
Target-Completion: [YYYY-MM-DD]
Actual-Completion: [YYYY-MM-DD or TBD]
---
```

## Corrective Action Plan

### 1. Issue Identification

**Issue ID**: [Reference number if from incident/review]  
**Issue Title**: [Brief description]  
**Discovery Date**: [YYYY-MM-DD]  
**Discovered By**: [Name/role]  
**Severity**: [Low|Medium|High|Critical]

**Type of Issue**:
- [ ] Governance violation
- [ ] Quality failure
- [ ] Security incident
- [ ] Process breakdown
- [ ] Policy non-compliance
- [ ] Systemic problem
- [ ] Other: [Specify]

**Description**:
[Detailed description of what went wrong]

**Impact**:
[Describe the impact - what was affected, what are the consequences]

### 2. Root Cause Analysis

**Analysis Method Used**:
- [ ] 5 Whys
- [ ] Fishbone diagram
- [ ] Timeline analysis
- [ ] Incident review
- [ ] Other: [Specify]

**Root Cause(s)**:
1. **[Root cause 1]**: [Detailed explanation]
   - **Category**: [Process|Technology|Human|Policy]
   - **Evidence**: [What supports this conclusion]

2. **[Root cause 2]**: [Detailed explanation]
   - **Category**: [Process|Technology|Human|Policy]
   - **Evidence**: [What supports this conclusion]

**Contributing Factors**:
- [Factor 1]: [How it contributed]
- [Factor 2]: [How it contributed]

**Why This Happened**:
[Synthesize root causes into clear explanation]

### 3. Immediate Actions Taken

**Emergency Response** (if applicable):
List any immediate actions taken to contain or mitigate:
1. **[Action]**: [When taken, by whom, result]
2. **[Action]**: [When taken, by whom, result]

**Temporary Workaround** (if applicable):
- **Workaround**: [Description]
- **Implemented**: [YYYY-MM-DD]
- **Effectiveness**: [Assessment]
- **Duration**: [Until permanent fix]

### 4. Corrective Actions

**Action 1: [Brief Title]**
- **Description**: [What will be done]
- **Rationale**: [Why this addresses root cause]
- **Owner**: [Who is responsible]
- **Target Date**: [YYYY-MM-DD]
- **Status**: [Not Started|In Progress|Complete]
- **Dependencies**: [Prerequisites or blockers]
- **Verification Method**: [How we'll know it's done correctly]

**Action 2: [Brief Title]**
- **Description**: [What will be done]
- **Rationale**: [Why this addresses root cause]
- **Owner**: [Who is responsible]
- **Target Date**: [YYYY-MM-DD]
- **Status**: [Not Started|In Progress|Complete]
- **Dependencies**: [Prerequisites or blockers]
- **Verification Method**: [How we'll know it's done correctly]

**Action 3: [Brief Title]**
[Continue as needed]

### 5. Preventive Measures

**Changes to Prevent Recurrence**:

**Process Changes**:
- [ ] Update procedure: [Which procedure, how]
- [ ] Add review gate: [Where, what checks]
- [ ] Modify workflow: [What changes]

**Policy Changes**:
- [ ] Update policy: [Which policy, what changes]
- [ ] Create new policy: [What coverage]
- [ ] Clarify requirements: [Where, what needs clarification]

**Training/Communication**:
- [ ] Train affected parties on: [Topic]
- [ ] Communicate lesson learned to: [Audience]
- [ ] Update documentation: [Which documents]

**Technical Changes**:
- [ ] Implement validation: [What kind, where]
- [ ] Add monitoring: [What to monitor]
- [ ] Improve tooling: [What improvements]

### 6. Verification Plan

**How Will We Verify Effectiveness?**

**Success Criteria**:
1. [Criterion 1]: [How measured]
2. [Criterion 2]: [How measured]
3. [Criterion 3]: [How measured]

**Verification Activities**:
- [ ] Test corrective actions in controlled environment
- [ ] Review after implementation
- [ ] Monitor for [X period] to ensure no recurrence
- [ ] Conduct follow-up assessment on [date]

**Verification Owner**: [Who verifies]  
**Verification Date**: [YYYY-MM-DD]

### 7. Implementation Tracking

**Timeline**:

| Action | Owner | Start Date | Target Date | Status | Notes |
|--------|-------|------------|-------------|--------|-------|
| [Action 1] | [Name] | [Date] | [Date] | [Status] | [Notes] |
| [Action 2] | [Name] | [Date] | [Date] | [Status] | [Notes] |
| [Action 3] | [Name] | [Date] | [Date] | [Status] | [Notes] |

**Milestones**:
- [ ] Root cause identified - [Date]
- [ ] Corrective action plan approved - [Date]
- [ ] Actions implemented - [Date]
- [ ] Verification complete - [Date]
- [ ] Issue closed - [Date]

### 8. Communication Plan

**Who Needs to Know**:
- [ ] System Architect
- [ ] Meta-Orchestrator
- [ ] Governance Orchestrator
- [ ] Operations Orchestrator
- [ ] Affected departments
- [ ] All agents (empire-wide)

**Communication Method**:
- [ ] Formal report
- [ ] Email notification
- [ ] Document in records
- [ ] Lesson learned session

**Key Messages**:
1. [What happened]
2. [What was done]
3. [What changed]
4. [What's expected going forward]

### 9. Cost/Impact Assessment

**Resources Required**:
- **Time**: [Estimated person-hours]
- **Budget**: [If applicable]
- **Tools/Systems**: [Any new tools needed]

**Disruption Assessment**:
- **Downtime required**: [If any]
- **Affected operations**: [What's impacted during fix]
- **Mitigation**: [How to minimize disruption]

### 10. Lessons Learned

**What Went Well**:
- [Positive aspect 1]
- [Positive aspect 2]

**What Could Be Improved**:
- [Improvement area 1]
- [Improvement area 2]

**Systemic Issues Identified**:
- [Broader issue 1]
- [Broader issue 2]

**Recommendations for Future**:
1. [Recommendation 1]
2. [Recommendation 2]

### 11. Closure

**Completion Status**: [Complete|Partial|Ongoing]

**Completion Summary**:
[Brief summary of what was accomplished]

**Outstanding Items** (if any):
- [Item 1]: [Why outstanding, new owner/date]
- [Item 2]: [Why outstanding, new owner/date]

**Verification Results**:
- **Verified By**: [Name/role]
- **Verification Date**: [YYYY-MM-DD]
- **Result**: [Pass|Fail|Partial]
- **Evidence**: [Reference to verification records]

**Sign-Off**:
- **Completed By**: [Name/role] on [YYYY-MM-DD]
- **Reviewed By**: [Governance Orchestrator] on [YYYY-MM-DD]
- **Approved By**: [Meta-Orchestrator if required] on [YYYY-MM-DD]

**Follow-Up Required**:
- [ ] No follow-up needed
- [ ] Schedule review in [X days/months]
- [ ] Monitor metric: [What metric, for how long]
- [ ] Related work: [Reference to related initiatives]

---

## Storage Location

Save to: `07-RECORDS/corrective-actions/[YYYY-MM-DD]-[issue-id]-corrective-action.md`

Link from related incident/review: `07-RECORDS/incidents/[incident-id].md`

## Retention

- Retain all corrective action records indefinitely
- Include in annual governance reporting
- Reference in training and onboarding materials
