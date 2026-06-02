# proof.uniterasystems

**Public evidence surface and architecture reference for UNITERA** — a governance-first operating layer between enterprise systems and AI models, controlling AI-assisted business processes through to accountable, auditable commitments.

→ **Live:** [proof.uniterasystems.com](https://proof.uniterasystems.com)
→ **Product:** [uniterasystems.com](https://www.uniterasystems.com/en)
→ **Portfolio:** [portfolio.uniterasystems.com](https://portfolio.uniterasystems.com)

---

## What UNITERA is

UNITERA is an **AI Governance Operating System for business commitments**.

The canonical description: a governance-first operating layer between enterprise systems and AI models — making AI-assisted processes structured, controllable, reviewable, auditable, traceable, and accountable.

This is not a copilot, a dashboard, or an automation tool. The question UNITERA answers is not *"Is the AI output good?"* — it is:

> **Who approved what, on what basis, under which policy, in which state, and when?**

AI may draft, analyse, and prepare. It may not commit without a governance path.

---

## The strategic shift: from output control to commitment governance

| Before | Now |
|---|---|
| Review AI output after the draft | Govern the entire commit path |
| Review happens after the draft | Governance runs through the full flow |
| Product = OfferFlow | OfferFlow = first app on the OS |
| UI / workflow focus | Domain, policy, review, audit focus |
| Trust through good answers | Trust through evidence, roles, gates, traceability |

The old framing: *AI generates something, then we review it.*
The current framing: an AI-assisted process runs through defined states — and the transition to binding business commitment is controlled at every step.

---

## System architecture

UNITERA is structured in seven layers:

```
1. Governance Kernel      — states, transitions, commit rules
2. Context Binding        — allowed sources, assumptions, scope boundaries
3. Policy & Risk Engine   — risk gates, claim checks, commit blockers
4. Role & Accountability  — who decides what, on what basis
5. Workflow Runtime       — review queues, escalation, approval conditions
6. Agent Control          — what agents may do, and what requires a human gate
7. Evidence & Audit       — sources, decisions, approvals, commit receipt
```

The commit flow every document must pass through:

```
Intake
  └── Context Binding (Opportunity, Documents, Rules)
        └── Governed Draft (AI-assisted, not AI-decided)
              └── Policy Evaluation (Risk Gates)
                    └── Multi-Role Review Queue
                          └── Approval Console
                                └── Traceable Commit
                                      └── Audit Timeline / Evidence Bundle
```

A document cannot reach Commit unless Review, Policy, and Approval are fully resolved. Missing approval = blocked commit. This is enforced server-side, not trusted from the client.

---

## OfferFlow: first app on the OS

OfferFlow is the first application running on the UNITERA governance layer — a revenue commitment workflow for Proposals, RFPs, and Change Requests.

The platform logic sits beneath it: roles, rules, context, policies, commit checks, and audit paths. This makes UNITERA extensible: ContractFlow, PolicyFlow, or AgentFlow can be built on the same governance kernel without each module inventing its own source of truth.

---

## Tech stack

| Layer | Technology |
|---|---|
| Frontend | Next.js 14 (App Router), TypeScript, Tailwind CSS |
| Backend | Node.js, TypeScript, Supabase (PostgreSQL + RLS + Auth) |
| ORM | Prisma |
| Deployment | Vercel |
| AI Integration | Anthropic Claude API (`claude-sonnet-4-6`) |
| Protocol | MCP (Model Context Protocol) — provider-agnostic tool/context layer |
| Auth / RBAC | Supabase Auth + Row Level Security + JWT role claims |
| PDF generation | Server-side artifact rendering |

---

## Key engineering decisions

**Backend owns authority.** No critical state lives in the UI. Approval decisions, commit status, policy gate results, and audit records are server-enforced. The client renders state — it does not determine it.

**Fail-closed commit flow.** A workflow cannot reach Commit without a complete Review + Approval chain. There is no skip, no implicit approval, no fallback to "just send it."

**Explicit claim boundary.** The system distinguishes runtime-backed gates (enforced by code) from architecturally modelled gates (design intent, not yet wired to runtime). This distinction is documented and visible — not hidden behind confident UI language.

**Multi-tenant from day one.** Row Level Security policies isolate all tenant data at the database layer. `tenantId` is injected server-side from the authenticated session. It is never read from the request body.

**Model-agnostic by design.** AI models connect through a controlled adapter layer. Swapping providers does not change governance logic, commit conditions, or audit records. The system's integrity does not depend on any one model.

**MCP-native context integration.** External context (CRM state, document sources, policy rules) arrives through MCP servers. Tool boundaries are explicit — agents operate within defined, auditable scope.

---

## What this repo contains

```
/
├── app/                    # Next.js App Router — pages and layouts
│   ├── (proof)/            # Public proof surface routes
│   └── api/                # API routes (server-side only, no auth bypass)
├── components/             # UI components — no business logic, no authority
├── lib/
│   ├── supabase/           # Supabase client + server helpers
│   ├── prisma/             # Prisma schema and client
│   └── anthropic/          # Claude API integration layer
├── public/
│   └── assets/             # Downloadable synthetic PDF artifacts
├── types/                  # Shared TypeScript interfaces
└── docs/                   # Architecture notes, governance boundary documentation
```

---

## What this repo is not

- Not a live customer integration
- Not a compliance or legal certification tool
- Not a claim that all policy gates are runtime-enforced (the Risk Checklist documents which are)
- Not a competitor analysis or marketing comparison

The boundary between "runtime-enforced" and "architecturally modelled" is documented honestly throughout. That distinction is part of the design philosophy, not a limitation to be hidden.

---

## Related repos

| Repo | Description |
|---|---|
| `Unitera_Systems` | Main application — governance kernel, workflow engine, review queues, approval console, audit timeline |
| `proof.uniterasystems` | This repo — public evidence surface and architecture reference |
| `warenwirtschaft-gastronovi-workflow` | Warehouse / F&B workflow system — domain-specific system built on the same governance patterns |

---

## Author

**Cheikh Fall** — AI Governance & Agentic Systems  
Self-taught engineer and founder. Based in Böblingen, Germany.  
Building governance-first infrastructure for AI-assisted business processes.

→ Portfolio: [portfolio.uniterasystems.com](https://portfolio.uniterasystems.com)  
→ Book a call: [cal.eu/cheikh-fall](https://cal.eu/cheikh-fall)  
→ Contact: [briefings@uniterasystems.com](mailto:briefings@uniterasystems.com)

---

*All synthetic artifacts on proof.uniterasystems.com are clearly labelled as synthetic. No customer data, no active integration claims, no compliance assertions.*
