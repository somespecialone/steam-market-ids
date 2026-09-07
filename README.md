# Steam Market Ids

[![license](https://img.shields.io/github/license/somespecialone/steam-item-name-ids)](https://github.com/somespecialone/steam-item-name-ids/blob/master/LICENSE)
[![steam](https://shields.io/badge/steam-1b2838?logo=steam)](https://store.steampowered.com/)

This is a storage repo of `Steam Market`-related identifiers.

> [!WARNING]
> Does not contain all items 📦

If you find some items missing, consider [contributing](#contributing).

## Apps

- [x] [730/CS2](./data/CS2).
- [x] [440/TF2](./data/TF2).

## Structure

All files are UTF-8 JSON objects. Keys are exact Steam names; do not normalize
case, punctuation, or Unicode.

- `item_names.json` - `<market_hash_name>: <item_name_id>` map. Values are integers.
- `market_bucket_groups.json` - `<market_bucket_group_name>: <market_bucket_group_id>` map.
  Values are strings. A bucket group ID can belong to multiple item covariants.

Steam bucket groups include item covariants rather than only distinct items. For
example, `G1883283004` includes `Austin 2025 Dust II Souvenir Package` and
`Austin 2025 Dust II Souvenir Highlight Package`: the highlight package is a
category of the souvenir package, not a distinct item. `StatTrak™` variants
follow the same rule. If Steam has only a `StatTrak™` variant or variants has distinct market groups,
the index uses its exact `StatTrak™` name, such as `StatTrak™ Deluge Music Kit Box`.

Bucket group IDs are not a reverse index: multiple names can map to the same ID.

## Contributing

New entries should be at the end of the file for better observability.
Before opening a PR, use UTF-8 encoding with two-space indentation, matching
the existing files. Pull requests validate JSON structure, unique keys, and
value types automatically.

## See also 👀

- [aiosteampy](https://github.com/somespecialone/aiosteampy) - library to interact with `Steam Market`.
