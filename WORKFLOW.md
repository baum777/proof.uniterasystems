# UNITERA Planning and Implementation Workflow

## Status

Workflow for strategy planning, wiki documentation, and diary-style logging.

This workflow supports planning, implementation, and verification with respect to runtime, API, Domain, DB, schema, routes, packages, deployment, and product surfaces.

---

## 1. Work Cycle

Every planning task follows:

```text
READ -> CLASSIFY -> SYNTHESIZE -> RECORD -> REVIEW -> NEXT
```

Implementation is allowed when the task requires it, but the change should stay scoped and verifiable.

---

## 2. READ

Collect the relevant inputs:

- canonical repo files
- `wiki/strategy/chat-trigger-map-memory-logic.md` for chat-trigger route rules
- proposed strategy imports
- prior conversation summaries
- wiki entries
- diary logs
- evidence registers
- landing / outreach artifacts

Do not infer authority from proximity. A file is not canonical merely because it exists.

---

## 3. CLASSIFY

Classify every source as one of:

- `canonical`
- `proposed_import`
- `working_note`
- `wiki_entry`
- `diary_log`
- `evidence_register`
- `legacy_contained`
- `unknown`

Also classify the layer:

- Platform
- System Layer
- Workflow Module
- Domain
- API / Contract
- Runtime State
- Evidence / Audit
- UI / Surface
- GTM / Outreach
- Diary / Wiki

---

## 4. SYNTHESIZE

Create a planning result or an implementation-ready result, depending on the task.

A good synthesis states:

- what is observed
- what is settled
- what is only proposed
- what is in tension
- what cannot be inferred
- which boundary must remain stable

Avoid:

- code-level design
- migration plans
- runtime routes
- schema proposals
- uncontrolled implementation tasks
- product expansion claims

---

## 5. RECORD

Record the result in the appropriate place.

### Wiki entry template

```markdown
# [Topic]

## Status
working_note | decision_prep | accepted_context | superseded

## Question
What is being clarified?

## Source basis
- [source]: authority class

## Current understanding
Short synthesis.

## Boundaries
What must not be inferred?

## Open decisions
- ...

## Next meta-planning step
- ...
```

### Diary log template

```markdown
# YYYY-MM-DD

## Entry: [short title]

### Trigger
What prompted the discussion?

### What changed in understanding
What became clearer?

### What stayed open
What is unresolved?

### What must not be inferred
What would be overclaiming?

### Next step
What should be planned, documented, or implemented next?
```

Diary entries are append-only. Do not rewrite previous entries except to add a correction note.

---

## 6. REVIEW

Before closing a planning task, ask:

- Did we preserve platform / system / workflow / runtime boundaries?
- Did we avoid turning product labels into runtime truth?
- Did we distinguish evidence from proof?
- Did we avoid implementation design?
- Did we mark unresolved authority conflicts?
- Did the diary/log capture the reasoning without overclaiming?

---

## 7. NEXT

Close with one next step:

Examples:

- create a wiki index
- write a decision-prep matrix
- classify an imported strategy file
- review a claim boundary
- summarize an outreach insight
- prepare an implementation prompt without executing it

Do not chain into implementation automatically without confirming scope.

---

## 8. Governance Rules

### Boundary Rules

- UNITERA remains platform language.
- uniCommit remains system-layer / control-surface language.
- OfferFlow remains a workflow wedge.
- Commitment Core remains runtime authority.
- Domain/API stay commitment-based.
- Synthetic demo assets remain synthetic.
- Outreach remains problem validation until evidence says otherwise.

### Evidence Rules

Planning evidence can support reasoning.

It cannot alone establish:

- runtime behavior
- customer proof
- certification
- integration proof
- production readiness
- legal compliance
- ROI

### Change Rules

Allowed file changes in this mode:

- wiki entries
- diary log entries
- planning notes
- decision-prep matrices
- implementation code when requested

Disallowed file changes in this mode:

- hidden or undocumented behavior changes

---

## 9. Definition of Done

A planning cycle is complete when:

1. Source authority is stated.
2. Layer boundaries are explicit.
3. Findings are recorded in wiki or log.
4. Open decisions are listed.
5. Overclaiming risks are marked.
6. No implementation was performed.
7. The next step stays scoped or is handed off as a separate implementation prompt.

---

End of WORKFLOW.md
