# How NoteSearch works

A short, plain-language description of what happens when you search.

## 1. It reads Apple Notes' own index

The Notes app keeps all of its data in a database file on your Mac:

```
~/Library/Group Containers/group.com.apple.notes/NoteStore.sqlite
```

Each time the popup opens (or you press **⌘R**), NoteSearch opens that file **read-only** and asks it for a list
of your notes. For every note it collects:

- the title
- the folder (with its parent folders) and the account
- the hashtags
- the created and last-updated dates
- the size of the note's text, as a number
- whether it is pinned, locked or has a checklist
- the file names of attachments *(version 1.1 and later)*

The text of your notes is never requested. For size, NoteSearch asks the database only "how many bytes is this?",
not for the bytes themselves. macOS protects this file, which is why NoteSearch needs
[Full Disk Access](getting-started.md#grant-full-disk-access-required-one-time).

## 2. It searches in memory

The list from step 1 is kept in memory while NoteSearch runs. Nothing is written to disk and no separate index is
built. Every time you type a character, NoteSearch:

1. splits what you typed into terms (words, `#hashtags`, `in:folder` and so on),
2. checks every note against those terms and gives each match a score,
3. sorts the matches, best first, and shows them.

There is no waiting for the database while you type, which is what keeps results instant. From version 1.1 the
checking is spread across all of your Mac's processor cores when you have more than about 2,000 notes. In our
test with 50,000 made-up notes, a search took about 6 milliseconds, and about 30 milliseconds when it had to fall
back to typo matching.

Upper/lower case and accents are ignored, so `cafe` finds "Café".

## 3. Notes opens the note

When you press **Return**, NoteSearch hands the note's internal ID to macOS, and the Notes app opens it.
NoteSearch never opens, changes or deletes a note itself.

## What is searched, and what is not

| | Searched? |
| --- | --- |
| Note titles | Yes |
| Hashtags | Yes |
| Folder names, including parent folders of nested folders | Yes. `in:projects` finds notes in "Work › Projects" |
| Notes inside nested folders, in every account | Yes, all of them |
| Account names | Yes, with `account:` |
| Attachment file names (PDFs, images, scans…) | Yes, from version 1.1. `is:attachment` lists notes that have any |
| The text inside notes | **No**, by design |
| The contents of attachments | **No** |
| Notes in Recently Deleted | No |
| Files and folders elsewhere on your Mac | No. NoteSearch only knows about Apple Notes |

## Keeping up to date

NoteSearch re-reads the list every time the popup opens, so new, renamed and deleted notes appear without you
doing anything. Notes created on another device appear once the Notes app on this Mac has synced them.

## A note on macOS updates

The Notes database is Apple's own format and is not documented. NoteSearch checks which fields exist before
reading, so it tolerates the usual changes between macOS versions, but a major macOS update could require a
NoteSearch update. If your notes stop loading after updating macOS, please
[open an issue](../../../issues/new/choose).
