# Keyboard shortcuts

## Anywhere on your Mac

| Shortcut | Action |
| --- | --- |
| **⌃⌥N** | Show or hide the search popup. You can change or disable this in [Settings](tabs-and-settings.md#settings) |

## In the popup

| Shortcut | Action |
| --- | --- |
| **↑ / ↓** | Move the selection |
| **Page Up / Page Down** | Move the selection by 10 |
| **Return** | Open the selected note in Notes |
| **⌘Return** | Open the selected note and keep the popup on screen |
| **Tab** | Accept the first autocomplete suggestion. With no suggestions: go to the next tab |
| **⇧Tab** | Go to the previous tab |
| **⌘1 … ⌘8** | Search, Updated, Created, Largest, Tags, Folders, History, Settings *(before 1.8 there is no Folders tab, so History is ⌘6 and Settings ⌘7)* |
| **⌘,** | Settings |
| **⌘T** | Switch between matching titles only and titles plus note text *(1.3+)* |
| **⌘S** | Change the sort order: best match, last updated, newest, largest, A–Z *(1.4+; A–Z from 1.8)* |
| **⌥1 … ⌥9** | Apply the first to ninth **Narrow** button above the results *(1.8+)* |
| **⌘+ / ⌘−** | Make the popup larger / smaller. It stays centred and remembers the size *(1.9+)* |
| **⌘0** | Return the popup to its default size *(1.9+)* |
| **⌘/** | Show or hide the list of all shortcuts *(1.8+)* |
| **⌘D** | Star or unstar the selected note as a favourite *(1.4+)* |
| **⇧⌘D** | Save the search you are typing. It appears starred at the top of the History tab *(1.7+)* |
| **⌘N** | Create a new note in Notes, titled with whatever you have typed. macOS asks for permission the first time *(1.4+)* |
| **⇧⌘C** | Copy a link to the selected note. Opening the link shows that note in Notes |
| **⌥⌘C** | Copy the selected note's title *(1.7+)* |
| **⌃⌘C** | Copy a Markdown link to the selected note, `[title](link)` *(1.7+)* |
| **⌘R** | Reload notes |
| **Esc** | Clear the search box. If it is already empty, close the popup |
| **⌘W** | Close the popup |
| **⌘Q** | Quit NoteSearch |

The usual text shortcuts (⌘A, ⌘C, ⌘V, ⌘X, ⌘Z) work in the search box.

## On the Tags tab

| Shortcut | Action |
| --- | --- |
| **Return** | Search for the highlighted hashtag, or for notes that have **all** the ticked hashtags |
| **Space** | Tick or untick the highlighted hashtag *(1.3+)* |
| **⌥Return** | Search for notes that have **any** of the ticked hashtags *(1.3+)* |
| **⌘S** | Switch the list between most used first and A–Z *(1.4+)* |

## On the Folders tab *(1.8+)*

| Shortcut | Action |
| --- | --- |
| **Return** | List the notes in the highlighted folder and its sub-folders |

## On the History tab *(1.3+)*

| Shortcut | Action |
| --- | --- |
| **Return** | Run the highlighted search again |
| **⌘D** | Save or unsave the highlighted search *(1.7+)* |
| **⌘⌫** | Remove the highlighted search from the history |

## Menu-bar icon

| Action | Result |
| --- | --- |
| Click | Show or hide the popup |
| Right-click | Menu with Search Notes, Reload Notes, Settings and Quit |

Opening NoteSearch again from Applications or Spotlight also shows the popup.

## From other apps *(1.8+)*

Opening a link of the form `notesearch://search?q=budget` shows the popup with that search already typed. Use it
from Raycast, Alfred, Shortcuts or the `open` command. Spaces are written `%20` and `#` is written `%23`, as in
`notesearch://search?q=plan%20%23work`.
