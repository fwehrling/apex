
# APEX Files - Step 4: REVIEW

You are performing a thorough review of the completed implementation.

## Prerequisites

1. Locate the task directory
2. Read all previous files:
   - `analysis.md` - Original requirements
   - `implementation-plan.md` - What was planned
   - `implementation-notes.md` - What was actually done

## Instructions

### 1. Gather Context

Read all task files and understand:
- What was supposed to be built
- What was actually built
- Any deviations or decisions made

### 2. Code Review

Review all modified/created files for:

**Correctness**
- Does it fulfill the requirements?
- Are there logic errors?
- Are edge cases handled?

**Code Quality**
- Follows project conventions?
- Clean and readable?
- No code smells?

**Type Safety** (if TypeScript)
- Proper typing?
- No `any` types?
- Interfaces well-defined?

**Performance**
- No obvious performance issues?
- Efficient algorithms?
- No memory leaks?

**Security**
- Input validation?
- No XSS/injection risks?
- Proper authentication/authorization?

### 3. Testing Verification

- Run all tests: `pnpm test` (or equivalent)
- Check test coverage if available
- Perform manual testing steps from the plan

### 4. Create Review Report

Create `review-report.md` in the task directory:

```markdown
# Review Report: [Feature Name]

## Date: [Current Date]
## Reviewer: Claude Code
## Status: Approved / Needs Changes / Rejected

## 1. Implementation Summary

### What Was Built
[Brief description of the implemented feature]

### Files Changed
| File | Lines Added | Lines Removed | Assessment |
|------|-------------|---------------|------------|
| path/to/file | +XX | -XX | Good / Needs attention |

## 2. Requirements Verification

| Requirement | Status | Notes |
|-------------|--------|-------|
| [Requirement 1] | Met | |
| [Requirement 2] | Met | |
| [Requirement 3] | Partial | [What's missing] |

## 3. Code Quality Assessment

### Strengths
- [What was done well]
- [Good patterns used]

### Areas for Improvement
- [ ] [Improvement 1] - Priority: Low/Medium/High
- [ ] [Improvement 2] - Priority: Low/Medium/High

## 4. Test Results

### Automated Tests
- Unit Tests: Passing (XX/XX)
- Integration Tests: Passing (XX/XX)
- Type Check: No errors

### Manual Testing
- [ ] [Test case 1] - Passed
- [ ] [Test case 2] - Passed

## 5. Security Review

- [ ] Input validation: Adequate
- [ ] Authentication: Proper
- [ ] Authorization: Proper
- [ ] Data sanitization: Adequate

## 6. Performance Considerations

[Any performance observations or concerns]

## 7. Documentation

- [ ] Code comments: Adequate / Needs improvement
- [ ] README updates: Done / Not needed / Missing
- [ ] API documentation: Done / Not needed / Missing

## 8. Recommendations

### Before Merging
1. [Required action if any]

### Future Improvements
1. [Nice-to-have improvement]
2. [Technical debt to address later]

## 9. Final Verdict

**Status**: APPROVED FOR MERGE

[Or if issues found:]

**Status**: NEEDS CHANGES

Required changes before approval:
1. [Change 1]
2. [Change 2]

---

## Sign-off

- [x] Code review complete
- [x] Tests passing
- [x] No critical issues found
- [x] Ready for deployment
```

### 5. Output Summary

After completing review:

```
## Review Complete

**Status**: [APPROVED / NEEDS CHANGES]

### Summary
- Files reviewed: [count]
- Issues found: [count]
- Critical: [count]

### Next Steps
[What should happen next]

Full report: [path to review-report.md]
```

---

## Mandatory Agent Delegation for Review

**CRITICAL**: Use specialized agents for comprehensive review:

| Review Area | Agent to Use | What They Review |
|-------------|--------------|------------------|
| Code Quality | `refactoring-expert` | Clean code, SOLID, maintainability |
| Angular Code | `angular-expert` | Angular 21+ best practices, signals, patterns |
| Next.js Code | `nextjs-expert` | Next.js 15+ best practices, App Router patterns |
| Security | `security-engineer` | Vulnerabilities, OWASP compliance |
| Performance | `performance-engineer` | Bottlenecks, optimization opportunities |
| Testing | `quality-engineer` | Test coverage, edge cases |
| Architecture | `system-architect` | Design patterns, scalability |
| Root Cause | `root-cause-analyst` | Any issues found during review |
| E-commerce Code | `ecommerce-marketing-expert` | Conversion best practices, UX optimization |
| Legal Compliance | `ecommerce-legal-expert` | Terms of service, GDPR, legal notices, regulatory compliance |

**Review Process**:
1. Delegate code review to `refactoring-expert`
2. Security review to `security-engineer`
3. Performance review to `performance-engineer`
4. Test review to `quality-engineer`
5. Compile all findings into the review report

---

## French Language Rule
- **Mandatory accents**: Always use correct accents on French words (é, è, ê, ë, à, â, ù, û, ô, î, ï, ç)
- **Critical examples**: Sélection, Créer, Prénom, Téléphone, Séance, Précédent, Création, créé, succès, trouvé, envoyé, étape
- **Verification**: Before finalizing any task, verify that all French text has correct accents
- **No exceptions**: Encoding or keyboard issues do not justify omitting accents

---

## Task directory (optional):
$ARGUMENTS
