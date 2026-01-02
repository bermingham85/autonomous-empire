---
Title: Assessment Template
Version: 0.1.0
Status: Approved
Owner: Governance Orchestrator
Applies-To: All Governance Assessments
Last-Reviewed: 2026-01-02
Next-Review: 2026-04-02
---

# Assessment Template

Use this template when conducting governance assessments of deliverables, prompts, or policy changes.

---

## Assessment Header (Required)

```yaml
---
Title: Assessment of [Subject]
Version: 1.0.0
Status: [Draft|Complete]
Owner: [Assessor name or role]
Applies-To: [What is being assessed]
Assessment-Date: [YYYY-MM-DD]
Assessed-By: [Governance Orchestrator or delegated authority]
---
```

## Assessment Details

### 1. Subject Information

**Subject**: [Name/identifier of what is being assessed]  
**Subject Version**: [Version number if applicable]  
**Subject Owner**: [Who is responsible for the subject]  
**Submitted By**: [Who requested the assessment]  
**Submission Date**: [YYYY-MM-DD]

### 2. Assessment Scope

**Type of Assessment**:
- [ ] Pre-validation (before execution)
- [ ] Post-validation (after completion)
- [ ] Periodic review
- [ ] Incident investigation
- [ ] Policy compliance audit
- [ ] Other: [Specify]

**Assessment Criteria**:
List the specific standards, policies, or requirements being evaluated against.

1. [Criterion 1]
2. [Criterion 2]
3. [Criterion 3]

### 3. Document Control Check

- [ ] Subject has valid header block
- [ ] Version number is appropriate
- [ ] Status field is accurate
- [ ] Owner is identified
- [ ] Last-Reviewed date is present
- [ ] Next-Review date is present and future-dated
- [ ] Document is within review period

**Document Control Status**: [PASS|FAIL]  
**Issues Found**: [List any document control violations]

### 4. Technical Validation

**Evaluation**:
- [ ] Syntax/format is correct
- [ ] Technical specifications are met
- [ ] Implementation is sound
- [ ] Dependencies are satisfied
- [ ] Testing is complete (if applicable)

**Technical Status**: [PASS|FAIL|N/A]  
**Findings**: [Describe technical issues or validation results]

### 5. Compliance Check

**Policy Compliance**:
- [ ] Adheres to governance principles
- [ ] Follows established processes
- [ ] Meets quality standards
- [ ] Respects scope boundaries
- [ ] Authorization is proper

**Compliance Status**: [PASS|FAIL|N/A]  
**Violations**: [List any policy or process violations]

### 6. Security Review

**Security Assessment**:
- [ ] No critical vulnerabilities identified
- [ ] Access controls are appropriate
- [ ] Data handling is secure
- [ ] Third-party dependencies are vetted
- [ ] Security best practices followed

**Security Status**: [PASS|FAIL|N/A]  
**Security Concerns**: [List any security issues or risks]

### 7. Risk Assessment

**Risk Level**: [Low|Medium|High|Critical]

**Identified Risks**:
1. **[Risk name]**: [Description]
   - **Impact**: [Low|Medium|High]
   - **Likelihood**: [Low|Medium|High]
   - **Mitigation**: [How risk is mitigated or accepted]

2. **[Risk name]**: [Description]
   - **Impact**: [Low|Medium|High]
   - **Likelihood**: [Low|Medium|High]
   - **Mitigation**: [How risk is mitigated or accepted]

### 8. Overall Assessment

**Decision**: [APPROVE|BLOCK|CONDITIONAL APPROVAL]

**Rationale**:
[Provide clear explanation for the decision based on findings above]

**Conditions** (if applicable):
List any conditions that must be met before approval:
1. [Condition 1]
2. [Condition 2]

**Recommendations**:
- [Recommendation 1]
- [Recommendation 2]

### 9. Required Actions

**For BLOCK decisions**:
- **What must be corrected**: [Specific issues to address]
- **Who is responsible**: [Owner or assigned party]
- **Resubmission required**: [Yes|No]
- **Escalation path**: [If issues cannot be resolved]

**For CONDITIONAL APPROVAL**:
- **Conditions to satisfy**: [List conditions]
- **Verification method**: [How conditions will be verified]
- **Deadline**: [YYYY-MM-DD]

**For APPROVE**:
- **Effective date**: [YYYY-MM-DD]
- **Next review date**: [YYYY-MM-DD]
- **Monitoring requirements**: [Any ongoing oversight needed]

### 10. Documentation

**Evidence**:
- [Link or reference to supporting documentation]
- [Test results or validation reports]
- [Security scan reports]

**Related Records**:
- Previous assessments: [References]
- Related incidents: [References]
- Policy documents: [References]

### 11. Sign-Off

**Assessed By**: [Name/Role]  
**Date**: [YYYY-MM-DD]  
**Approved By** (if required): [Name/Role]  
**Date**: [YYYY-MM-DD]

---

## Storage

Save completed assessments to:
- **Pre/Post Validation**: `07-RECORDS/reviews/[YYYY-MM-DD]-[subject-name].md`
- **Incident Related**: `07-RECORDS/incidents/[YYYY-MM-DD]-[incident-id].md`
- **Audit Reports**: `07-RECORDS/audits/[YYYY-MM-DD]-[audit-type].md`

## Retention

- Keep all assessments for minimum 1 year
- Archive approved assessments after 1 year
- Retain blocked/incident assessments indefinitely
