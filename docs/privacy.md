# Privacy

NoteSearch is built to know as little about your notes as it can, and to keep everything on your Mac.

## What it reads by default

For each note, from the Notes library on your Mac:

- Title
- Folder (with parent folders) and account name
- Hashtags
- Created and last-updated dates
- Size of the note's text (a number only)
- Whether it is pinned, locked or contains a checklist
- The file names of its attachments, from version 1.1 (never the attachments themselves)

With the default settings the text of your notes is not read.

## Note text: only if you turn it on

From version 1.3 there is an optional setting, **Search inside note text**, which is **off** unless you switch it on
(in Settings, with **⌘T**, or by clicking the "titles" label in the popup). While it is on:

- NoteSearch reads the text of your notes into memory so that searches can match it.
- The text is **never written to disk** by NoteSearch and **never displayed**. A matching note is only marked
  "in text".
- **Locked notes are never read.** They are encrypted, and NoteSearch does not ask for their password.
- Turning the setting off again discards the text from memory.

## What it never does

- It never changes, creates or deletes notes. Access is read-only.
- It never reads what is inside attachments.
- It never connects to the network. Nothing leaves your Mac, and there is no analytics or telemetry.

## What it stores

Only its own preferences, on your Mac:

- Your settings (theme, shortcut, options)
- Identifiers of the last 30 notes you opened through NoteSearch, so they can be listed first. These are internal
  IDs, not titles or text.
- Your last 50 searches, for the History tab *(1.3+)*. You can turn this off or clear it in Settings.

No copy or index of your notes is saved. The list is rebuilt in memory each time the popup opens.
To erase the stored preferences, see [How do I uninstall?](troubleshooting.md#how-do-i-uninstall).

## Diagnostics

**Settings → Copy diagnostics** puts a short report on your clipboard for bug reports. It contains counts and
Apple's internal field names only: no note titles, text, folder names or account names. Nothing is sent anywhere;
you choose whether to paste it.

## Why Full Disk Access?

macOS protects the Notes library and offers no narrower permission for reading it. Full Disk Access is the only
way macOS lets an app see your note titles. NoteSearch uses it for the Notes library and nothing else.
