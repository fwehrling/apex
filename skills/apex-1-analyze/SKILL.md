
# APEX Files - Step 1: ANALYZE

You are performing deep analysis for a complex feature. This analysis will be saved to a file for use in subsequent steps.

## Instructions

### 1. Create Task Directory

First, check existing task directories in `.claude/tasks/` or `tasks/` (whichever exists in the project, or create `.claude/tasks/` if neither exists).

Create a new numbered directory:
- Check the highest existing number (e.g., `01-feature-name`, `02-other-feature`)
- Create the next number with a descriptive name
- Example: `03-unsubscribe-page-builder`

### 2. Launch Parallel Exploration

Use subagents to explore these areas simultaneously:

**Agent 1: Architecture Analysis**
- Overall project structure
- Relevant modules and their responsibilities
- Data flow patterns

**Agent 2: Similar Features**
- Find similar implementations in the codebase
- Identify reusable components
- Note patterns to follow

**Agent 3: Integration Points**
- APIs and services involved
- Database schemas if relevant
- External dependencies

### 3. Create Analysis File

Create `analysis.md` in the task directory with this structure:

```markdown
# Feature Analysis: [Feature Name]

## Date: [Current Date]

## 1. Executive Summary
[2-3 sentences describing what we're building and the main challenges]

## 2. Current State Analysis

### 2.1 Relevant Architecture
[Describe the parts of the codebase that relate to this feature]

### 2.2 Existing Similar Features
[List similar features with file paths]
- Feature A: `path/to/files`
- Feature B: `path/to/files`

### 2.3 Reusable Components
| Component | Location | Can Reuse? | Notes |
|-----------|----------|------------|-------|
| ComponentX | path/to/file | Yes/Partial/No | Notes |

## 3. Key Files Identified

### 3.1 Files to Modify
- `path/to/file1.ts` - Reason
- `path/to/file2.ts` - Reason

### 3.2 Files to Create
- `path/to/new-file.ts` - Purpose

### 3.3 Reference Files (read-only, for patterns)
- `path/to/reference.ts` - What pattern to follow

## 4. Technical Considerations

### 4.1 Dependencies
[List dependencies that will be used or added]

### 4.2 Database/Schema Changes
[If applicable]

### 4.3 API Changes
[If applicable]

## 5. Risks and Challenges
1. [Risk 1 and mitigation]
2. [Risk 2 and mitigation]

## 6. Questions for Clarification
1. [Question that needs human input]
2. [Question that needs human input]

## 7. Recommended Next Steps
[What should happen in the PLAN phase]
```

### 4. Confirm Completion

After creating the file, output:
- Analysis complete
- Task directory: [path]
- Analysis file: [path]
- Questions requiring input: [count]

---

## Mandatory Agent Delegation for Analysis

**CRITICAL**: You MUST use specialized agents for thorough analysis. Launch them in parallel using the Task tool.

### Native Agents (use directly as `subagent_type`)

| Analysis Area | subagent_type | Purpose |
|---------------|---------------|---------|
| Angular Apps | `angular-expert` | Angular 21+, signals, standalone components, control flow |
| Next.js Apps | `nextjs-expert` | Next.js 15+, App Router, Server Components, Server Actions |
| E-commerce Apps | `ecommerce-marketing-expert` | Conversion optimization, UX, marketing strategy |
| E-commerce Legal | `ecommerce-legal-expert` | Terms of service, GDPR, legal notices, compliance |

### Role-Based Agents (use `subagent_type="general-purpose"` with role prompt)

| Analysis Area | Role Prompt Prefix | Purpose |
|---------------|--------------------|---------|
| Backend | "You are a senior backend architect." | API patterns, database design, server architecture |
| Frontend | "You are a senior frontend architect." | UI patterns, accessibility, component structure |
| System Design | "You are a system architect." | Architecture, scalability, dependencies |
| Security | "You are a security engineer." | Security implications, vulnerabilities |
| Performance | "You are a performance engineer." | Performance considerations, bottlenecks |
| Requirements | "You are a requirements analyst." | Scope clarification, user stories |

**Agent Teams Acceleration**:
When `CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1` is set and 2+ agents are needed, use Agent Teams instead of subagents for true parallel execution:
- Create a team with `TeamCreate`
- Spawn each analysis agent as a teammate with a self-sufficient prompt (role + task + file scope)
- Teammates communicate results via the shared task list
- Collect all outputs and integrate into `analysis.md`

If Agent Teams is unavailable, fall back to parallel Task tool calls (subagents).

**Example Parallel Launch (subagents)**:
```
Use Task tool with subagent_type="angular-expert" for Angular analysis
Use Task tool with subagent_type="general-purpose", prompt="You are a senior backend architect. Analyze..." for API analysis
Use Task tool with subagent_type="general-purpose", prompt="You are a system architect. Review..." for architecture review
```

Integrate all agent outputs into the final `analysis.md`.

---

## French Language Rule
- **Mandatory accents**: Always use correct accents on French words (é, è, ê, ë, à, â, ù, û, ô, î, ï, ç)
- **Critical examples**: Sélection, Créer, Prénom, Téléphone, Séance, Précédent, Création, créé, succès, trouvé, envoyé, étape
- **Verification**: Before finalizing any task, verify that all French text has correct accents
- **No exceptions**: Encoding or keyboard issues do not justify omitting accents

---

## Feature to analyze:
$ARGUMENTS
