# Wrap Protocol

*Complete reference for session wrapping - FlowScript markers + procedure*
*Load this file when wrapping a session*

---

## FlowScript Markers for Encoding

**Essential markers for continuity.md Developing Knowledge and narrative compression.**

### State Markers (Active Threads)

#### `?` Question needing decision
```
? Redis vs Postgres for sessions
? Should we launch publicly or keep private
```

#### `thought:` Insight worth preserving
```
thought: Relations force explicit relationship definition
thought: Hybrid approach emerged naturally through use
```
Can add confidence prefix: `* thought:` (high confidence) or `~ thought:` (uncertain)

#### `✓` Completed / done
```
✓ Auth system implementation
✓ Documentation updated
```

#### `[blocked(reason, since)]` Waiting on dependency
**Required fields** - forces explicit tracking:
- `reason`: What blocks progress
- `since`: When block began (date)

```
[blocked(reason: "waiting on API keys", since: "Jan 10")] Deploy to staging
[blocked(reason: "needs design review", since: "Jan 8")] Feature implementation
```

#### `[parking(why, until)]` Not ready to process yet
**Recommended fields** (warning if missing, not error):
- `why`: Reason for parking
- `until`: When to revisit

```
[parking(why: "not needed until v2", until: "after MVP")] Browser extension
[parking(why: "requires research", until: "Phase 1 done")] Advanced feature
```

#### `[decided(rationale, on)]` Commitment made
**Required fields** - documents reasoning:
- `rationale`: Why this decision
- `on`: When decided (date)

```
[decided(rationale: "user feedback validates need", on: "Jan 10")] Ship minimal version
[decided(rationale: "simplicity wins", on: "Jan 8")] Use Postgres over Redis
```

#### `[exploring]` Investigating, not committed
```
[exploring] New architecture approach
[exploring(hypothesis: "might improve performance")] Caching layer
```

### Relationship Markers (Narrative)

#### `->` Leads to / causes / results in
```
auth bug -> login failures
complexity -> maintenance burden
```

#### `<-` Derives from / caused by
```
login failures <- auth bug
decision <- user feedback
```

#### `<->` Bidirectional / mutual influence
```
team size <-> project scope
performance <-> memory usage
```

#### `><[axis]` Tension / tradeoff
**Axis label REQUIRED** - forces precision on what's being traded:
```
speed ><[velocity vs maintainability] code quality
features ><[stability vs functionality] stability
cost ><[performance vs budget] performance
```
Cannot write bare `><` - must specify the axis of tension.

### Modifiers (Prefixes)

#### `!` Urgent
```
! ? Launch timing - need decision today
! [blocked(reason: "critical path", since: "Jan 10")] Deploy
```

#### `*` High confidence / proven
```
* thought: Evidence validates this works
* [decided(rationale: "proven through testing", on: "Jan 10")] Use this approach
```

#### `~` Low confidence / uncertain
```
~ thought: Not sure but maybe relevant
~ performance improvement (depends on conditions)
```

#### `++` Strong positive / emphatic (always prefix)
```
++ Love this direction
++ That analysis nailed it
```

### Quick Reference Table

| Marker | Meaning | Required Fields |
|--------|---------|-----------------|
| `?` | Question/decision | - |
| `thought:` | Insight | - |
| `✓` | Completed | - |
| `[blocked]` | Waiting on dependency | reason, since |
| `[parking]` | Not ready yet | why, until (recommended) |
| `[decided]` | Commitment made | rationale, on |
| `[exploring]` | Investigating | - |
| `->` | Leads to/causes | - |
| `<-` | Derives from | - |
| `<->` | Bidirectional | - |
| `><[axis]` | Tension/tradeoff | axis label |
| `!` | Urgent (prefix) | - |
| `*` | High confidence (prefix) | - |
| `~` | Uncertain (prefix) | - |
| `++` | Strong positive (prefix) | - |

---

## Wrap Procedure

**Command:** "update continuity" (or "wrap" conversationally)
**Full procedure:** See global CLAUDE.md Continuity Management section.

This file serves as **FlowScript encoding reference** loaded on-demand during wraps.

---

### PROCESS A: Wrap in Claude Code (Primary - 90% of use)

**Context:** Conversation happening in Claude Code.

#### STEP 0: Size Check

- Run: `wc -l ./global/continuity.md`
- If >500 lines: compress using Compression Guardrails (see below)
- Target: ~500 lines total (~12-13k tokens) — all sections counted

#### STEP 1: Parse Session

- Compress session to key developments (shape, not transcript)
- Identify new patterns for Developing Knowledge
- Extract validated observations

#### STEP 2: Execute Update

Follow global CLAUDE.md Continuity Management "Update Process" — mode-adaptive:
1. Current State → REPLACE
2. Action Items → update lifecycle markers
3. Top of Mind → update salience
4. Recent Context → REWRITE narrative
5. Developing Knowledge → add 1x, increment 2x, graduate 3x → Proven
6. Temporal cleanup → >7d stale developing → archive

**FLOW MODE ALSO:** FlowScript encode session insights using markers above.

#### STEP 3: Git Commit and Push

```bash
cd /path/to/your/flow-repo
git add global/continuity.md
git add WRAP_PROTOCOL.md  # if modified
git commit -m "Session wrap [date]: [brief description]"
git push
```

#### STEP 4: Confirm to User

```
Updated continuity:
- State: [focus summary]
- Context: [session type] → momentum rewritten
- Top of Mind: [added/removed items]
- Patterns: [new] | [incremented] | [graduated → destination]
- Status: ~[lines] lines, ~[tokens] tokens
```

---

## Critical Rules

### Temporal Architecture

**Update Operations per continuity.md section:**
- **Current State:** REPLACE completely each session
- **Action Items:** Update lifecycle markers
- **Top of Mind:** Update cognitive salience
- **Recent Context:** REWRITE narrative (prose, auto-compresses)
- **Developing Knowledge:** Add 1x, increment 2x, graduate 3x → Proven
- **Proven Knowledge:** Rarely touch (only when graduating from Developing)
- **Foundation:** Almost never (near-permanent truths)

### Temporal Cleanup

- **Developing >7 days stale** → archive (git has it)
- **Proven >30 days stale** → archive
- **Pattern at 3x** → graduate to Proven (extract + FlowScript compress)

### Philosophy

- Information has half-life (immediate → stable layers)
- FlowScript lifecycle tracks pattern validation (1x → 2x → 3x)
- Projects carry detail, continuity carries patterns
- Git is transcript (trust it, stop duplicating)

### Quality Standards

- FlowScript markers in Developing Knowledge (with dates)
- Prose (not FlowScript) in Recent Context narrative
- Specific observations (not generic)
- Proven patterns only (not speculation)

### Compression Discipline

**Temporal balance is critical.** Compression has known failure modes:
- **Recency bias:** Recent material feels more "important" because it's vivid. RESIST THIS.
- **Over-compression:** Stripping too much, losing meaning. Compress for density, not loss.
- **Proportional weight:** A breakthrough from 3 weeks ago matters as much as today's work.

**The rule:** Simple as possible, complex as needed. Compression is power — but loss is failure.

### Compression Guardrails (Research-Validated Feb 2026)

**Protection hierarchy — what to compress and what to protect:**

1. **Activation zone (`<activation>` — Partnership, State, Top of Mind, Recent):**
   - Partnership behavioral instructions are LOAD-BEARING. Causal chains (e.g., `constraint → ENABLES != PROTECTS → handle_cognitive_load`) RESIST compression — removing the WHY causes ~30% persona drift (Li et al. 2024).
   - State/Top of Mind: REPLACE each session (not compressed, overwritten).
   - Recent Context: REWRITE as prose narrative (auto-compresses through rewriting).
   - **Rule: Never reduce Partnership below its current behavioral instruction density.**

2. **Action Items (`<reference>`):**
   - Self-cleaning — tasks complete and get removed naturally.
   - Don't compress to make room; let lifecycle handle it.

3. **Developing Knowledge (`<reference>`):**
   - Primary compression target via temporal cleanup (>7d → archive).
   - Format-compress via FlowScript density, not content removal.

4. **Proven / Foundation (`<knowledge>`):**
   - Rarely touch. Only when graduating from Developing.

**Compression order (when over limit):**
1. Temporal cleanup first (archive stale Developing >7d)
2. Format improvements (denser FlowScript, compressed notation)
3. Content reduction LAST RESORT — and never from activation zone

**Safe reduction range: 28-43% max.** Beyond this risks functional loss. v2.0 at 70% failed catastrophically — Claude instances couldn't activate correct behavior. Format improvements > content reduction.

**This file is a cognitive prosthetic, not a document.** Apply medical device standard: reliability > optimization, redundancy > efficiency.

---

## File Size Guidelines

**continuity.md:**
- **Target: ~500 lines total (~12-13k tokens) — all sections counted, no exclusions**
- **Warning: >500 lines — compress using guardrails above**

---

*v1.1 - Feb 18, 2026 — Added compression guardrails from v2.0-v2.2 research*
*Self-contained wrap reference with FlowScript markers*
*For complete FlowScript language spec: github.com/phillipclapham/flowscript*
