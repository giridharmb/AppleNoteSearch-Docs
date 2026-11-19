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
- The text is **never written to disk** by NoteSearch. A matching note is only marked "in text".
- The text is **not displayed** unless you also turn on **Show the matching line for text matches** *(1.4+)*,
  which shows the single line that matched under the result.
- **Locked notes are never read.** They are encrypted, and NoteSearch does not ask for their password.
- Turning the setting off again discards the text from memory.

## What it never does

- It never changes, creates or deletes notes. Access is read-only.
- It never reads what is inside attachments.
- It never sends anything about you or your notes anywhere. There is no analytics or telemetry.
- It never creates a note unless you press **⌘N** *(1.4+)*, and then it is the Notes app that creates it, after
  macOS has asked for your permission.

## Network use

Versions before 1.4 never connect to the network.

From version 1.4, NoteSearch checks **once a day** whether a newer version exists. It asks GitHub's public address
for this project's latest release and reads the version number from the reply. The request contains nothing about
you, your Mac or your notes. To stop it, turn off **Check for updates once a day** in Settings; NoteSearch then
makes no network connections at all.

From version 1.7, clicking **Download and open** on the update notice downloads the new version's disk image from
this project's GitHub releases to your Downloads folder. This happens only when you click it.

## What it stores

Only its own preferences, on your Mac:

- Your settings (theme, shortcut, options)
- Identifiers of the last 30 notes you opened through NoteSearch, so they can be listed first. These are internal
  IDs, not titles or text.
- Your last 50 searches, for the History tab *(1.3+)*. You can turn this off or clear it in Settings.
- Your saved searches, and the terms in **Added to every search** *(1.7+)*.
- The colour you gave each note, by internal ID *(1.12+)*.
- Identifiers of the notes you starred as favourites *(1.4+)*. Internal IDs again, not titles or text.
- The latest version number seen by the update check, and when it last ran *(1.4+)*.

No copy or index of your notes is saved. The list is rebuilt in memory each time the popup opens.

**Version 1.5 only:** that version had an optional setting, off by default, called **Save an index for the iPhone
and iPad app**. If you turned it on, it saved a list of note titles, folders, hashtags, dates and attachment names
(never note text) to a **NoteSearch** folder in your iCloud Drive. The setting was removed in 1.6. Updating does
not delete that file; if you turned the setting on, delete the NoteSearch folder from iCloud Drive in Finder.
To erase the stored preferences, see [How do I uninstall?](troubleshooting.md#how-do-i-uninstall).

## Diagnostics

**Settings → Copy diagnostics** puts a short report on your clipboard for bug reports. It contains counts and
Apple's internal field names only: no note titles, text, folder names or account names. Nothing is sent anywhere;
you choose whether to paste it.

## Why Full Disk Access?

macOS protects the Notes library and offers no narrower permission for reading it. Full Disk Access is the only
way macOS lets an app see your note titles. NoteSearch uses it for the Notes library and nothing else.
