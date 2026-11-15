<p align="center"><img src="docs/images/icon.png" width="128" alt="NoteSearch icon"></p>

# NoteSearch

Find any Apple Note in a keystroke. NoteSearch lives in the macOS menu bar: press a shortcut, type part of a title,
a `#hashtag` or a folder name, press Return, and the note opens in Notes.

<p align="center"><b><a href="https://github.com/giridharmb/AppleNoteSearch-Docs/releases/latest">⬇ Download the latest version</a></b> · macOS 14 or later · signed and notarized by Apple</p>

![The NoteSearch popup listing notes](docs/images/hero.png)

*All screenshots in this documentation show made-up sample notes.*

## Download and install

1. [Download the latest `NoteSearch-<version>.dmg`](https://github.com/giridharmb/AppleNoteSearch-Docs/releases/latest) from the Releases page.
2. Open it and drag **NoteSearch** to **Applications**.
3. Open NoteSearch and grant it Full Disk Access when asked.

Step-by-step instructions with pictures are in [Getting started](docs/getting-started.md).

## What it does

- **Search as you type** by note title, hashtag, folder or account, with fuzzy matching and typo tolerance.
- **Combine filters**: several hashtags (AND / OR / exclude) together with title words.
- **Autocomplete** for hashtags and folders that already exist in your notes.
- **Tabs** for the most recently updated, most recently created and largest notes, plus a list of all hashtags.
- **Keyboard first**: a global shortcut, arrow keys and Return. No mouse needed.
- **Search inside note text, if you want it**: off by default; one switch (or ⌘T) turns it on *(1.3+)*.
- **Search history** and **multi-select hashtags** with live note counts *(1.3+)*.
- **Date filters, sort order, favourites** and a **new-note shortcut** *(1.4+)*.
- **Saved searches**, filters for size, untagged and shared notes, a text-size setting, a resizable popup and a
  one-click update download *(1.7+)*.
- **Private**: by default only titles and metadata are read. Note text is read only if you turn that on, is kept
  in memory only, and is never saved, and is shown only if you ask for the matching line. The only network use is an optional daily
  check for a newer version, which sends nothing about you or your notes.
- **Nine colour themes** and a handful of useful options.

## Screenshots

| | |
| --- | --- |
| ![Search combining hashtags and a title word](docs/images/search.png) <br> Either of two hashtags, plus a word in the title | ![Hashtag autocomplete](docs/images/autocomplete.png) <br> Hashtag autocomplete |
| ![Typo-tolerant search with folder autocomplete](docs/images/typo.png) <br> A typo still finds the note; folders autocomplete too | ![Largest notes tab](docs/images/largest.png) <br> Largest notes (Dracula theme) |
| ![Notes with PDF attachments](docs/images/attachments.png) <br> Notes with a PDF attached: `is:attachment pdf` | ![Notes in a folder and its sub-folders](docs/images/folders.png) <br> A folder and its sub-folders: `in:work` (Solarized Dark theme) |
| ![Search inside note text](docs/images/text.png) <br> Searching inside note text, when turned on | ![Selecting several hashtags](docs/images/tags-multi.png) <br> Ticking several hashtags shows how many notes have all or any |
| ![Notes changed in the last week](docs/images/dates.png) <br> Date filter: `updated:7d` | ![The matching line of text](docs/images/snippet.png) <br> Optional: the line of text that matched |
| ![Search history](docs/images/history.png) <br> History of past searches | ![Tags tab](docs/images/tags.png) <br> Every hashtag with its note count (Midnight theme) |
| ![Settings](docs/images/settings.png) <br> Settings (Notes Yellow theme) | |

## Documentation

| Guide | What's inside |
| --- | --- |
| [Getting started](docs/getting-started.md) | Requirements, installing, granting Full Disk Access, first search |
| [Search syntax](docs/search-syntax.md) | Hashtags, AND / OR / exclude, folders, accounts, fuzzy and typo matching, ranking |
| [Keyboard shortcuts](docs/keyboard-shortcuts.md) | Every key, in the popup and system-wide |
| [Tabs and settings](docs/tabs-and-settings.md) | Updated / Created / Largest / Tags tabs, themes, options |
| [How it works](docs/how-it-works.md) | Where results come from, what is and is not searched, speed |
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
| `is:attachment` | Notes that have attachments *(1.1+)* |
| `updated:7d` | Notes changed in the last 7 days *(1.4+)* |
| `is:favorite` | Notes you starred with ⌘D *(1.4+)* |

## Help and feedback

- Something not working? Check [Troubleshooting](docs/troubleshooting.md) first.
- Found a bug or have an idea? [Open an issue](../../issues/new/choose).

## License

This documentation is © 2026 giridharmb and licensed under [CC BY 4.0](LICENSE): you may copy and adapt it if you
give credit. The license covers the documentation in this repository only, not the NoteSearch app.
