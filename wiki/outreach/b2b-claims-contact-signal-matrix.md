# B2B- und Claims-Kontaktmatrix

## Status
decision_prep / working_note

## Fragestellung
Wie lassen sich relevante Kontaktpersonen außerhalb von LinkedIn priorisieren, wenn der Fokus auf B2B-Angebotsprozessen und Versicherung/Claims liegt?

## Source Basis
- `AGENTS.md`: canonical
- `README.md`: canonical
- `WORKFLOW.md`: canonical
- User-Kontext vom 2026-05-15: proposed_import

## Current Understanding
Observed:
Der aktuelle Fokus liegt auf B2B-Angebotsprozessen sowie Versicherung/Claims. Gesucht ist eine Matrix mit Signalen, Prioritäten, Scoring und zusätzlicher Eingabefeld-Logik für strukturierte Dokumentation.

Inferred:
Die höchste Kontaktwahrscheinlichkeit liegt dort, wo Prozessdruck, Budgetsignal, konkrete Tool-Spuren und Governance-Bedarf gleichzeitig sichtbar sind. Im D-A-CH-Kontext sollte die Ansprache eher über Kontrolle, Nachvollziehbarkeit, Durchlaufzeit und Fehlerreduktion laufen als über abstrakte Innovationssprache.

## Prioritätsmatrix

| Segment | Zielrollen | Primärer Schmerz | Relevante Signale | Priorität |
|---|---|---|---|---|
| B2B-Angebotsmanagement | Head of Sales Operations, RevOps, Bid Manager, Angebotsmanagement | Lange Angebotszyklen, manuelle Freigaben, CRM/ERP-Brüche | CPQ, Quote-to-Cash, Angebotsautomatisierung, Deal Desk | Hoch |
| B2B-Vertrieb komplexer Produkte | Head of Sales, Presales, Technical Sales, Commercial Operations | Sonderpreise, technische Klärungen, Vertragsabweichungen | Salesforce, HubSpot, SAP, Microsoft Dynamics, DealHub, Conga | Hoch |
| Versicherung Claims | Head of Claims, Claims Operations, Schadenmanagement, Claims Transformation | Rückstände, Dokumentenprüfung, Eskalationen, SLA-Druck | Claims Automation, Document AI, Guidewire, UiPath, ServiceNow | Hoch |
| Versicherung Backoffice | COO Office, Operations Excellence, Prozessmanagement, IT Business Partner | Medienbrüche, Kostenquote, manuelle Kontrollen | Process Mining, RPA, Workflow Automation, SAP FS | Hoch |
| Versicherung Compliance / Audit | Compliance Ops, Risk, Datenschutz, Internal Audit | Blackbox-Risiko, Nachvollziehbarkeit, Verantwortlichkeit | Audit Trail, Governance, Human-in-the-loop, Freigabelogik | Mittel bis hoch |

## Signal-Matrix

| Signalquelle | Was dokumentieren? | Stärke | Beispiel-Suchbegriffe |
|---|---|---:|---|
| Jobanzeigen | Rollen, Tools, Prozessbegriffe, Teamzuständigkeit | 5 | `Claims Automation`, `RevOps`, `CPQ`, `Power Automate`, `RPA` |
| Vendor-Webinare | Speaker, Firmenname, Use Case, Projektrolle | 5 | `Guidewire`, `UiPath`, `Celonis`, `ServiceNow`, `Salesforce` |
| Case Studies | Kunde, Problem, genutztes Tool, Ergebnisbehauptung | 4 | `Quote-to-Cash`, `Claims Transformation`, `Process Mining` |
| Konferenzprogramme | Vortragstitel, Rolle, Firma, Prozessbezug | 4 | `Schadenmanagement`, `Sales Excellence`, `Operations Excellence` |
| Vergabeportale | Ausschreibungstitel, Budgetnähe, Leistungsbeschreibung | 5 | `Dokumentenautomation`, `KI Assistenz`, `Workflow` |
| Tool-Communities | Implementierer, technische Fragestellung, Stack | 3 | `n8n`, `Power Platform`, `UiPath Community` |
| Firmen-Newsroom | Rollout-Meldung, Partnerschaft, Transformationsprogramm | 3 | `führt Copilot ein`, `digitalisiert Schadenprozess` |

## Scoring-Modell

| Kriterium | 0 Punkte | 1 Punkt | 2 Punkte | 3 Punkte |
|---|---|---|---|---|
| Prozessdruck | nicht sichtbar | allgemein erwähnt | konkreter Prozess betroffen | messbarer Engpass oder Rückstand |
| Tool-/Vendor-Spur | keine | generische Digitalisierung | konkretes Tool sichtbar | Tool plus Projekt-/Rollout-Kontext |
| Rollenfit | unklar | Strategie/Innovation | operative Prozessrolle | Budget- oder Ergebnisverantwortung |
| Governance-Bedarf | keiner sichtbar | indirekt möglich | regulierter Prozess | Audit, Freigabe, Risiko oder Compliance klar sichtbar |
| Implementierungsnähe | abstrakt | Pilot erwähnt | Use Case aktiv | Rollout, Betrieb oder Ausschreibung sichtbar |
| UNITERA-Fit | schwach | teilweise | klarer Workflow-Fit | Workflow plus Nachweis-/Commitment-Bedarf |

Maximalwert: 18 Punkte.

| Score | Priorität | Handlung |
|---:|---|---|
| 0-5 | Niedrig | Nicht verfolgen |
| 6-9 | Beobachten | In Longlist aufnehmen |
| 10-13 | Relevant | Kurz recherchieren und anschreiben |
| 14-16 | Hoch | Individuelle Ansprache vorbereiten |
| 17-18 | Sehr hoch | Top-Ziel, detaillierte Hypothese und konkreter Einstieg |

## Eingabefeld-Logik

Jeder potenzielle Kontakt sollte als strukturierter Datensatz dokumentiert werden:

| Feld | Zweck |
|---|---|
| Firma | Organisation eindeutig benennen |
| Segment | B2B-Angebot, B2B-Vertrieb, Claims, Backoffice, Compliance |
| Kontaktrolle | Rolle, Zuständigkeit und vermutete Entscheidungsebene |
| Quelle | Jobanzeige, Webinar, Case Study, Ausschreibung, Konferenz, Newsroom |
| Beobachtetes Signal | Nur belegte Information eintragen |
| Inferenz | Plausible Ableitung getrennt vom Signal notieren |
| Prozessschmerz | Welcher Workflow scheint betroffen? |
| Tool-Spur | Genannte Systeme, Plattformen oder Anbieter |
| Governance-Spur | Freigabe, Audit, Risiko, Compliance, Verantwortlichkeit |
| Score | Summe aus Scoring-Modell |
| Priorität | Niedrig, Beobachten, Relevant, Hoch, Sehr hoch |
| Outreach-Hypothese | Warum könnte diese Person antworten? |
| Erste Nachricht | Problemorientierter Einstieg ohne Überclaim |
| Next Gate | Nächste saubere Aktion |

## Dokumentations-Template

```text
Firma:
Segment:
Kontaktrolle:
Quelle:
Link / Fundort:

Observed Signal:

Inferred Need:

Prozessschmerz:
Tool-Spur:
Governance-Spur:

Score Prozessdruck:
Score Tool-/Vendor-Spur:
Score Rollenfit:
Score Governance-Bedarf:
Score Implementierungsnähe:
Score UNITERA-Fit:
Gesamtscore:
Priorität:

Outreach-Hypothese:
Erste Nachricht:
Next Gate:
```

## Boundaries
Diese Matrix ist ein Planungs- und Priorisierungsartefakt. Sie erzeugt keine Customer-Proof-, ROI-, Compliance-, Integrations- oder Produktwahrheit.

## Open Decisions
- Welche Region wird zuerst bearbeitet: Deutschland, Österreich oder Schweiz?
- Soll die erste Longlist stärker auf B2B-Angebotsprozesse oder auf Claims fokussieren?
- Welche Mindestpunktzahl gilt für aktive Ansprache?

## Next Read-only Step
Eine Longlist mit 20 bis 30 Firmen erstellen und jeden Treffer anhand dieser Matrix bewerten.
