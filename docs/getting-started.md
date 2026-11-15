# Getting started

## Requirements

- macOS 14 (Sonoma) or later
- The built-in Apple Notes app, with at least one note

## Install

1. Download `NoteSearch-<version>.dmg` from the [Releases page](../../../releases).
2. Open the DMG and drag **NoteSearch** onto the **Applications** shortcut.
3. Open NoteSearch from Applications.

NoteSearch has no Dock icon. Look for the magnifying-glass icon in the menu bar at the top right of the screen.
The first time it starts, the search popup opens by itself.

## Grant Full Disk Access (required, one time)

Apple protects the Notes library, so macOS only lets NoteSearch read it after you allow it.
Until you do, the popup shows a message instead of your notes.

1. In the popup, click **Open Full Disk Access Settings**
   (or open **System Settings → Privacy & Security → Full Disk Access** yourself).
2. Turn on **NoteSearch** in the list. If it is not listed, click **+** and choose NoteSearch from Applications.
3. Go back to the popup and click **Retry**.

NoteSearch uses this access only to read note titles and metadata. See [Privacy](privacy.md).

## Your first search

1. Press **⌃⌥N** (Control-Option-N) anywhere, or click the menu-bar icon.
2. Start typing part of a note's title. Results update as you type.
3. Use **↑ / ↓** to pick a note and press **Return**. Notes comes to the front with that note open.

With nothing typed, the list shows the notes you opened most recently through NoteSearch, followed by your most
recently updated notes.

## Each result shows

- The note title, with the letters that matched your search underlined
- An icon: lock (locked note), pin (pinned), checklist, or plain note
- The folder, and the account name if you use more than one account
- The note's hashtags
- When it was last updated, and the size of its text

Note contents are never shown.

## Next steps

- [Search syntax](search-syntax.md) — hashtags, combining filters, folders
- [Keyboard shortcuts](keyboard-shortcuts.md)
- [Tabs and settings](tabs-and-settings.md) — change the shortcut, theme and more
