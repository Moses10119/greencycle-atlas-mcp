# Contributing

The atlas data and the server live at https://greencyclepedia.com; this repository holds the listing, the examples and these templates.

## Report a data error

Every value in the atlas traces to a PubMed identifier, a DOI or a database record. If one is wrong, missing or misread, tell us with the source that shows it:

- On GitHub: open a [data correction](https://github.com/Moses10119/greencycle-atlas-mcp/issues/new?template=data-correction.yml) issue with the record (for example `compound:cbd`), the field, what it says, what it should say and the PubMed identifier or DOI.
- Without a GitHub account: the contact form at https://greencyclepedia.com/#view=contact, topic "A correction to a source".

## Ask for a new compound

Open a [new compound request](https://github.com/Moses10119/greencycle-atlas-mcp/issues/new?template=new-compound.yml) with its name, its PubChem CID and at least one paper that measured it in cannabis or at a molecular target: every value in the atlas needs a source.

## Client set up problems

Open a [client set up problem](https://github.com/Moses10119/greencycle-atlas-mcp/issues/new?template=client-setup.yml) with the client and version, the config you used and the exact error. The [examples](examples/README.md) show working calls.

## Add to the atlas

Laboratories, researchers and growers can add measured data and sources on the site: https://greencyclepedia.com/#view=contributors

## Ground rules

- Sources only: no unsourced claims, no doses, no medical advice.
- Be kind. Assume good faith.
- Security problems: see [SECURITY.md](SECURITY.md), never a public issue.
