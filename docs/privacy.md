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

## Index file for iPhone and iPad *(1.5+)*

From version 1.5 there is an optional setting, **Save an index for the iPhone and iPad app**, which is **off**
unless you switch it on. While it is on:

- NoteSearch saves one file, `NoteSearch-index.json`, in a **NoteSearch** folder in your iCloud Drive, and
  rewrites it when your notes change.
- The file lists, for each note: title, folder, account name, hashtags, created and last-updated dates, size,
  attachment file names, and whether it is pinned, locked or has a checklist.
- The file **never contains note text**, even when **Search inside note text** is on.
- Titles of locked notes are included, as they are in the popup. Their text is not.
- Because the file is in iCloud Drive, **Apple's iCloud syncs it** to your other devices, like any other file
  there. NoteSearch itself sends it nowhere.
- Turning the setting off stops the file being updated but does **not delete it**. To remove it, delete the
  NoteSearch folder from iCloud Drive in Finder.

The setting exists for a companion iPhone and iPad app, which is not available for download yet. Until it is,
there is no reason to turn the setting on.

## What it never does

- It never changes, creates or deletes notes. Access is read-only.
- It never reads what is inside attachments.
- It never sends anything about you or your notes anywhere. There is no analytics or telemetry. (The optional
  index file above is carried to your own devices by iCloud Drive, not by NoteSearch.)
- It never creates a note unless you press **⌘N** *(1.4+)*, and then it is the Notes app that creates it, after
  macOS has asked for your permission.

## Network use

Versions before 1.4 never connect to the network.

From version 1.4, NoteSearch checks **once a day** whether a newer version exists. It asks GitHub's public address
for this project's latest release and reads the version number from the reply. The request contains nothing about
you, your Mac or your notes. To stop it, turn off **Check for updates once a day** in Settings; NoteSearch then
makes no network connections at all.

## What it stores

Only its own preferences, on your Mac:

- Your settings (theme, shortcut, options)
- Identifiers of the last 30 notes you opened through NoteSearch, so they can be listed first. These are internal
  IDs, not titles or text.
- Your last 50 searches, for the History tab *(1.3+)*. You can turn this off or clear it in Settings.
- Identifiers of the notes you starred as favourites *(1.4+)*. Internal IDs again, not titles or text.
- The latest version number seen by the update check, and when it last ran *(1.4+)*.

No copy or index of your notes is saved, unless you turn on the
[index file for iPhone and iPad](#index-file-for-iphone-and-ipad-15). The list is rebuilt in memory each time the
popup opens.
To erase the stored preferences, see [How do I uninstall?](troubleshooting.md#how-do-i-uninstall).

## Diagnostics

**Settings → Copy diagnostics** puts a short report on your clipboard for bug reports. It contains counts and
Apple's internal field names only: no note titles, text, folder names or account names. Nothing is sent anywhere;
you choose whether to paste it.

## Why Full Disk Access?

macOS protects the Notes library and offers no narrower permission for reading it. Full Disk Access is the only
way macOS lets an app see your note titles. NoteSearch uses it for the Notes library and nothing else.
