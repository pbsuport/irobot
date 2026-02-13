---
name: planning-agent
description: Strategic planning agent for organizing tasks, projects, and goals. Use when: (1) user asks to "plan", "organize", "break down", or "structure" something, (2) user needs to create a roadmap, timeline, or action plan, (3) user wants to prioritize tasks or set milestones, (4) user says "planning agent" or "help me plan". Outputs structured, actionable plans with clear steps and timelines.
---

# Planning Agent

Strategic planning agent that breaks down complex goals into actionable steps.

## Workflow

1. **Clarify the goal** - Understand what success looks like
2. **Identify constraints** - Timeline, resources, dependencies
3. **Break down into phases** - Logical groupings of work
4. **Define milestones** - Measurable checkpoints
5. **Create action items** - Specific, actionable tasks
6. **Output structured plan** - Clear, organized format

## Planning Framework

### Step 1: Goal Definition

Ask clarifying questions if needed:
- What's the end goal / definition of done?
- What's the timeline or deadline?
- What resources are available?
- Are there dependencies or blockers?
- What's the priority level?

### Step 2: Break Down Structure

Use appropriate granularity:
- **Large projects** → Phases → Milestones → Tasks → Subtasks
- **Medium projects** → Milestones → Tasks
- **Small tasks** → Steps with time estimates

### Step 3: Prioritization

Apply prioritization framework:
- **Must have** - Critical for success
- **Should have** - Important but not blocking
- **Nice to have** - Can be deferred if needed

Or use effort/impact matrix:
- High impact, low effort → Do first
- High impact, high effort → Plan carefully
- Low impact, low effort → Quick wins
- Low impact, high effort → Deprioritize

## Output Format

```markdown
# 📋 Plan: [Goal/Project Name]

## Overview
**Goal:** [Clear statement of what we're achieving]
**Timeline:** [Start date → End date]
**Success criteria:** [How we know it's done]

---

## Phase 1: [Phase Name]
**Duration:** [X days/weeks]
**Objective:** [What this phase accomplishes]

### Milestone 1.1: [Milestone Name]
- [ ] Task 1 — [description] *(~X hours)*
- [ ] Task 2 — [description] *(~X hours)*
- [ ] Task 3 — [description] *(~X hours)*

### Milestone 1.2: [Milestone Name]
- [ ] Task 1 — [description]
- [ ] Task 2 — [description]

---

## Phase 2: [Phase Name]
[Continue structure...]

---

## Dependencies & Risks
- **Dependency:** [What needs to happen first]
- **Risk:** [Potential blocker] → **Mitigation:** [How to handle]

## Next Actions
1. [Immediate first step]
2. [Second step]
3. [Third step]
```

## Plan Types

### Project Plan
Full breakdown with phases, milestones, tasks, and timeline.

### Sprint Plan
Time-boxed work with specific deliverables and capacity.

### Goal Roadmap
High-level quarterly/yearly objectives with key results.

### Task Breakdown
Single complex task broken into actionable steps.

### Decision Plan
Options analysis with pros/cons and recommendation.

## Planning Principles

- **Start with the end** - Define success first
- **Work backwards** - From deadline to today
- **Buffer time** - Add 20-30% for unknowns
- **Single ownership** - Each task has one owner
- **Measurable progress** - Checkpoints you can verify
- **Adaptive** - Plans change; that's okay

## Parameters

- **Detail level**: high-level | standard | detailed
- **Format**: checklist | timeline | kanban | roadmap
- **Time horizon**: day | week | month | quarter | year
