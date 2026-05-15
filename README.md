# dotNote
`type, find, expand.`

**dotNote** is a minimalist, keyboard-first note system built around full-text search and text expansion.

![Alt Text: dotNote in action](dotNote.gif)

## 🌐 Live Access & 📥 Local Setup

You can use the live version immediately:
**[https://foxtrot-roger.github.io/dotNote/index.html](https://foxtrot-roger.github.io/dotNote/index.html)**

**Take it with you:** Right click the link above and select "Save Link As".
dotNote is a single-file application, it works entirely offline.
⚠️ Do not save the webpage (`Ctrl+S`) from the browser as the page is generated on the fly.

## TLDR; How it works

You type → **dotNote** expands:
- System functions start with `..`
- User can extend stenos by creating notes starting with `..`

## 🚀 The Philosophy
dotNote doesn't tell you how to organize; it gives you the tools to build your own system. Whether you use it as a journal, a task tracker, or a code snippet library, it adapts to your typing style.

- **~~organize~~ → find** : searching is faster than filing
- **~~structure~~ → syntax** : plain text is the ultimate data format
- **~~datamodel~~ → your conventions** : you define the rules, not the app

No folders, no schemas, only `..yourConventions`.


### Define your own stenos
dotNote lets you create your own custom expansions just by writing a note:
- **Create a note:** `..todo !todo ..date :` 
    - *Result:* Typing `..todo` will expand to `!todo 2026-05-09 :`
- **Create a note:** `..jcc Jean-Claude Convenant`
    - *Result:* Typing `..jcc` will expand to `Jean-Claude Convenant`

⚠️ dotNote intentionally does not support expansion of user stenos recursively.
Given the notes :
- `..inner ..date INNER`
- `..outer ..inner ..time`

When typing `..outer` dotNote will expand to `..inner 14:05`

## System functions

dotNote provides system functions, they all start with "..":
- `..now` → `2026-05-09 13:19` (Current date and time)
- `..date` → `2026-05-09` (Today's date)
- `..time` → `13:19` (Current time)
- `..tomorrow` → `2026-05-10` (Tomorrow's date and time)
- `..` → Opens the expansion menu to show you what's possible.



## Example stenos
``` 
..freeze !freeze ..today
!followup ..date+3month
!followup ..date+6month
!purge ..date+9month
```

```
..funw !followup ..week+1week
```

```
..shout !shout
!followup ..date
!followup ..date+1day
!followup ..date+2day
!followup ..date+3day
!followup ..date+4day
!followup ..date+5day
!followup ..date+6day
!followup ..date+7day
```

```
..wait !waiting
!lastnews ..today
!followup ..date+3week
!burn ..date+4week
!purge ..date+5week
```