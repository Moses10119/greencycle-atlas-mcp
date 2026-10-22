# 2. Search by any name

search answers with id, title and url, the shape ChatGPT deep research expects. Pass an id to fetch for the full record.

Captured from the live server (version 1.1.0) on 22 October 2026. Long arrays and texts are trimmed and marked; nothing else is changed.

```sh
curl -s https://greencyclepedia.com/mcp \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json, text/event-stream' \
  -H 'MCP-Protocol-Version: 2025-06-18' \
  -d '{"jsonrpc":"2.0","id":3,"method":"tools/call","params":{"name":"search","arguments":{"query":"CB2"}}}'
```

structuredContent of the answer (the same JSON also comes as text in content):

```json
{
  "results": [
    {
      "id": "target:CB2",
      "title": "CB2 (CB2), receptor",
      "url": "https://greencyclepedia.com/receptors/?ref=mcp#cb2"
    },
    {
      "id": "trial:NCT07783295",
      "title": "Evaluation of Bone Turnover Biomarkers, CB2 and TRPV1 Polymorphisms as Potential Preventive Data in Osteoporosis and Perception of Improvement in Quality of Life in Women With Chronic Pain Treated With Medicinal Cannabis (NCT07783295, not yet recruiting)",
      "url": "https://clinicaltrials.gov/study/NCT07783295"
    }
  ]
}
```
