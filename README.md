# dotNote
`type, find, expand.`

**dotNote** is a minimalist, keyboard-first note system built around full-text search and text expansion.

![Alt Text: dotNote in action](dotNote.gif)

## 🌐 Live Access & 📥 Local Setup

You can use the live version immediately:
**[https://foxtrot-roger.github.io/dotNote/index.html](https://foxtrot-roger.github.io/dotNote/index.html)**

**Take it with you:** dotNote is a single-file application, it works entirely offline. You can download the `index.html` directly from the app (using the "Export" or "Download" feature).
⚠️ Do not save the webpage (`Ctrl+S`) from the browser as the page is generated on the fly. 


## TLDR; How it works

You type → **dotNote** expands:
- `..now` → `2026-05-09 13:19` (Current date and time)
- `..date` → `2026-05-09` (Today's date)
- `..time` → `13:19` (Current time)
- `..tomorrow` → `2026-05-10` (Tomorrow date and time)
- `..` → Opens the expansion menu to show you what's possible.
- Create your own shortcodes by createing notes starting with `..`

### Define your own Shortcodes
dotNote lets you create your own custom expansions just by writing a note:
- **Create a note:** `..todo ..date [TODO] :` 
    - *Result:* Typing `..todo` will expand to `2026-05-09 [TODO] :`
- **Create a note:** `..jcc Jean-Claude Convenant`
    - *Result:* Typing `..jcc` will expand to `Jean-Claude Convenant`
- **Create a note:** `..todo [TODO]`
    - *Result:* Searching for `..todo` in the master bar will instantly find all notes containing `[TODO]`.

⚠️ dotNote intentionally only support system shortcode expansion in shortcodes, custom shortcodes will not be recursively expanded.
Given the notes :
- `..inner ..date INNER`
- `..outer ..inner ..time`

When typing `..outer` dotNote will expand to `..inner 14:05`

## 🚀 The Philosophy
dotNote doesn't tell you how to organize; it gives you the tools to build your own system. Whether you use it as a journal, a task tracker, or a code snippet library, it adapts to your typing style.

- **~~organize~~ → find** : searching is faster than filing
- **~~structure~~ → syntax** : plain text is the ultimate data format
- **~~datamodel~~ → your conventions** : you define the rules, not the app

No folders, no schemas, only `..yourConventions`.