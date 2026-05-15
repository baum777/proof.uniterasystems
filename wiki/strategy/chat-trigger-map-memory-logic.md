# Chat-Trigger-Map für kontextsichere Memory-Einträge

## Status
decision_prep

## Question
Wie werden Konversationen iterativ in `wiki/` und `log/` eingetragen, ohne False Signals aus normalem Chat-Text?

## Source Basis
- `AGENTS.md`: canonical
- `WORKFLOW.md`: canonical
- `README.md`: canonical
- Chat-Kontext 2026-05-15: working_note

## Current Understanding
Observed:
- Der aktuelle Modus ist Read-only-Planung mit erlaubten Änderungen in Wiki- und Log-Flächen.
- Es existiert keine implementierte NLP-/Semantik-Automation im Repository.

Inferred:
- Ein expliziter `\`-Prefix als Opt-in reduziert Fehltrigger deutlich.
- Eine Zwei-Stufen-Logik (`\keyword` + `\apply`) vermeidet ungewollte Persistenz.

## Boundaries
- Kein Runtime-, API-, DB-, Schema-, Route-, Package- oder Deploy-Eingriff.
- Keine Ableitung von Produkt-, Compliance-, Integrations-, Customer- oder ROI-Proof.
- Wiki/Log bleiben Planungs- und Verlaufssurfaces, keine Runtime-Truth.

## Trigger-Map (Opt-in via `\`)
```yaml
version: 1
default_mode: no_write
escape_rule: "\\\\keyword => no_trigger"
codeblock_rule: "ignore triggers in fenced code blocks"
quote_rule: "ignore triggers in blockquotes"
url_rule: "ignore triggers in URLs"
confirm_token: "\\apply"
cancel_token: "\\cancel"

triggers:
  - keyword: "\\entscheidung"
    target: "wiki/decisions/"
    tags: ["#decisions", "#governance"]
    instruction: "Optionen, Kriterien, offene Gating-Fragen erfassen."
    template: "decision_prep"

  - keyword: "\\strategie"
    target: "wiki/strategy/"
    tags: ["#strategy", "#wedge"]
    instruction: "Spannung, Priorisierung, stabile Boundary dokumentieren."
    template: "working_note"

  - keyword: "\\naming"
    target: "wiki/naming/"
    tags: ["#naming", "#boundary"]
    instruction: "Begriffsgrenzen und Nicht-Ableitungen festhalten."
    template: "working_note"

  - keyword: "\\outreach"
    target: "wiki/outreach/"
    tags: ["#outreach", "#signal"]
    instruction: "Marktsignal und Überinterpretationsgrenzen dokumentieren."
    template: "working_note"

  - keyword: "\\evidenz"
    target: "wiki/evidence/"
    tags: ["#evidence", "#claims"]
    instruction: "Observed/Inferred trennen, Overclaiming-Risiko markieren."
    template: "working_note"

  - keyword: "\\risiko"
    target: "wiki/decisions/"
    tags: ["#risk", "#open"]
    instruction: "Risk/Open explizit markieren, keine Finalisierung."
    template: "decision_prep"
```

## Iterative Ablauf-Logik
1. Input erfassen (`timestamp`, `thread_id`, `speaker`, `text`).
2. Parser prüfen (`\`-Trigger, Escape-Regel, Codeblock-/Zitat-/URL-Filter).
3. Falls kein gültiger Trigger: nur Konversation fortsetzen, kein Write.
4. Falls Trigger gültig: Draft erzeugen (noch keine Persistenz).
5. Kontext-Wolke aktualisieren (nur Memory-Cache, keine Dateiänderung).
6. Bei `\apply`: Draft in Zielordner schreiben und Tageslog appenden.
7. Bei `\cancel`: Draft verwerfen, nur optionalen Log-Hinweis schreiben.
8. Bei neuer Wiki-Seite: `wiki/index.md` um Katalogzeile ergänzen.

## Kontext-Wolken-Logik
- Zweck: thematische Verdichtung ohne automatisches Schreiben.
- Input: kontextstarke Tokens ohne `\` (z. B. Risiko, Commitment, Evidenz).
- Wirkung: Score pro Thema erhöhen, aber `write_permission = false`.
- Umschalten auf `write_permission = true` nur bei explizitem `\keyword`.

## Persistenzregeln
- `log/YYYY-MM-DD.md`: append-only je bestätigtem Eintrag.
- `wiki/index.md`: nur bei neuer Wiki-Seite ergänzen.
- Dedupe: Wenn `(thread_id + normalized_text_hash)` bereits vorhanden, nur Log-Append ohne neue Wiki-Seite.

## Open Decisions
- Soll `\apply` global oder pro Trigger (`\apply entscheidung`) gelten?
- Soll die Kontext-Wolke pro Thread oder global geführt werden?
- Welche Mindestlänge braucht ein Draft vor Persistenz?

## Next Read-only Step
- Entscheidungsnotiz zur Bestätigungs-Syntax (`\apply` granular vs global) anlegen und danach Trigger-Map auf `accepted_context` prüfen.
