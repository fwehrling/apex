# APEX

**Analyze, Plan, Execute, Examine**

A structured 4-phase development workflow for [Claude Code](https://docs.anthropic.com/en/docs/claude-code). APEX guides implementation through systematic analysis, planning with user validation, disciplined execution, and thorough review.

```
/apex "Add user authentication with JWT"
```

---

## How It Works

APEX splits every feature implementation into 4 sequential phases. Each phase produces a persistent artifact that feeds into the next, creating a traceable decision trail.

```
  ANALYZE          PLAN            EXECUTE          EXAMINE
 ┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐
 │ Explore  │──▶│ Design   │──▶│ Build    │──▶│ Review   │
 │ codebase │   │ strategy │   │ feature  │   │ quality  │
 └──────────┘   └──────────┘   └──────────┘   └──────────┘
       │              │              │              │
  analysis.md   impl-plan.md   impl-notes.md  review-report.md
```

**Phase 1 (Analyze)** explores the codebase with parallel agents to understand architecture, find similar features, and identify integration points.

**Phase 2 (Plan)** produces a detailed implementation plan with phased steps, component specs, and open questions. **Stops for user approval before proceeding.**

**Phase 3 (Execute)** implements the approved plan step by step, tracking progress, deviations, and decisions in real time.

**Phase 4 (Examine)** performs a comprehensive code review covering correctness, quality, security, and performance.

### Standalone Phases

Each phase can also be invoked independently:

```
/apex-1-analyze "feature description"    # Deep analysis only
/apex-2-plan                             # Plan from existing analysis
/apex-3-implement                        # Execute approved plan
/apex-4-review                           # Review completed work
```

---

## Features

### Agent Delegation

Each phase instructs Claude to delegate domain-specific work to specialized agents via the Task tool. These agents are **not included in APEX** -- they are Claude Code's built-in subagent types (e.g. `angular-expert`, `nextjs-expert`) or general-purpose agents prompted with a specific role (e.g. `backend-architect`, `security-engineer`).

APEX tells Claude *when* and *how* to delegate. The agents themselves are part of Claude Code.

### Persistent Artifacts

Every phase writes its output to a task directory under `.claude/tasks/` (or `tasks/`), creating a traceable record:

```
.claude/tasks/
  01-user-auth/
    analysis.md           # Phase 1 output
    implementation-plan.md # Phase 2 output
    implementation-notes.md # Phase 3 output
    review-report.md       # Phase 4 output
```

### Human-in-the-Loop

Phase 2 (Plan) always stops for user approval. Open questions are presented with options and recommendations. No code is written until the plan is validated.

---

## Installation

```bash
# Clone the repo and copy skills into your project
git clone https://github.com/fwehrling/apex.git /tmp/apex
cp -r /tmp/apex/skills/apex* /path/to/your/project/.claude/skills/
```

---

## Commands

| Command | Phase | Output | Description |
|---------|-------|--------|-------------|
| `/apex` | All 4 | Full workflow | Run the complete APEX cycle |
| `/apex-1-analyze` | Analyze | `analysis.md` | Deep codebase exploration |
| `/apex-2-plan` | Plan | `implementation-plan.md` | Implementation strategy |
| `/apex-3-implement` | Execute | `implementation-notes.md` | Build the feature |
| `/apex-4-review` | Examine | `review-report.md` | Quality audit |

---

## Project Structure

```
apex/
  skills/
    apex/                    # Main APEX skill (all 4 phases)
      SKILL.md
    apex-1-analyze/          # Phase 1: Analyze
      SKILL.md
    apex-2-plan/             # Phase 2: Plan
      SKILL.md
    apex-3-implement/        # Phase 3: Execute
      SKILL.md
    apex-4-review/           # Phase 4: Examine
      SKILL.md
  README.md
  LICENSE
```

---

## Requirements

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) CLI

---

## License

MIT License. See [LICENSE](LICENSE).

---

*Built for Claude Code. Structured development, every time.*
