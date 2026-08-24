# proof.uniterasystems

**Static public evidence and orientation surface for UNITERA.**

This repository is a small, claim-bounded website. Its tracked implementation
is a static `index.html` plus visual assets and synthetic reference artifacts;
it is not the UNITERA runtime, API, database, or product authority.

## Current repository state (observed 2026-08-18)

- The committed site entry point is [`index.html`](index.html).
- The page contains inline HTML/CSS/JS and the sections Problem, Process,
  Comparison, Artifacts, and Checklist.
- `assets/` contains downloadable synthetic PDFs and one static HTML artifact,
  including the Problem Brief, Revenue Commitment Risk Checklist, Mini Audit
  Evidence Demo, and outreach material.
- Favicon, manifest, and touch-icon assets are committed at repository root.
- There is no `package.json`, application source tree, database schema, API
  route, build script, or automated test configuration in the committed surface.
- The page declares `noindex,nofollow` and labels the concept layer and all
  artifacts as synthetic. A local `.vercel/project.json` exists, but it is only
  project metadata; deployment and live-runtime behavior are not claimed from
  this checkout.

A local untracked `review/` directory is present in the worktree. It is not part
of the committed public proof surface and is intentionally excluded from this
README's implementation description.

## What UNITERA is

UNITERA is a governance-first operating layer for AI-assisted business
workflows. The public page demonstrates the control idea:

```text
Intake
  → Context Binding
  → Governed Draft
  → Policy Evaluation
  → Multi-Role Review
  → Approval Console
  → Traceable Commit
  → Audit Evidence
```

OfferFlow is presented as the first demonstrated workflow wedge on the UNITERA
OS. This repository explains that framing; it does not create runtime routes,
domain objects, execution authority, or product modules.

## Evidence and claim boundary

The page and its downloads are orientation and problem-validation artifacts.
They may illustrate roles, policy gates, review, approval, commit, and audit
evidence, but they do not prove:

- a live customer integration or customer data;
- a productive external execution path;
- regulatory compliance or certification;
- production readiness, procurement readiness, or ROI;
- that every depicted policy gate is runtime-enforced.

The boundary is also stated in the page itself: synthetic artifacts are not
customer proof, implementation proof, or compliance proof.

## External surfaces

These links are the external surfaces named by the project. Their current live
state is not verified by the local repository checks:

- [Proof site](https://proof.uniterasystems.com)
- [Product site](https://www.uniterasystems.com/en)
- [Portfolio](https://portfolio.uniterasystems.com)

## Local preview

No package-manager setup is required by the tracked site. Open `index.html` in a
browser or serve the repository with a static file server. There is no committed
build or test command to report as a passing project gate.

## Repository guidance

Read [`AGENTS.md`](AGENTS.md) and [`WORKFLOW.md`](WORKFLOW.md) before changing
the proof surface. Planning, wiki, diary, and evidence artifacts remain
classified by authority and must not be promoted into runtime truth merely by
being placed in this repository.
