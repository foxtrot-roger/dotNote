## dotNote

**A keyboard-first, local-first notebook with instant search + text expansion.**
```
Write everything. Organize nothing. Find it instantly.
```

![Alt Text: dotNote in action](dotNote.gif)

---

## 🚀 Try it now
👉 Live demo: **[https://foxtrot-roger.github.io/dotNote/index.html](https://foxtrot-roger.github.io/dotNote/index.html)**

Works fully offline. No install. No account. No setup.

**Take it with you:** Right-click the link above and select `Save Link As`, then open the downloaded page.

---

## 🧠 What is dotNote?

dotNote is a minimalist notebook that replaces folders and structure with:
- full-text search
- keyboard-driven workflows
- custom text shortcuts

Instead of organizing notes, you just write them, and find them later instantly.

Think of it as: `Ctrl+F for your brain` + `text expansion`

---

## ⚡ The core idea

Most note apps force you to decide *where things belong*.
dotNote removes that step completely:

No folders
No tagging system required
No upfront structure
Just write → search → reuse

Your brain already knows how to find things. dotNote leans into that.

---

## ✨ Key features
### 🔎 Search-first notes
Everything is instantly searchable with fuzzy matching.
### ⌨️ Text expansion (“stenos”)
Create your own shortcuts while you write:
- `todo` → !todo 2026-05-15
- `jcc` → Jean-Claude Convenant
- `..date+3week` → future date

Just type to trigger expansion tools, type `..` for system expansion.

### ⌨️ Keyboard Cheat Sheet
| Shortcut | Action |
| --- | --- |
| `Esc` | Focus / clear search bar |
| `Ctrl+↑/↓` | Navigate to note up / down |
| `Ctrl+C` | Copy full note (when no text is selected) |

---

### ⚡ System shortcuts (built-in)
- `..date` → today’s date
- `..time` → current time
- `..now` → full timestamp
- `..tomorrow` → next day
- `..date+3days` → date in 3 days

---

### 🧩 Create your own shortcuts
You don’t configure anything.
Just write a note like:
```
..brb Be right back
```
Now typing `br` opens a suggestion menu that will display every expansion that starts with `br`.

---

### 🧠 Search + write in the same bar

The search bar lets you create notes.
- type to search notes
- press enter to create
- type `..` to manage shortcuts

No mode switching. No context switching.

---

### 💾 Fully local-first
- Stored in browser IndexedDB
- Works offline
- Nothing is sent anywhere by default

Optional sync available via JSONBin (or similar services).

---

🔄 Example workflow

You’re working all day and dumping notes quickly:

```
meeting ideas
bug: login broken
follow up with client
random thought about architecture
```

Later you type:
```
follow
```
and instantly everything relevant appears—no folders, no tagging, no sorting.

---

### 🧭 Philosophy

dotNote is built on a simple idea:

```
Don’t organize your thoughts. Retrieve them faster instead.
```
- ~~structure~~ → search
- ~~folders~~ → queries
- ~~schemas~~ → personal conventions

You decide the meaning of your system.

---

### ⚙️ Advanced features
- Overloadable shortcuts (`stenos`)
- Non-recursive expansion (predictable behavior)
- Import / export (JSON)
- Optional sync via webhooks / external storage
- Mobile-friendly controls

---

### 📱 Mobile ready
- quick insert `..` shortcuts
- fast add button
- export/share support

---

### ⚠️ Important note

dotNote is intentionally minimal.

It does not try to be:
- a knowledge graph
- a task manager
- a workspace system

It is just:
```
a fast way to write things down and get them back later
```

---

### 📦 Download / self-host

Single-file app:
👉 https://foxtrot-roger.github.io/dotNote/index.html
Right-click → “Save as” → run locally.

---

### 💬 Why I built this

I kept losing small pieces of information in:
- too many tab
- scattered notes
- over-structured systems

So I built something that assumes:
```
You will never organize perfectly - so retrieval should be instant.
```
---

## HowTo: Sync with JSONBin

Copy JSONBin info into dotNote
- Open dotNote either locally or through the live version
- Open the side menu → `Cloud Sync` → `Show Config`
- In the dropdown `Service Preset` → select `JSONBin.io`

You will see the following information:

```
VERB: `PUT`
ENDPOINT: `https://api.jsonbin.io/v3/b/<YOUR_BIN_ID>`
HEADERS:
Content-Type: application/json
X-Master-Key: <API_KEY>
X-Access-Key: <ACCESS_KEY>
DATA PATH: `record`
```

The values are provided by JSONBin

**Create a free JSONBin account**

Create a free JSONBin account
- Navigate to https://jsonbin.io
- Create a **free** account using any sign up method


**Create a bin to store your notes**
- `https://api.jsonbin.io/v3/b/<YOUR_BIN_ID>`:
- [JSONBin](https://jsonbin.io) → `BINS` → `Create a Bin`
	- `⚙️` → change the name to `dotNote`
	- In the JSON section, write `[{}]`
	- Click `Save Bin`
	- In the bins, click the bin you just created and copy it's ID
- In dotNote, replace `<YOUR_BIN_ID>` with the ID you copied

**Configure API keys**
***Note:** API Keys are stored in the browser's LocalStorage, and only sent over HTTPS to JSONBin*
```
Content-Type: application/json
X-Master-Key: <API_KEY>
X-Access-Key: <ACCESS_KEY>
```
- [JSONBin](https://jsonbin.io) → `API KEYS`
	- In dotNote, replace `<API_KEY>` with the value under `X-Master-Key`

- [JSONBin](https://jsonbin.io) → `API KEYS` → `Create Access Key`
	- Write `dotNote` in the `NAME` field
	- Check the `UPDATE` checkbox
	- Click `Save Access Key`
	- In dotNote, replace `<ACCESS_KEY>` with the value under `X-Access-Key` with name `DOTNOTE`

**Configure Data Path**
- In dotNote, leave the field `DATA PATH` set to `record`
*Technically, it is the path of the data in the JSON returned by JSONBin*

**Synchronize with JSONBin**
- Click the `↑` button to send everything to JSONBin
- Click the `↓` button to receive everything from JSONBin
**Note:** The app will ask you to confirm overriding when downloading but there is no check for version at the moment