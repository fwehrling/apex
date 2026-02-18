
# APEX Files - Step 2: PLAN

You are creating a detailed implementation plan based on the previous analysis.

## Prerequisites

First, locate and read the `analysis.md` file from the task directory.

If no task directory is specified in the arguments, list available task directories and ask which one to use.

## Instructions

### 1. Read Analysis

- Read the `analysis.md` file thoroughly
- Understand all identified components and risks
- Review the questions that were raised

### 2. Create Implementation Plan

Create `implementation-plan.md` in the same task directory:

```markdown
# Implementation Plan: [Feature Name]

## Date: [Current Date]
## Based on: analysis.md

## 1. Implementation Strategy

### 1.1 High-Level Approach
[Describe the overall strategy in 3-5 sentences]

### 1.2 Architecture Decisions
| Decision | Choice | Rationale |
|----------|--------|-----------|
| [Decision point] | [What we'll do] | [Why] |

## 2. Implementation Phases

### Phase 1: [Foundation/Setup]
**Objective**: [What this phase accomplishes]
**Estimated Complexity**: Low/Medium/High

| Step | File | Action | Description |
|------|------|--------|-------------|
| 1.1 | path/to/file | Create | Description |
| 1.2 | path/to/file | Modify | Description |

### Phase 2: [Core Implementation]
**Objective**: [What this phase accomplishes]
**Estimated Complexity**: Low/Medium/High

| Step | File | Action | Description |
|------|------|--------|-------------|
| 2.1 | path/to/file | Create | Description |
| 2.2 | path/to/file | Modify | Description |

### Phase 3: [Integration/Polish]
**Objective**: [What this phase accomplishes]
**Estimated Complexity**: Low/Medium/High

| Step | File | Action | Description |
|------|------|--------|-------------|
| 3.1 | path/to/file | Modify | Description |
| 3.2 | path/to/file | Create | Description |

## 3. Component Specifications

### 3.1 [Component Name]
**File**: `path/to/component`
**Purpose**: [What it does]
**Props/Interface**:
```typescript
interface ComponentProps {
  // Define the interface
}
```
**Dependencies**: [What it imports/uses]

### 3.2 [Next Component]
[Same structure]

## 4. Data Flow

[Describe how data flows through the new feature]
[Can include ASCII diagram if helpful]

## 5. Testing Strategy

### 5.1 Unit Tests
- [ ] Test for [component/function]
- [ ] Test for [component/function]

### 5.2 Integration Tests
- [ ] Test for [flow]

### 5.3 Manual Testing Steps
1. [Step to verify]
2. [Step to verify]

## 6. Rollback Plan

If issues arise:
1. [How to revert]
2. [What to check]

## 7. Open Questions (Require Human Input)

1. **[Question]**
   - Option A: [Description]
   - Option B: [Description]
   - My recommendation: [Which and why]

2. **[Question]**
   - [Options and recommendation]

---

**AWAITING APPROVAL**

Please review this plan and:
1. Answer the open questions
2. Approve to proceed to implementation
3. Or request modifications

---
```

### 3. Present Plan Summary

After creating the file, output:
- Plan created: [path]
- Phases: [count]
- Steps: [total count]
- Questions requiring input: [count]
- Waiting for approval before Step 3 (implement)

---

## Mandatory Agent Delegation for Planning

**CRITICAL**: Consult specialized agents for each domain in the implementation plan:

| Plan Domain | Agent to Consult | What to Get |
|-------------|------------------|-------------|
| API Design | `backend-architect` | API structure, endpoints, error handling |
| UI Components | `frontend-architect` | Component specs, accessibility requirements |
| Angular Apps | `angular-expert` | Angular 21+ patterns, signals, standalone components |
| Next.js Apps | `nextjs-expert` | Next.js 15+ patterns, App Router, Server Components |
| Architecture | `system-architect` | Architecture decisions, patterns to follow |
| Testing | `quality-engineer` | Test strategy, edge cases, coverage requirements |
| Security | `security-engineer` | Security requirements, validation rules |
| Performance | `performance-engineer` | Performance targets, optimization strategies |
| E-commerce Apps | `ecommerce-marketing-expert` | Conversion strategy, UX patterns, marketing features |
| E-commerce Legal | `ecommerce-legal-expert` | Terms of service, GDPR, legal compliance, sole proprietorship obligations |

**Planning Process**:
1. Read the analysis.md
2. Identify domains involved in the feature
3. Launch appropriate agents to get detailed recommendations
4. Incorporate their expertise into the implementation plan

---

## French Language Rule
- **Mandatory accents**: Always use correct accents on French words (é, è, ê, ë, à, â, ù, û, ô, î, ï, ç)
- **Critical examples**: Sélection, Créer, Prénom, Téléphone, Séance, Précédent, Création, créé, succès, trouvé, envoyé, étape
- **Verification**: Before finalizing any task, verify that all French text has correct accents
- **No exceptions**: Encoding or keyboard issues do not justify omitting accents

---

## Task directory (optional, will auto-detect if not provided):
$ARGUMENTS
