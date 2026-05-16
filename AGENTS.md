# UNITERA — AGENTS.md

## Status
Repository root guidance for planning und implementation.

This file defines how agents work in this repository while the project is in **design, implementation, and verification mode**.

The purpose is to deepen UNITERA strategy, naming, governance, evidence, outreach logic, and the related implementation surfaces in a controlled way.

---

## 1. Core Identity

UNITERA is a governance-first AI operating layer for governed business workflows.

The strategic frame is:

- Platform layer: `UNITERA`
- System layer / control surface: `uniCommit`
- First workflow wedge: `OfferFlow`
- Runtime authority: `Commitment Core`

Agents must preserve this distinction.

Product labels may guide planning language, but they must not create Domain, API, route, schema, lifecycle, or runtime authority.

---

## 2. Implementation Mode

Implementation mode means:

Allowed:

- read repository files
- summarize findings
- create planning notes
- create wiki entries
- append diary/log entries
- create decision-prep matrices
- classify open questions
- document conversations and strategic reasoning

Not allowed:

- edit runtime code
- edit API, DB, schema, package, route, or deployment behavior
- rename Domain objects
- add productized modules
- add integrations
- introduce `/unicommit` or `/offerflow` runtime routes
- convert planning language into implementation truth
- claim compliance, certification, production-readiness, integration proof, customer proof, or ROI evidence without runtime-backed evidence

Implementation work must still stay scoped, evidence-based, and reviewable. When a task is risky or touches shared surfaces, prefer a small patch plus verification instead of broad refactors.

---

## 3. Source Authority

Agents must distinguish authority levels before writing anything.

Authority classes:

- `canonical`: current repository source of truth
- `proposed_import`: strategy or prompt logic not yet accepted as repo truth
- `working_note`: exploratory planning note
- `wiki_entry`: structured thought record
- `diary_log`: chronological discussion / reasoning record
- `legacy_contained`: historical content, not active authority
- `unknown`: unresolved or not yet classified

Rules:

- Canonical files override working notes.
- Proposed imports must be labeled until accepted.
- Wiki/log entries do not create runtime truth.
- Evidence registers describe observed proof; they do not replace runtime tests or code.
- If authority conflicts, mark the conflict and stop.

---

## 4. Planning Boundaries

Agents must keep these separations explicit:

- Governance Core ≠ vertical workflow module
- Runtime state ≠ response surface
- Evidence ≠ business state
- Audit record ≠ compliance certification
- UI language ≠ technical truth
- GTM wedge ≠ platform architecture
- Operator diagnosis ≠ second source of truth
- Planning note ≠ approved implementation

---

## 5. Wiki / Diary Discipline

The repository may use a `wiki/` or `docs/wiki/` space for structured thinking.

Route reference for chat-triggered memory planning:
- `wiki/strategy/chat-trigger-map-memory-logic.md` (planning authority for trigger syntax and recording flow)

Wiki entries should capture:

- question or tension
- current understanding
- relevant sources
- open decisions
- rejected readings
- implications
- next meta-planning step

Diary/log entries should capture:

- date/time
- conversation trigger
- what changed in understanding
- what remains unresolved
- what must not be inferred

Do not rewrite historical diary entries. Add new dated entries instead.

---

## 6. Agent Output Requirements

Every non-trivial agent response should include:

- scope
- source basis
- findings or proposed framing
- open questions
- risk of overclaiming
- next smallest step

Do not state that a decision is final unless a canonical file or explicit human decision makes it final.

---

## 7. Red Lines

Agents must not:

- make hidden implementation decisions
- turn a strategy discussion into repo changes
- treat synthetic demo assets as customer proof
- treat outreach responses as product validation
- treat `OfferFlow` as platform name
- treat `uniCommit` as runtime authority
- treat future workflow families as released modules
- use marketing language as architecture truth

---

## 8. Definition of Done

An implementation-aware planning task is complete only when:

1. Sources are classified by authority.
2. Findings stay inside planning / wiki / diary scope.
3. Runtime, API, Domain, DB, route, and package behavior are intentionally changed only when the task requires it.
4. Open questions are explicitly marked.
5. Claims are bounded by evidence.
6. A next step, verification note, or handoff prompt is provided.

---

End of AGENTS.md
