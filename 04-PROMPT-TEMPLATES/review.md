---
Title: Review Template
Version: 0.1.0
Status: Approved
Owner: Governance Orchestrator
Applies-To: Periodic Document Reviews
Last-Reviewed: 2026-01-02
Next-Review: 2026-04-02
---

# Review Template

Use this template for scheduled periodic reviews of prompts, policies, and procedures.

---

## Review Header (Required)

```yaml
---
Title: Review of [Document Name]
Version: 1.0.0
Status: Complete
Owner: [Reviewer name or role]
Applies-To: [Document being reviewed]
Review-Date: [YYYY-MM-DD]
Reviewer: [Name or role]
---
```

## Review Information

### 1. Document Identification

**Document Name**: [Full title of document being reviewed]  
**Document Version**: [Current version number]  
**Document Location**: [Path to document]  
**Document Owner**: [Responsible party]  
**Last Review Date**: [Previous review date]  
**This Review Date**: [Current review date]  
**Review Type**: [Scheduled|Triggered|Incident-Driven|Ad-Hoc]

### 2. Review Trigger

**Reason for Review**:
- [ ] Scheduled periodic review (per Next-Review date)
- [ ] Policy change impacting document
- [ ] Incident requiring review
- [ ] Requested by [Name/Role]
- [ ] Other: [Specify]

### 3. Document Status Check

**Current Status**: [Draft|Review|Approved|Deprecated]  
**Is Status Appropriate?**: [Yes|No]  
**Recommended Status**: [If change needed]

**Review Period**:
- **Last-Reviewed**: [YYYY-MM-DD]
- **Next-Review**: [YYYY-MM-DD]
- **Is document current?**: [Yes|No]

### 4. Content Review

**Accuracy**:
- [ ] Information is factually correct
- [ ] No contradictions with other policies
- [ ] References are valid and current
- [ ] Examples/procedures are still applicable

**Findings**: [Note any inaccuracies or outdated content]

**Completeness**:
- [ ] All required sections present
- [ ] Header block complete and valid
- [ ] Scope clearly defined
- [ ] Responsibilities clearly assigned

**Findings**: [Note any gaps or missing information]

**Clarity**:
- [ ] Language is clear and unambiguous
- [ ] Instructions are actionable
- [ ] Terms are defined or obvious
- [ ] Structure is logical

**Findings**: [Note any confusing or unclear sections]

### 5. Effectiveness Assessment

**Usage Metrics** (if available):
- Frequency of use: [How often referenced/executed]
- Success rate: [Percentage of successful applications]
- Incident rate: [Issues arising from this document]

**Has the document been effective?**: [Yes|No|Partially]  
**Evidence**: [Data or examples supporting assessment]

**User Feedback**:
- [Summarize feedback from agents/orchestrators using this document]
- [Note any recurring issues or suggestions]

### 6. Compliance Review

**Governance Alignment**:
- [ ] Aligns with constitutional principles
- [ ] Follows document control standards
- [ ] Respects separation of powers
- [ ] Includes appropriate review gates

**Policy Compliance**:
- [ ] Complies with all applicable policies
- [ ] No conflicts with other documents
- [ ] Authorization levels appropriate

**Findings**: [Note any compliance issues]

### 7. Change Assessment

**Changes Since Last Review**:
List any changes made to the document since last review:
1. [Change 1 with date and version]
2. [Change 2 with date and version]

**Were changes properly managed?**:
- [ ] Version incremented appropriately
- [ ] Changes documented in changelog
- [ ] Stakeholders notified
- [ ] Re-approval obtained if needed

**Environmental Changes**:
Have there been changes in the environment that affect this document?
- [ ] New tools or systems
- [ ] Organizational changes
- [ ] Policy updates
- [ ] Lessons learned from incidents

**Impact**: [Describe how environmental changes affect document relevance]

### 8. Recommendations

**Overall Assessment**: [Satisfactory|Needs Updates|Major Revision|Deprecate]

**Recommended Actions**:
Select all that apply:
- [ ] No changes needed - approve as-is
- [ ] Minor updates required (clarifications, typos)
- [ ] Moderate revision needed (update procedures/examples)
- [ ] Major overhaul required (scope/responsibilities change)
- [ ] Deprecate and replace with [new document]
- [ ] Deprecate without replacement (no longer needed)

**Specific Changes Needed**:
1. **[Section/Area]**: [What needs to change and why]
2. **[Section/Area]**: [What needs to change and why]
3. **[Section/Area]**: [What needs to change and why]

**Priority**: [Low|Medium|High|Critical]  
**Suggested Timeline**: [Timeframe for implementing changes]  
**Responsible Party**: [Who should make the changes]

### 9. Next Steps

**Immediate Actions**:
1. [Action 1]
2. [Action 2]

**Next Review Schedule**:
- **Recommended Next-Review Date**: [YYYY-MM-DD]
- **Rationale**: [Why this timeframe - typically 90 days]
- **Trigger conditions for early review**: [Circumstances requiring review before scheduled date]

**Stakeholder Notifications**:
- [ ] Document owner
- [ ] Meta-Orchestrator (if significant changes)
- [ ] Affected agents/departments
- [ ] Governance Orchestrator

### 10. Decision

**Review Decision**: [APPROVE|UPDATE REQUIRED|DEPRECATE]

**Approval to Continue Use** (if no immediate changes):
- [ ] Document approved for continued use as-is
- [ ] Next-Review date updated to [YYYY-MM-DD]
- [ ] Last-Reviewed date updated to [YYYY-MM-DD]

**Update Required**:
- [ ] Corrective action plan created
- [ ] Owner notified and assigned updates
- [ ] Target completion date: [YYYY-MM-DD]
- [ ] Status changed to "Review" until updates complete

**Deprecation**:
- [ ] Reason for deprecation: [Explanation]
- [ ] Replacement document: [If applicable]
- [ ] Transition plan: [How to migrate]
- [ ] Status changed to "Deprecated"

### 11. Sign-Off

**Reviewed By**: [Name/Role]  
**Review Date**: [YYYY-MM-DD]  
**Approved By** (if required): [Name/Role]  
**Approval Date**: [YYYY-MM-DD]

---

## Storage Location

Save completed reviews to: `07-RECORDS/reviews/[YYYY-MM-DD]-review-[document-name].md`

## Follow-Up

- Schedule follow-up review if updates required
- Track implementation of recommended changes
- Update document metadata after review complete
- Archive review record per retention policy
