# 5. A ready citation

The citation line, BibTeX, the original papers and the licence. url is the page to cite; link is the same page with ?ref=mcp for a reader.

Captured from the live server (version 1.1.0) on 22 October 2026. Long arrays and texts are trimmed and marked; nothing else is changed.

```sh
curl -s https://greencyclepedia.com/mcp \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json, text/event-stream' \
  -H 'MCP-Protocol-Version: 2025-06-18' \
  -d '{"jsonrpc":"2.0","id":5,"method":"tools/call","params":{"name":"cite","arguments":{"id":"compound:cbd"}}}'
```

```json
{
  "record": "CBD",
  "type": "compound",
  "url": "https://greencyclepedia.com/compounds/cbd/",
  "link": "https://greencyclepedia.com/compounds/cbd/?ref=mcp",
  "version": "2026-10-20",
  "citation": "GreenCycle Compound Atlas. CBD. Version 2026-10-20. Retrieved 2026-10-22 from https://greencyclepedia.com/compounds/cbd/. Sources: PubChem CID 644019; PMID 17876302; PMID 21079038; PMID 32880179; PMID 39835903; PMID 30219789; PMID 37330538.",
  "bibtex": "@misc{greencyclepedia-cbd-20261020,\n  title = {CBD},\n  author = {{GreenCycle Compound Atlas}},\n  year = {2026},\n  note = {Version 2026-10-20. Accessed 2026-10-22},\n  howpublished = {\\url{https://greencyclepedia.com/compounds/cbd/}}\n}",
  "originalPapers": [
    {
      "source": "PMID 17876302",
      "link": "https://pubmed.ncbi.nlm.nih.gov/17876302/"
    },
    {
      "source": "PMID 21079038",
      "link": "https://pubmed.ncbi.nlm.nih.gov/21079038/"
    },
    "[4 more papers left out]"
  ],
  "otherSources": [
    "PubChem CID 644019"
  ],
  "licence": {
    "name": "CC BY 4.0",
    "terms": "CC BY 4.0 for the atlas text and curation: reuse it with a citation to the atlas and to the original source. Values from other sources keep their own licence, listed beside them.",
    "url": "https://creativecommons.org/licenses/by/4.0/"
  },
  "rule": "Cite the original paper for a finding (its PubMed link) and this atlas page for the map."
}
```
