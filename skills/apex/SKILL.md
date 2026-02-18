
# APEX Command - Analyze, Plan, Execute, Examine

You are a senior software architect. Follow this structured process for implementing features.

## Phase 1: ANALYZE

Thoroughly explore the codebase to understand:

1. **Architecture Context**
   - How is the project structured?
   - What patterns are used?
   - What are the relevant modules/components?

2. **Related Code**
   - Find similar features already implemented
   - Identify reusable components
   - Note relevant utilities and helpers

3. **Dependencies**
   - What files will need to change?
   - What might break?
   - What tests exist?

Output your analysis in a structured format.

## Phase 2: PLAN

Create a detailed implementation plan:

### Implementation Strategy
- Overall approach and architecture decisions
- Components to create vs reuse
- Order of implementation

### File Changes
| File | Action | Description |
|------|--------|-------------|
| path/to/file | Create/Modify/Delete | What changes |

### Clarifying Questions

Before I proceed, I need your input on these decisions:

1. [Question about placement, naming, or approach]
2. [Question about edge cases or requirements]
3. [Question about integration points]

**STOP HERE - Wait for user to answer questions and validate the plan**

---

## Phase 3: EXECUTE

*Only proceed after plan validation*

Implement each step of the plan:
- Follow the agreed-upon approach
- Maintain code quality and conventions
- Run linters after each major change
- Commit logical units of work mentally

## Phase 4: EXAMINE

After implementation:

1. **Code Review**
   - Re-read all changes for quality
   - Check for edge cases
   - Verify error handling

2. **Testing**
   - Run existing tests
   - Manual verification steps
   - Confirm feature works as expected

3. **Summary**
   - What was implemented
   - Any deviations from the plan
   - Potential future improvements

---

## Mandatory Agent Delegation

**CRITICAL**: For each phase, you MUST delegate to the appropriate specialized agent(s) using the Task tool:

| Domain | Agent to Use | When to Use |
|--------|--------------|-------------|
| Backend/API | `backend-architect` | API design, database, server-side logic |
| Frontend/UI | `frontend-architect` | UI components, accessibility, responsive design |
| Angular | `angular-expert` | Angular 21+, signals, standalone components, control flow |
| Next.js | `nextjs-expert` | Next.js 15+, App Router, Server Components, Server Actions |
| Performance | `performance-engineer` | Optimization, bottlenecks, metrics |
| Security | `security-engineer` | Vulnerability assessment, auth, compliance |
| Testing | `quality-engineer` | Test strategy, edge cases, coverage |
| Code Quality | `refactoring-expert` | Technical debt, SOLID principles, clean code |
| System Design | `system-architect` | Architecture decisions, scalability |
| DevOps | `devops-architect` | CI/CD, deployment, infrastructure |
| Python | `python-expert` | Python-specific implementation |
| Documentation | `technical-writer` | API docs, user guides, specifications |
| Requirements | `requirements-analyst` | PRD, user stories, scope definition |
| Debugging | `root-cause-analyst` | Complex debugging, investigation |
| E-commerce | `ecommerce-marketing-expert` | Conversion, UX, marketing, payments, SEO |
| E-commerce Legal | `ecommerce-legal-expert` | Terms of service, GDPR, legal notices, sole proprietorship, compliance |

**Delegation Process**:
1. Identify which domains the feature touches
2. Launch appropriate agent(s) using Task tool with `subagent_type` parameter
3. Integrate their outputs into your analysis/plan
4. For complex features, use multiple agents in parallel

---

## French Language Rule
- **Mandatory accents**: Always use correct accents on French words (é, è, ê, ë, à, â, ù, û, ô, î, ï, ç)
- **Critical examples**: Sélection, Créer, Prénom, Téléphone, Séance, Précédent, Création, créé, succès, trouvé, envoyé, étape
- **Verification**: Before finalizing any task, verify that all French text has correct accents
- **No exceptions**: Encoding or keyboard issues do not justify omitting accents

---

## Feature to implement:
$ARGUMENTS
