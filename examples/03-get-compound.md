# 3. One compound with every source

Targets with the measured binding values, the PubMed identifiers behind each, the evidence grade, cautions and the provenance of the answer.

Captured from the live server (version 1.1.0) on 22 October 2026. Long arrays and texts are trimmed and marked; nothing else is changed.

```sh
curl -s https://greencyclepedia.com/mcp \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json, text/event-stream' \
  -H 'MCP-Protocol-Version: 2025-06-18' \
  -d '{"jsonrpc":"2.0","id":4,"method":"tools/call","params":{"name":"get_compound","arguments":{"id":"cbd"}}}'
```

```json
{
  "compound": {
    "id": "cbd",
    "name": "CBD",
    "fullName": "Cannabidiol",
    "class": "cannabinoid",
    "formula": "C21H30O2",
    "molecularMass": 314.5,
    "pubchemCid": 644019,
    "summary": "Non-intoxicating, and almost none of what it does happens at CB1.",
    "[trimmed]": "more identity fields left out"
  },
  "targets": [
    {
      "target": "5-HT1A",
      "action": "agonist",
      "effect": "reduces anxiety, notably in public-speaking trials",
      "evidence": "clinical",
      "evidenceLabel": "Controlled human trials",
      "basis": "trial",
      "structures": [
        "amygdala",
        "hippocampus",
        "cerebral_cortex"
      ],
      "pmids": [
        "21307846"
      ],
      "pubmedSearch": "https://pubmed.ncbi.nlm.nih.gov/?term=cannabidiol%205-HT1A%20anxiety%20clinical%20trial"
    },
    {
      "target": "GPR55",
      "action": "antagonist",
      "effect": "reduces seizure activity; the leading mechanism for its approved epilepsy indication",
      "evidence": "clinical",
      "evidenceLabel": "Controlled human trials",
      "basis": "trial",
      "structures": [
        "cerebral_cortex",
        "hippocampus"
      ],
      "pmids": [
        "28538134",
        "29768152"
      ],
      "pubmedSearch": "https://pubmed.ncbi.nlm.nih.gov/?term=cannabidiol%20GPR55%20epilepsy%20Dravet%20Lennox-Gastaut"
    },
    "[5 more targets left out]"
  ],
  "bindingValues": [
    {
      "target": "GPR55",
      "parameter": "pIC50",
      "value": 6.3,
      "originalValue": "4.45x10-7 - 3.5x10-7",
      "originalType": "IC50",
      "action": "Antagonist",
      "species": "Human",
      "pmids": [
        "17876302",
        "21079038"
      ],
      "guideTarget": "https://www.guidetopharmacology.org/GRAC/ObjectDisplayForward?objectId=109"
    },
    {
      "target": "TRPA1",
      "parameter": "pEC50",
      "value": 6.3,
      "originalValue": "4.8x10-7",
      "originalType": "EC50",
      "action": "Agonist",
      "species": "Rat",
      "pmids": [
        "32880179"
      ],
      "guideTarget": "https://www.guidetopharmacology.org/GRAC/ObjectDisplayForward?objectId=485"
    },
    "[13 more binding values left out]"
  ],
  "evidenceSummary": {
    "targetEffects": 7,
    "byGrade": {
      "clinical": 3,
      "preclinical": 4
    },
    "highestGrade": "Controlled human trials",
    "gradeScale": "From highest to lowest: controlled human trials, human studies, tested in animals, cells or tissue only, proposed mechanism."
  },
  "cautions": [
    {
      "topic": "Other medicines",
      "text": "CBD slows liver enzymes that clear many medicines (CYP3A4, CYP2C9 and CYP2C19). In 169 people, more CBD went with higher blood levels of clobazam and several other anti-seizure medicines.",
      "studyType": "Review of studies in people",
      "pmids": [
        "41417208",
        "37593907"
      ]
    },
    "[1 more left out]"
  ],
  "notice": "Educational reference, not medical advice. No doses are given. Risks and effects are reported as the cited studies found them, which is not a prediction for [trimmed]",
  "provenance": {
    "dataset": "https://greencyclepedia.com/api/compounds.json",
    "title": "Mapped compounds",
    "version": "2026-10-20",
    "generated": "2026-10-22",
    "retrieved": "2026-10-22T14:01:55Z",
    "sources": [
      "PubChem CID 644019",
      "PMID 21307846",
      "PMID 28538134",
      "PMID 29768152",
      "[14 more sources left out]"
    ],
    "licences": [
      "GreenCycle Compound Atlas curation and text: CC BY 4.0",
      "PubChem, National Library of Medicine: Public domain",
      "IUPHAR/BPS Guide to PHARMACOLOGY: CC BY-SA 4.0"
    ],
    "thirdPartyText": "Titles, quotes, summaries and names of papers, trials and products in this result are third party text copied word for [trimmed]",
    "notice": "Educational reference, not medical advice. No doses are given. Talk to a doctor or pharmacist about any medicine, including cannabis.",
    "howToCite": "Give the person the link of a record; cite its url (the atlas page) and the original papers (PubMed links) for any finding.",
    "citation": "GreenCycle Compound Atlas. CBD. Version 2026-10-20. Retrieved 2026-10-22 from https://greencyclepedia.com/compounds/cbd/. Sources: PubChem CID 644019; PMID 17876302; PMID 21079038; PMID 32880179; PMID 39835903; PMID 30219789; PMID 37330538."
  }
}
```
