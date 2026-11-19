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
| **⌘1 … ⌘9** | Search, Favourites, Updated, Created, Largest, Tags, Folders, History, Settings. The numbers are for 1.12; earlier versions have fewer tabs, so their numbers are lower. **⌘,** always opens Settings |
| **⌘,** | Settings |
| **⌘T** | Switch between matching titles only and titles plus note text *(1.3+)* |
| **⌘S** | Change the sort order: best match, last updated, newest, largest, A–Z *(1.4+; A–Z from 1.8)* |
| **⌥1 … ⌥9** | Apply the first to ninth **Narrow** button above the results *(1.8+)* |
| **⌘+ / ⌘−** | Make the popup larger / smaller. It stays centred and remembers the size *(1.9+)* |
| **⌘0** | Return the popup to its default size *(1.9+)* |
| **⌘/** | Show or hide the list of all shortcuts *(1.8+)* |
| **⌘D** | Star or unstar the selected note as a favourite *(1.4+)* |
| **⌃1 … ⌃7** | Give the selected note a colour: red, orange, yellow, green, blue, purple, grey. The same key again removes it *(1.12+)* |
| **⌃0** | Remove the selected note's colour *(1.12+)* |
| **⌘M** | Move the selected note to a category: a list opens, press its number (1–9), or 0 for none *(1.15+)* |
| **⌘B** | Show or hide the categories sidebar *(1.15+)* |
| **⇧↑ / ⇧↓** | Select several notes; ⌘D, ⌃1–⌃7 and ⌘M then act on all of them *(1.19+)* |
| **⇧⌘A** | Select every note in the list *(1.19+)* |
| **⇧⌘D** | Save the search you are typing. It appears starred at the top of the History tab *(1.7+)* |
| **⌘N** | Create a new note in Notes, titled with whatever you have typed. macOS asks for permission the first time *(1.4+)* |
| **⇧⌘C** | Copy a link to the selected note. Opening the link shows that note in Notes |
| **⌥⌘C** | Copy the selected note's title *(1.7+)* |
| **⌃⌘C** | Copy a Markdown link to the selected note, `[title](link)` *(1.7+)* |
| **⌘R** | Reload notes |
| **Esc** | Clear the selection of several notes if there is one, then the search box; if that is empty, close the popup |
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

## With the mouse *(1.15+)*

Right-click a note for a menu *(1.15+)*:

| Menu item | What it does |
| --- | --- |
| **Open in Notes** / **Open and Keep This Popup** | The same as Return and ⌘Return |
| **Star** / **Remove Star** | The same as ⌘D |
| **Colour** | Pick one of the seven colours, or None |
| **Category** | Move the note to one of your categories, take it out of its category, or make a new one |
| **Hide from NoteSearch** | Keeps the note out of every list. See [Hiding notes](search-syntax.md#hiding-notes-113) |
| **Notes in "folder"** | Lists the notes in the same folder |
| **Notes Tagged** | Lists the notes with one of this note's hashtags, or with all of them |
| **Notes Marked "colour"** / **Notes in Category** | Lists the other notes with the same colour or category |
| **Copy** | Link, title or Markdown link |

Right-click a category in the sidebar to show its notes, rename it, change its icon, move it up or down, put it
inside another category *(1.19+)*, or delete it.

**⌘-click** a note to select it along with others, and **⇧-click** to select a run of notes *(1.19+)*.

Nothing in these menus changes the note in Apple Notes.

**Versions 1.12 to 1.14:** the right-click menu on notes was announced for these versions but did not open. Update
to 1.15 or later. Everything it offers was, and is, also available from the keyboard.

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
