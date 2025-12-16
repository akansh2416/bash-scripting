# ✏️ VI Editor Shortcuts

The **VI editor** is a powerful, modal text editor widely used in Linux and Unix systems. Mastering its shortcuts greatly improves editing speed and efficiency.

---

## 🧭 Modes in VI Editor

| Mode | Description |
|----|------------|
| **Normal Mode** (default) | Navigation and command execution |
| **Insert Mode** | Text editing (`i` to enter, `Esc` to exit) |
| **Command Mode** | Saving, quitting, and searching (`:` from Normal mode) |

---

## 🧭 Basic Navigation

| Shortcut | Action |
|--------|-------|
| `h` | Move left |
| `l` | Move right |
| `j` | Move down |
| `k` | Move up |
| `0` | Move to the beginning of the line |
| `^` | Move to the first non-blank character |
| `$` | Move to the end of the line |
| `w` | Move to the next word |
| `b` | Move to the previous word |
| `gg` | Move to the start of the file |
| `G` | Move to the end of the file |
| `:n` | Move to line number `n` |

---

## ✍️ Insert Mode Shortcuts

| Shortcut | Action |
|--------|-------|
| `i` | Insert before cursor |
| `I` | Insert at the beginning of the line |
| `a` | Append after cursor |
| `A` | Append at the end of the line |
| `o` | Open a new line below |
| `O` | Open a new line above |
| `Esc` | Exit Insert mode |

---

## ✂️ Editing Text

| Shortcut | Action |
|--------|-------|
| `x` | Delete a character |
| `X` | Delete character before cursor |
| `dw` | Delete a word |
| `dd` | Delete a line |
| `d$` | Delete from cursor to end of line |
| `d0` | Delete from cursor to beginning of line |
| `D` | Delete from cursor to end of line |
| `u` | Undo last action |
| `Ctrl + r` | Redo an undone change |
| `yy` | Copy (yank) a line |
| `yw` | Copy (yank) a word |
| `p` | Paste after cursor |
| `P` | Paste before cursor |

---

## 🔍 Search and Replace

| Command | Action |
|-------|-------|
| `/pattern` | Search forward |
| `?pattern` | Search backward |
| `n` | Repeat search forward |
| `N` | Repeat search backward |
| `:%s/old/new/g` | Replace all occurrences in file |
| `:s/old/new/g` | Replace all occurrences in current line |

---

## 🗂 Working with Multiple Files

| Command | Action |
|-------|-------|
| `:e filename` | Open a new file |
| `:w` | Save file |
| `:wq` | Save and exit |
| `:q!` | Quit without saving |
| `:split filename` | Horizontal split and open file |
| `:vsplit filename` | Vertical split and open file |
| `Ctrl + w + w` | Switch between split screens |

---

## ✅ Summary

VI editor is built around **modal editing and keyboard-driven commands**. Learning these shortcuts allows faster navigation, efficient editing, and effective multitasking across files.

---
