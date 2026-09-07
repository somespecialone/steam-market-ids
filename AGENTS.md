# Agent Guide

## Project
Static Steam Market identifier datasets; no application build or test suite.
- `data/CS2/`: Counter-Strike 2 (app 730).
- `data/TF2/`: Team Fortress 2 (app 440).
- `item_names.json`: market hash names → integer item name IDs.
- `market_bucket_groups.json`: market bucket group names → string group IDs (currently CS2 only).

## Editing Rules
- Preserve exact Steam names, Unicode, punctuation, and identifier types.
- Append new entries at the end, as required by `README.md`; do not sort existing entries.
- Never invent identifiers. Use verifiable Steam data and describe the source when submitting changes.
- Keep keys unique. Correct or remove existing mappings only with supporting evidence.
- Use UTF-8 and two-space indentation, matching existing files. Avoid whole-file reformatting unless requested.
- Keep changes limited to the requested datasets; do not add dependencies or tooling for routine data updates.

## Validation
Pull requests validate every `data/**/item_names.json` and
`data/**/market_bucket_groups.json` file for valid UTF-8 JSON, unique keys, and
the expected value type. For each changed dataset, run:
```sh
python3 -m json.tool data/CS2/item_names.json > /dev/null
```
Replace the path as needed. Also check for duplicate keys and verify value
types; `json.tool` does not reject duplicate keys.

## Delivery
Report changed datasets, entry additions/corrections/removals, data sources, and validation performed. These datasets are intentionally incomplete; do not claim exhaustive coverage.
