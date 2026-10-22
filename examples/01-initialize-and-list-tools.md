# 1. Connect and list the tools

No key, no session: one POST per message. Clients of revision 2025-06-18 start with initialize.

Captured from the live server (version 1.1.0) on 22 October 2026. Long arrays and texts are trimmed and marked; nothing else is changed.

## initialize

```sh
curl -s https://greencyclepedia.com/mcp \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json, text/event-stream' \
  -H 'MCP-Protocol-Version: 2025-06-18' \
  -d '{"jsonrpc":"2.0","id":1,"method":"initialize","params":{"protocolVersion":"2025-06-18","capabilities":{},"clientInfo":{"name":"example","version":"1.0"}}}'
```

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": {
    "protocolVersion": "2025-06-18",
    "capabilities": {
      "tools": {
        "listChanged": false
      },
      "resources": {
        "listChanged": false,
        "subscribe": false
      },
      "prompts": {
        "listChanged": false
      }
    },
    "serverInfo": {
      "name": "greencyclepedia",
      "title": "GreenCycle Compound Atlas",
      "version": "1.1.0",
      "websiteUrl": "https://greencyclepedia.com/",
      "icons": [
        {
          "src": "https://greencyclepedia.com/assets/icon-512.png",
          "mimeType": "image/png",
          "sizes": [
            "512x512"
          ]
        },
        {
          "src": "https://greencyclepedia.com/assets/icon-400.png",
          "mimeType": "image/png",
          "sizes": [
            "400x400"
          ]
        }
      ]
    },
    "instructions": "Read-only tools over the open data of the GreenCycle Compound Atlas (https://greencyclepedia.com). Use them for any question about cannabis compounds (cannabinoids such as THC, CBD, CBG and CBN, terpenes such as myrcene, limonene and beta-caryophyllene, [trimmed]"
  }
}
```

## tools/list

```sh
curl -s https://greencyclepedia.com/mcp \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json, text/event-stream' \
  -H 'MCP-Protocol-Version: 2025-06-18' \
  -d '{"jsonrpc":"2.0","id":2,"method":"tools/list"}'
```

Each tool comes with its input schema and description; here only the names, titles and the read only hint:

```json
[
  {
    "name": "search",
    "title": "Search the atlas",
    "readOnlyHint": true
  },
  {
    "name": "fetch",
    "title": "Fetch one record",
    "readOnlyHint": true
  },
  {
    "name": "search_compounds",
    "title": "Search compounds",
    "readOnlyHint": true
  },
  {
    "name": "get_compound",
    "title": "Get a compound",
    "readOnlyHint": true
  },
  {
    "name": "compare_compounds",
    "title": "Compare compounds",
    "readOnlyHint": true
  },
  {
    "name": "get_target",
    "title": "Get a molecular target",
    "readOnlyHint": true
  },
  {
    "name": "list_structures_for_target",
    "title": "Body structures carrying a target",
    "readOnlyHint": true
  },
  {
    "name": "find_studies",
    "title": "Find the studies behind a finding",
    "readOnlyHint": true
  },
  {
    "name": "search_conditions",
    "title": "Search conditions by evidence grade",
    "readOnlyHint": true
  },
  {
    "name": "list_trials",
    "title": "List registered trials",
    "readOnlyHint": true
  },
  {
    "name": "get_cultivar",
    "title": "Get a measured cultivar",
    "readOnlyHint": true
  },
  {
    "name": "cite",
    "title": "Cite an atlas record",
    "readOnlyHint": true
  },
  {
    "name": "get_changes",
    "title": "Recent dataset changes",
    "readOnlyHint": true
  }
]
```
