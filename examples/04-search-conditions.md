# 4. The evidence grade for a condition

Conditions by evidence grade with the systematic reviews and trials behind them. Never a dose.

Captured from the live server (version 1.1.0) on 22 October 2026. Long arrays and texts are trimmed and marked; nothing else is changed.

```sh
curl -s https://greencyclepedia.com/mcp \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json, text/event-stream' \
  -H 'MCP-Protocol-Version: 2025-06-18' \
  -d '{"jsonrpc":"2.0","id":6,"method":"tools/call","params":{"name":"search_conditions","arguments":{"query":"epilepsy"}}}'
```

```json
{
  "matches": 1,
  "conditions": [
    {
      "id": "epilepsy",
      "name": "Drug-resistant epilepsy",
      "bodySystem": "nervous",
      "evidenceGrade": "substantial",
      "evidenceGradeLabel": "Substantial evidence",
      "gradeNote": "This is the strongest evidence in the field: multiple large, randomised, placebo-controlled phase 3 trials with consistent effect, leading to FDA and EMA approval of purified cannabidiol (Epidiolex/Epidyolex).",
      "systematicReviews": [
        {
          "pmid": "37593907",
          "citation": "Gaston TE et al. Epilepsia Open. 2023",
          "atlasSummary": "Documents the interaction that shapes real-world dosing: cannabidiol raises N-desmethylclobazam substantially, and clobazam dose reduction is frequently required. Part of the observed benefit in early trials was attributed to this interaction, which later placebo-controlled work addressed."
        }
      ],
      "trials": [
        {
          "pmid": "28538134",
          "citation": "Devinsky O et al. NEJM. 2017 (Dravet syndrome)",
          "route": "oral",
          "duration": "14 weeks",
          "note": "as administered in this trial; the dose is left out on purpose, read the paper"
        },
        "[2 more trials left out]"
      ],
      "url": "https://greencyclepedia.com/conditions/epilepsy/",
      "link": "https://greencyclepedia.com/conditions/epilepsy/?ref=mcp",
      "[trimmed]": "what, compounds, structures and citeAs left out"
    }
  ],
  "disclaimer": "A record of published trials, not medical advice, a diagnostic tool or a dosing plan. Screening tools are meant for trained clinicians. Decisions about cannabis-based medicines belong with a qualified prescriber who knows the person, their diagnosis and their other medicines."
}
```
