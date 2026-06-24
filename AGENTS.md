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
- nächster Checkpoint oder Arbeitsblock (nur wenn relevant: bei Risiko, Entscheidung oder Abschluss — kein automatischer Schritt nach jedem Pass)

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

<!-- workspace-root-sync:agents:start -->
## Workspace Root Integration

Class: repo-local agent frontdoor extension.
Use rule: read after this repository's own opening instructions. The workspace root `README.md` and `AGENTS.md` route entry, authority checks, reusable-surface checks, evidence, and stop rules; this repository's local files remain the canonical source for repo-specific product, runtime, archive, contract, and implementation truth.

### Authority And Scope

- Repo-local `AGENTS.md`, `README.md`, `docs/`, manifests, contracts, validators, tests, and workflow files govern this repository.
- Workspace-root files provide routing and constraints only; they do not replace repo-local architecture, implementation, product, runtime, or archive truth.
- Portfolio surfaces may classify, coordinate, or record cross-repo work, but they do not override this repository unless this repository explicitly adopts them.
- Shared-core assets under `model-agnostic-workflow-system/` are the reusable authority for portable skills, contracts, templates, validators, provider exports, and workflow routing patterns.
- For non-trivial, cross-repo, governance-related, reusable, prompt/system-prompt, validator, template, skill, or workflow/path-routing work, check existing repo-local and shared-core assets before creating a new surface.

### Entry Sequence

1. When entering from `/home/baum/Schreibtisch/workspace/main_projects`, read the root `README.md` and root `AGENTS.md` first.
2. Read this repository's frontdoors next: `AGENTS.md`, `README.md`, relevant `docs/`, manifests, contracts, validators, tests, and local workflow files.
3. Identify owner, scope, canonical file, expected write targets, dirty/user-made changes, validation path, and next gate before editing.
4. Prefer existing repo-local or shared-core scripts, templates, validators, contracts, and docs over new files.
5. Apply the smallest safe change.
6. Verify by reading changed state and running the relevant local checks.
7. Report results with exact paths, evidence, unresolved gaps, and next gate.

### TTD-first / TDD-inside

For meaningful work, state a compact TTD frame before writing:

- Decision: what must become unambiguously true after the slice.
- Owner / Scope: which repo, surface, file family, or authority plane owns the change.
- Contract: which file, API behavior, UI state, schema, policy, or doc proves the decision.
- Gate / Test: the smallest check that would fail if the decision is false.
- Implementation Slice: the smallest safe change needed to make the gate pass.
- Evidence: the command, output, file, or log that proves the result.
- Next Gate: what remains deliberately not claimed or deferred.

Use TDD inside implementation-bearing slices. TDD tests code behavior; TTD tests whether the development claim is valid. A task is done only when the claimed decision state is locally verifiable with evidence, or when the result is explicitly reported as `partial` or `BLOCKED`.

### Evidence Language

Use exact paths and label claims as:

- `Observed`: directly read from files, commands, repo state, or tool output.
- `Inferred`: reasoned from observed evidence.
- `Recommended`: proposed next action.
- `Applied`: a real write occurred and the path is named.
- `Verified`: applied change was read back or checked with named evidence.
- `BLOCKED`: authority, source, scope, validation, permission, or preservation of existing work is insufficient.

Do not present imported, summarized, compressed, assumed, or loose-doc context as canonical repo truth unless the owning surface has reviewed and promoted it.

### Stop Conditions

Stop and report `BLOCKED` when:

- owner, scope, authority, source, or validation is unclear;
- root, portfolio, shared-core, and repo-local guidance conflict;
- a loose doc, chat summary, archive, or imported source would drive implementation without owning-surface approval;
- required checks or evidence cannot prove the claim;
- an edit would overwrite user or agent work that was not created by the current task.
<!-- workspace-root-sync:agents:end -->
