# Privacy

NoteSearch is built to know as little about your notes as it can.

## What it reads

For each note, from the Notes library on your Mac:

- Title
- Folder and account name
- Hashtags
- Created and last-updated dates
- Size of the note's text (a number only)
- Whether it is pinned, locked or contains a checklist

## What it never does

- It never reads, shows or stores the **contents** of your notes.
- It never changes, creates or deletes notes. Access is read-only.
- It never connects to the network. Nothing leaves your Mac, and there is no analytics or telemetry.

## What it stores

Only its own preferences, on your Mac:

- Your settings (theme, shortcut, options)
- Identifiers of the last 30 notes you opened through NoteSearch, so they can be listed first. These are internal
  IDs, not titles or text.

No copy or index of your notes is saved. The list is rebuilt in memory each time the popup opens.
To erase the stored preferences, see [How do I uninstall?](troubleshooting.md#how-do-i-uninstall).

## Why Full Disk Access?

macOS protects the Notes library and offers no narrower permission for reading it. Full Disk Access is the only
way macOS lets an app see your note titles. NoteSearch uses it for the Notes library and nothing else.
