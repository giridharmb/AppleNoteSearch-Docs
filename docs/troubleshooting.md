# Troubleshooting and FAQ

## "NoteSearch needs Full Disk Access"

macOS has not yet allowed NoteSearch to read the Notes library.

1. Open **System Settings → Privacy & Security → Full Disk Access**.
2. Turn on **NoteSearch**. If it is missing, click **+** and add it from Applications.
3. Click **Retry** in the popup, or quit and reopen NoteSearch.

If it is already on and the message stays, turn it off and on again, then reopen NoteSearch. This can be needed
after updating the app.

## The global shortcut does nothing

- Another app may be using the same combination. Open Settings (**⌘,**) and look for a red message under
  **Global shortcut**, then record a different one.
- Check the shortcut is not disabled in Settings.
- Make sure NoteSearch is running: its icon should be in the menu bar.

## I can't find the app after opening it

NoteSearch has no Dock icon and no window of its own. Look for the magnifying-glass icon in the menu bar, press
the global shortcut, or open NoteSearch again from Applications to bring up the popup. On a crowded menu bar the
icon may be hidden behind the notch; the shortcut still works.

## Many notes seem to be missing

- **Update to 1.2 or later.** Earlier versions listed at most 300 results on the Search tab, so with a large
  library most notes never appeared in the list.
- **Check the count** at the top right of the popup. "42 of 3,050 notes" means 3,050 notes were loaded and 42
  match what you typed.
- **The Updated, Created and Largest tabs show the top 50** by design. Raise the number in Settings, or use the
  Search tab to see everything.
- **Text inside notes is not searched unless you turn it on.** By default only titles, hashtags, folder names,
  account names and attachment file names are matched. From version 1.3, turn on **Search inside note text** in
  Settings or press **⌘T**.
- **Notes in Recently Deleted are not listed.**
- Notes that belong to a mail account (Gmail, Exchange, IMAP) rather than iCloud or On My Mac are not supported.

If notes are still missing, open Settings (**⌘,**), click **Copy diagnostics**, and paste the result into a
[bug report](../../../issues/new/choose). The report contains only counts, no titles or names.

## A note I just created or renamed is missing

NoteSearch re-reads your notes every time the popup opens. Press **⌘R** to reload while it is open. Notes that
were just created on another device appear once Notes on this Mac has synced them.

## A hashtag is missing

Only real Notes hashtags are indexed: the ones Notes highlights when you type `#something` in a note. Plain text
that merely contains a `#` is not a hashtag. Notes in the Recently Deleted folder are not listed.

## The popup disappears when I click somewhere else

That is the default. Turn off **Hide popup when it loses focus** in Settings to keep it on screen. To keep it open
after opening one note, use **⌘Return** instead of Return.

## Pressing Return does not open the note

Make sure the Notes app can open normally. If Notes opens but shows a different note, or nothing happens, please
[report it](../../../issues/new/choose) with your macOS version.

## The popup stays on top of System Settings while I grant access

This happened in version 1.0 when the popup had not been clicked: it floated above other windows and could not be
dismissed. Click once inside the popup and press **Esc**, or quit NoteSearch from its menu-bar icon, grant Full
Disk Access, and open it again. Version 1.1 hides the popup as soon as you click anywhere else.

## ⌘N does not create a note

The first time you press **⌘N**, macOS asks whether NoteSearch may control Notes. If you chose Don't Allow, open
**System Settings → Privacy & Security → Automation**, find NoteSearch and turn on **Notes**. The popup shows
"New note failed" when permission is missing.

## How do I turn off the update check?

Open Settings (**⌘,**) and turn off **Check for updates once a day**. See [Privacy](privacy.md#network-use).

## Can it search inside notes?

Yes, from version 1.3, but it is off by default. Turn on **Search inside note text** in Settings or press **⌘T**.
Locked notes are never read. See [How it works](how-it-works.md) for the full list of what is searched.

## Does it work with locked notes?

Yes. Locked notes are listed by title with a lock icon. Notes still asks for your password when you open one.

## Does it change my notes?

No. NoteSearch only reads. Opening a note is done by Notes itself.

## How do I quit?

Right-click the menu-bar icon and choose **Quit NoteSearch**, or press **⌘Q** while the popup is open.

## How do I uninstall?

1. Quit NoteSearch.
2. Drag NoteSearch from Applications to the Trash.
3. Optional: remove it from **System Settings → Privacy & Security → Full Disk Access**, and from
   **General → Login Items** if you enabled Launch at login.
4. Optional: delete its saved settings by running this in Terminal:

```bash
defaults delete com.giridharmb.NoteSearch
```

## Still stuck?

[Open an issue](../../../issues/new/choose) and include your macOS version, the NoteSearch version, and what you
typed or pressed.
