# Troubleshooting and FAQ

## "NoteSearch needs Full Disk Access"

macOS has not yet allowed NoteSearch to read the Notes library.

1. Open **System Settings → Privacy & Security → Full Disk Access**.
2. Turn on **NoteSearch**. If it is missing, click **+** and add it from Applications.
3. Click **Retry** in the popup, or quit and reopen NoteSearch.

If it is already on and the message stays, turn it off and on again, then reopen NoteSearch. This can be needed
after updating the app.

## The global shortcut does nothing

- Another app may be using the same combination. Open Settings (**⌘6**) and look for a red message under
  **Global shortcut**, then record a different one.
- Check the shortcut is not disabled in Settings.
- Make sure NoteSearch is running: its icon should be in the menu bar.

## I can't find the app after opening it

NoteSearch has no Dock icon and no window of its own. Look for the magnifying-glass icon in the menu bar, press
the global shortcut, or open NoteSearch again from Applications to bring up the popup. On a crowded menu bar the
icon may be hidden behind the notch; the shortcut still works.

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

## Can it search inside notes?

No. NoteSearch deliberately reads titles and metadata only and never note contents. Use the search in Notes for
that. See [How it works](how-it-works.md) for the full list of what is searched.

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
