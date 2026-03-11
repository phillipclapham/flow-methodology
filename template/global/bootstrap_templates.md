# Project Bootstrap Templates

> On-demand file — loaded when "init project" is called.
> Partnership protocol loads from global ~/.claude/CLAUDE.md — these templates capture project-specific context.

---

### projectbrief.md Template

```markdown
# [PROJECT NAME]

> [One-line purpose]

## Why This Matters

[What's at stake if this project succeeds? What's lost if it fails?]
[This is PROJECT-specific stakes - personal/partnership stakes are in global CLAUDE.md]

## Core Function

[2-3 sentences: What does this project DO? What problem does it solve?]

## Success Criteria

- [ ] [Primary deliverable]
- [ ] [Secondary deliverable]
- [ ] [Definition of "done"]

## Technical Context

**Stack:** [Languages, frameworks, key dependencies]
**Architecture:** [Brief description or "TBD - will emerge"]

## Constraints

- [Time, scope, or technical constraints]
- [Non-negotiables]

---

*Keep this file under 250 lines. Essence only.*
```

### ROADMAP.md Template

```markdown
# Roadmap

> Strategic plan and phase overview for [PROJECT NAME].

## Vision

[TBD - Refine in Session 1: Project Planning]

---

## Phases

### Phase 1: [NAME]
**Goal:** [TBD]
**Deliverables:** To be defined in Session 1

### Phase 2: [NAME]
**Goal:** [TBD]
**Deliverables:** To be defined in Session 1

### Phase 3: [NAME]
**Goal:** [TBD]
**Deliverables:** To be defined in Session 1

---

## Current Status

**Active Phase:** 0 - Bootstrap
**Progress:** Awaiting Session 1 planning

---

*Refine this document in Session 1. Update at phase boundaries thereafter.*
```

### next_steps.md Template

```markdown
# Next Steps

**Current Phase:** Phase 0 - Bootstrap (see ROADMAP.md)
**Updated:** [DATE]

---

## Session 1: Project Planning

**Status:** PENDING
**Date:** [DATE]

**Focus:** Define project vision and refine ROADMAP
**Goal:** Clear deliverables for Phase 1, Session 2 defined

**Planning agenda:**
- [ ] Discuss actual vision and features
- [ ] Refine ROADMAP with specific deliverables
- [ ] Define Phase 1 scope
- [ ] Set up Session 2 as first real work

---

## Completed

### Session 0: Project Bootstrap
- Initialized project_memory/ structure
- Captured stakes and phase skeleton
- Ready for planning discussion

---

*Active session tracker. Update after each session.*
```

### README.md Template

```markdown
# Project Memory

Navigation index for [PROJECT NAME].

## Commands

- "read project memory" - Load execution context (projectbrief + next_steps)
- "read full project memory" - Add orientation context (this file + ROADMAP + decisions)
- "update continuity" - End session, archive if complete

## Files

**Execution** (auto-loaded):
- `projectbrief.md` - Project essence + stakes
- `next_steps.md` - Active session tracker

**Orientation** (load with full):
- `README.md` - This navigation index
- `ROADMAP.md` - Strategic phases and milestones
- `decisions.md` - Technical decisions log

**Historical** (load explicitly):
- `COMPLETED_SESSIONS_ARCHIVE.md` - Session history (append-only)
- `historical/` - Archived specs and phase reports

---

*Navigation only. Status tracking belongs in next_steps.md.*
```

### decisions.md Template

```markdown
# Decisions Log

> Strategic and technical decisions with full context.
> Write here when: Choices that affect project direction, architecture, or approach.
> Reference when: Planning new work, stuck on something, questioning past choices.

---

## Graduated Principles

*Patterns validated 3x in continuity.md migrate here with full context.*

---

## Decision Log

*Newest first. Include: date, context, options considered, choice made, rationale.*

### [DATE]: [Decision Title]

**Context:** [What prompted this decision]

**Options considered:**
1. [Option A] - [pros/cons]
2. [Option B] - [pros/cons]

**Decision:** [What was chosen]

**Rationale:** [Why this option]

---

*Created [DATE] | Updated as decisions are made*
```

### COMPLETED_SESSIONS_ARCHIVE.md Template

```markdown
# Completed Sessions Archive

> Historical record of all session work. **Append-only, never auto-loaded.**
> Purpose: Timeline reconstruction, debugging reference, phase completion source.
> NOT part of any "read project memory" command - load explicitly when needed.
> Updated by: "update continuity" (full session completion only)

---

## Sessions

*Newest first. Each entry added during session completion or pause.*

### [DATE]: Session X - [Title]

**Status:** COMPLETED | CONTINUED in Xa | PAUSED (blocked by Xa)
**Duration:** ~[time]
**Commits:** [commit hashes or count]

**Accomplished:**
- [Key accomplishment 1]
- [Key accomplishment 2]

**Notes:** [Any important context]

---

*Created [DATE]*
```
