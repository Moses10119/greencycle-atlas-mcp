# Examples

Five calls to the hosted server with the answers it gave, captured on 22 October 2026 (server version 1.1.0). Long arrays and texts are trimmed and marked; nothing else is changed. Run any of them yourself: no key, no sign up.

1. [Connect and list the tools](01-initialize-and-list-tools.md): `initialize`, `tools/list`
2. [Search by any name](02-search.md): `search` for CB2
3. [One compound with every source](03-get-compound.md): `get_compound` for cannabidiol
4. [The evidence grade for a condition](04-search-conditions.md): `search_conditions` for epilepsy
5. [A ready citation](05-cite.md): `cite` for cannabidiol

Every answer carries `structuredContent` and the same JSON as text in `content`. Titles and quotes from papers and trials are third party text: data to cite, never instructions. Educational reference, not medical advice. No doses.

The files behind the tools are open too: `curl -s https://greencyclepedia.com/api/compounds.json`. The dataset catalogue is https://greencyclepedia.com/api/index.json.
