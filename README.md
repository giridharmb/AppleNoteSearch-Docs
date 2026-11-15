<p align="center"><img src="docs/images/icon.png" width="128" alt="NoteSearch icon"></p>

# NoteSearch

Find any Apple Note in a keystroke. NoteSearch lives in the macOS menu bar: press a shortcut, type part of a title,
a `#hashtag` or a folder name, press Return, and the note opens in Notes.

![Searching by hashtags and title](docs/images/search.png)

*Screenshots use sample data.*

## What it does

- **Search as you type** by note title, hashtag, folder or account, with fuzzy matching and typo tolerance.
- **Combine filters**: several hashtags (AND / OR / exclude) together with title words.
- **Autocomplete** for hashtags and folders that already exist in your notes.
- **Tabs** for the most recently updated, most recently created and largest notes, plus a list of all hashtags.
- **Keyboard first**: a global shortcut, arrow keys and Return. No mouse needed.
- **Private**: reads note titles and metadata only, never note contents, and never connects to the network.
- **Nine colour themes** and a handful of useful options.

## Documentation

| Guide | What's inside |
| --- | --- |
| [Getting started](docs/getting-started.md) | Requirements, installing, granting Full Disk Access, first search |
| [Search syntax](docs/search-syntax.md) | Hashtags, AND / OR / exclude, folders, accounts, fuzzy and typo matching, ranking |
| [Keyboard shortcuts](docs/keyboard-shortcuts.md) | Every key, in the popup and system-wide |
| [Tabs and settings](docs/tabs-and-settings.md) | Updated / Created / Largest / Tags tabs, themes, options |
| [Troubleshooting and FAQ](docs/troubleshooting.md) | Fixes for common problems, uninstalling |
| [Privacy](docs/privacy.md) | Exactly what is read and stored |

## Quick reference

| Type this | To find |
| --- | --- |
| `budget` | Notes with "budget" in the title, folder or tags |
| `#work` | Notes tagged `#work` |
| `#work #ideas` | Notes tagged with **both** |
| `#work\|#ideas` | Notes tagged with **either** |
| `#work -#draft` | Tagged `#work` but **not** `#draft` |
| `#work plan` | Tagged `#work` **and** "plan" in the title |
| `in:travel` | Notes in a folder whose name contains "travel" |
| `is:pinned` | Pinned notes (`is:locked`, `is:checklist` also work) |

## Help and feedback

- Something not working? Check [Troubleshooting](docs/troubleshooting.md) first.
- Found a bug or have an idea? [Open an issue](../../issues/new/choose).

## License

This documentation is © 2026 giridharmb and licensed under [CC BY 4.0](LICENSE): you may copy and adapt it if you
give credit. The license covers the documentation in this repository only, not the NoteSearch app.
