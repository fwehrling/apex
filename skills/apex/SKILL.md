
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

**CRITICAL**: For each phase, you MUST delegate to the appropriate specialized agent(s) using the Task tool.

### Native Agents (use directly as `subagent_type`)

| Domain | subagent_type | When to Use |
|--------|---------------|-------------|
| Angular | `angular-expert` | Angular 21+, signals, standalone components, control flow |
| Next.js | `nextjs-expert` | Next.js 15+, App Router, Server Components, Server Actions |
| E-commerce | `ecommerce-marketing-expert` | Conversion, UX, marketing, payments, SEO |
| E-commerce Legal | `ecommerce-legal-expert` | Terms of service, GDPR, legal notices, compliance |

### Role-Based Agents (use `subagent_type="general-purpose"` with role prompt)

For these domains, use `general-purpose` and start the Task prompt with the role description:

| Domain | Role Prompt Prefix | Focus |
|--------|--------------------|-------|
| Backend/API | "You are a senior backend architect." | API design, database, server-side logic |
| Frontend/UI | "You are a senior frontend architect." | UI components, accessibility, responsive design |
| Security | "You are a security engineer." | Vulnerability assessment, auth, compliance |
| Performance | "You are a performance engineer." | Optimization, bottlenecks, metrics |
| Testing | "You are a QA engineer." | Test strategy, edge cases, coverage |
| Code Quality | "You are a refactoring expert." | Technical debt, SOLID principles, clean code |
| System Design | "You are a system architect." | Architecture decisions, scalability |
| DevOps | "You are a DevOps engineer." | CI/CD, deployment, infrastructure |
| Python | "You are a Python expert." | Python-specific implementation |
| Documentation | "You are a technical writer." | API docs, user guides, specifications |
| Requirements | "You are a requirements analyst." | PRD, user stories, scope definition |
| Debugging | "You are a root cause analyst." | Complex debugging, investigation |

**Delegation Process**:
1. Identify which domains the feature touches
2. For native agents: launch with `subagent_type` directly
3. For role-based agents: launch with `subagent_type="general-purpose"` and include the role prompt prefix
4. Integrate their outputs into your analysis/plan
5. For complex features, use multiple agents in parallel

---

## French Language Rule
- **Mandatory accents**: Always use correct accents on French words (é, è, ê, ë, à, â, ù, û, ô, î, ï, ç)
- **Critical examples**: Sélection, Créer, Prénom, Téléphone, Séance, Précédent, Création, créé, succès, trouvé, envoyé, étape
- **Verification**: Before finalizing any task, verify that all French text has correct accents
- **No exceptions**: Encoding or keyboard issues do not justify omitting accents

---

## Feature to implement:
$ARGUMENTS
