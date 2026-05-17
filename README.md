# Steam Market Ids

[![license](https://img.shields.io/github/license/somespecialone/steam-item-name-ids)](https://github.com/somespecialone/steam-item-name-ids/blob/master/LICENSE)
[![steam](https://shields.io/badge/steam-1b2838?logo=steam)](https://store.steampowered.com/)

This is a storage repo of `Steam Market`-related identifiers.

> [!WARNING]
> Does not contain all items 📦

If you find some items missing, consider [contributing](#contributing).

## Apps:

- [x] [730/CS2](./data/CS2) (ex. CSGO).
- [x] [440/TF2](./data/TF2).

## Structure

* `item_names.json` - `<market_hash_name>:<item_name_id>` map.
* `market_bucket_groups.json` - `<market_bucket_group_name>:<market_bucket_group_id>` map.

## Contributing

New entries should be at the end of the file for better observability.
Please, before opening a PR format file properly: use **utf-8** encoding
with the **4 level indent**, thanks!

## TODO 📃

- [ ] `github action` that validates `json` files for pull requests.

## See also 👀

- [aiosteampy](https://github.com/somespecialone/aiosteampy) - library to interact with `Steam Market`.
