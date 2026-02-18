
# APEX Files - Step 3: IMPLEMENT

You are implementing a feature based on an approved plan.

## Prerequisites

1. Locate the task directory
2. Read `analysis.md` for context
3. Read `implementation-plan.md` for the approved plan

**Do NOT proceed if the plan wasn't approved. Ask for confirmation first.**

## Instructions

### 1. Load Context

Read both files to fully understand:
- What we're building (from analysis)
- How we're building it (from plan)
- The specific steps to follow

### 2. Execute Implementation

Follow the plan phases in order:

For each step:
1. Announce what you're implementing
2. Implement the code
3. Run linters/type-check after each file
4. Mark step as complete

### 3. Track Progress

Create/update `implementation-notes.md` as you work:

```markdown
# Implementation Notes: [Feature Name]

## Date Started: [Date]
## Status: In Progress / Complete

## Progress Tracker

### Phase 1: [Name]
- [x] Step 1.1: [Description] - Complete
- [x] Step 1.2: [Description] - Complete
- [ ] Step 1.3: [Description] - In Progress

### Phase 2: [Name]
- [ ] Step 2.1: [Description] - Pending

## Decisions Made During Implementation

| Decision | What I Did | Why |
|----------|-----------|-----|
| [Situation] | [Choice] | [Reasoning] |

## Deviations from Plan

### Deviation 1
**Original Plan**: [What was planned]
**What I Did**: [What actually happened]
**Reason**: [Why the change]

## Issues Encountered

### Issue 1
**Problem**: [Description]
**Solution**: [How it was resolved]

## Files Modified/Created

| File | Action | Status |
|------|--------|--------|
| path/to/file | Created | Done |
| path/to/file | Modified | Done |

## Commands Run
- `pnpm lint` - Passed
- `pnpm typecheck` - Passed
- `pnpm test` - Passed

## Notes for Review Phase
[Anything the reviewer should pay attention to]
```

### 4. Completion

After finishing all steps:
- Run full linter check
- Run type check if applicable
- Run tests if they exist
- Update implementation-notes.md with final status

Output:
- Implementation complete
- Notes: [path to implementation-notes.md]
- Ready for Step 4 (review)

---

## Mandatory Agent Delegation for Implementation

**CRITICAL**: Use specialized agents during implementation for quality code.

### Native Agents (use directly as `subagent_type`)

| Implementation Task | subagent_type | Purpose |
|---------------------|---------------|---------|
| Angular Code | `angular-expert` | Angular 21+ implementation, signals, standalone |
| Next.js Code | `nextjs-expert` | Next.js 15+ implementation, Server Components |
| E-commerce Code | `ecommerce-marketing-expert` | Cart, checkout, product pages, conversion elements |
| Legal Compliance | `ecommerce-legal-expert` | Legal notices, terms of service, cookies, GDPR |

### Role-Based Agents (use `subagent_type="general-purpose"` with role prompt)

| Implementation Task | Role Prompt Prefix | Purpose |
|---------------------|--------------------|---------|
| Backend Code | "You are a senior backend architect." | API implementation, database operations |
| Frontend Code | "You are a senior frontend architect." | UI components, accessibility |
| Python Code | "You are a Python expert." | Production-ready Python with tests |
| Refactoring | "You are a refactoring expert." | Clean code, SOLID principles |
| Security | "You are a security engineer." | Security validation, input sanitization |

**During Implementation**:
- For complex code sections, delegate to the appropriate specialist agent
- Have agents review critical code paths
- Use `general-purpose` with "You are a QA engineer." for test creation
- Use `general-purpose` with "You are a security engineer." for security-sensitive code

**Agent Teams Acceleration**:
When `CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1` is set and implementation involves 2+ independent modules:
- Create a team with `TeamCreate`, spawn specialist teammates in parallel
- Each teammate gets: role + implementation plan section + file scope (strict ownership, no overlap)
- Teammates implement their module and report completion via shared task list
- Lead integrates results and runs cross-module validation
- Falls back to sequential subagents if Agent Teams is unavailable

---

## French Language Rule
- **Mandatory accents**: Always use correct accents on French words (é, è, ê, ë, à, â, ù, û, ô, î, ï, ç)
- **Critical examples**: Sélection, Créer, Prénom, Téléphone, Séance, Précédent, Création, créé, succès, trouvé, envoyé, étape
- **Verification**: Before finalizing any task, verify that all French text has correct accents
- **No exceptions**: Encoding or keyboard issues do not justify omitting accents

---

## Task directory (optional):
$ARGUMENTS
