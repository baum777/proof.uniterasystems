# UNITERA Wiki

## Purpose
Das Wiki ist eine **planning, synthesis, and memory surface** für UNITERA im Read-only-Modus.
Es dient der strukturierten Klärung von Strategie, Benennung, Outreach, Evidenz und Entscheidungen, ohne Runtime- oder Produktwahrheit zu erzeugen.

## Wiki vs Log
Das Wiki ist die strukturierte Wissens- und Syntheseoberfläche.
Das Log ist die **diary / chronological evidence surface** für zeitliche Nachvollziehbarkeit.
Wiki-Einträge bündeln Themen stabil nach Sachgebiet; Log-Einträge dokumentieren den Verlauf append-only nach Datum.

## Directory Map
- `wiki/index.md`: Einstieg und Verweise auf relevante Themen
- `wiki/strategy/`: strategische Rahmen, Spannungen, Prioritäten
- `wiki/naming/`: Naming-Grenzen und Begriffsdisziplin
- `wiki/outreach/`: Outreach-Hypothesen, Rückmeldungen, Interpretationsgrenzen
- `wiki/evidence/`: Evidenzmodelle und Claim-Grenzen
- `wiki/decisions/`: Entscheidungsfelder, Optionen, offene Punkte

## Reading Order
1. `AGENTS.md` (Regeln und Red Lines)
2. `README.md` (Stack-Frame und Claim-Disziplin)
3. `WORKFLOW.md` (READ -> CLASSIFY -> SYNTHESIZE -> RECORD -> REVIEW -> NEXT)
4. `log/README.md` und aktueller Tageslog
5. `wiki/index.md` und thematische Wiki-Seiten

## Entry Rules
Jeder Wiki-Eintrag bleibt ein Planungsartefakt und enthält mindestens:
- Fragestellung oder Spannung
- Quellenbasis inkl. Authority-Klasse (`canonical`, `proposed_import`, `working_note`, `wiki_entry`, `diary_log` …)
- aktuelle Synthese (Observed/Inferred klar trennen)
- offene Entscheidungen
- nächste kleinste Read-only-Aktion

Klassifikation pro Thema:
- Strategy: Leitbild, Wedge-Logik, Priorisierung
- Naming: Begriffsgrenzen, Bedeutungsstabilität
- Outreach: Marktgespräche, Signale, Überinterpretationsrisiken
- Evidence: Evidenzstatus, Claim-Boundaries
- Decisions: Entscheidungsoptionen, Kriterien, offene Gating-Fragen

## Boundary Rules
Wiki-Einträge sind **nicht** Runtime-Truth, Product-Proof, Customer-Proof, Certification-Proof oder Implementation-Approval.
Strategy, naming, outreach, evidence und decisions bleiben Planungsartefakte, bis eine separate Promotion in kanonische Runtime-/Produktoberflächen erfolgt.

Unverrückbare Layer-Grenzen:
- UNITERA bleibt Platform Layer.
- `uniCommit` bleibt System Layer / Control Surface Label.
- `OfferFlow` bleibt erster Revenue-v1 Workflow Wedge.
- `Commitment Core` bleibt Runtime Authority.

Keine Ableitung von Runtime-Surfaces aus Wiki-Texten.
Keine Einführung von `/unicommit` oder `/offerflow` Routen.
Keine impliziten Aussagen zu Production-Readiness, Customer-Proof, Certification, Integration-Proof oder ROI-Proof.

## Suggested Entry Template
```markdown
# [Topic]

## Status
working_note | decision_prep | accepted_context | superseded

## Question
Was wird geklärt?

## Source Basis
- [datei/link]: authority_class

## Current Understanding
Observed:
Inferred:

## Boundaries
Was darf nicht inferiert werden?

## Open Decisions
- ...

## Next Read-only Step
- ...
```

## Open Folder Note
Leere Unterordner unter `wiki/` sind lokal nutzbar, werden aber von Git nicht versioniert.
Wenn Verzeichnispräsenz im Repository-Verlauf benötigt wird, sollten Platzhalterdateien (z. B. `.gitkeep`) in einem separaten Follow-up angelegt und freigegeben werden.

## Next Gate
Nächster sicherer Schritt: pro aktivem Themenordner den ersten Eintrag mit Authority-Klassifikation anlegen und anschließend einen kurzen Log-Eintrag append-only ergänzen.
