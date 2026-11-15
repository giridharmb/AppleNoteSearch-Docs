# Search syntax

Type one or more terms separated by spaces. A note must match **every** term. Upper/lower case and accents are
ignored, so `cafe` finds "Café".

## Terms

| Term | Matches | Example |
| --- | --- | --- |
| a word | Notes whose title, folder name or hashtags contain it | `budget` |
| `#tag` | Notes with that hashtag | `#work` |
| `in:name` | Notes in a folder whose name contains `name` (`folder:` also works) | `in:travel` |
| `account:name` | Notes in an account whose name contains `name` (`acct:` also works) | `account:icloud` |
| `is:pinned` | Pinned notes | |
| `is:locked` | Locked notes | |
| `is:checklist` | Notes that contain a checklist | |

Folder and account names are matched with spaces removed. For a folder called "Work Projects", type
`in:workprojects` or just `in:work`.

## Combining terms

| You type | Meaning |
| --- | --- |
| `#work #ideas` | Has **both** hashtags (AND) |
| `#work\|#ideas` | Has **either** hashtag (OR). `#work\|ideas` is a shorter way to write the same thing |
| `#work OR #ideas` | Also OR. `OR` must be in capitals |
| `-#draft` | Does **not** have the hashtag. A leading `-` excludes any kind of term |
| `#work plan` | Tagged `#work` and "plan" in the title |
| `#fitness\|#health in:personal -is:locked run` | Either hashtag, in a folder containing "personal", not locked, with "run" in the title |

OR also works for plain words and other terms, for example `invoice|receipt` or `in:work|in:clients`.

![Either of two hashtags plus a title word](images/search.png)

*`#work|#ideas plan`: tagged `#work` or `#ideas`, with "plan" in the title.*

## Hashtags

- While you are still typing a hashtag it matches as a prefix: `#wor` finds `#work` and `#workout`.
- Once what you typed is a complete hashtag that exists in your notes, it matches exactly: `#work` no longer
  finds `#workout`.
- Only real Notes hashtags are recognised (the ones Notes turns yellow when you type `#something` in a note).

## Autocomplete

- Type `#` to see hashtags that exist in your notes, most used first. Keep typing to narrow the list.
- Type `in:` to see your folders.
- Press **Tab** to accept the first (highlighted) suggestion, or click any suggestion.
- Autocomplete also works after `|`, so you can build `#work|#ideas` with two Tab presses.

![Hashtag autocomplete](images/autocomplete.png)

*Typing `#w` suggests the hashtags that contain "w"; Tab accepts the highlighted one.*

## Fuzzy matching and typos

If a word is not found as typed, NoteSearch tries two looser matches against note titles:

- **Skipped letters** (3 letters or more): the letters must appear in order, close together.
  `wrkt` finds "Workout plan".
- **Typos** (5 letters or more): one wrong, missing, extra or swapped letter is allowed, two for words of
  9 letters or more. `wrokout` finds "Workout plan".

These looser matches always rank below exact matches.

![A typo still finds the note](images/typo.png)

*`budgte` still finds "Budget 2027", and `in:fi` offers the Finance folder.*

## How results are ordered

On the **Search** tab, best matches come first:

1. Title is exactly what you typed
2. Title starts with it
3. A word in the title starts with it
4. It appears inside a word in the title
5. It matches the folder name
6. It matches the start of a hashtag
7. Fuzzy match
8. Typo match

Ties are ordered by most recently updated. The Search tab shows up to 300 results.

On the **Updated**, **Created** and **Largest** tabs the same search filters the list, but the order is fixed by
that tab. See [Tabs and settings](tabs-and-settings.md).
