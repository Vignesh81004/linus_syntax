
# ✅ **Start Practicing Vim**

### **Open Vim**

```bash
vim practice.txt
```

This creates/opens a file called *practice.txt* where you can try everything.

---

# 🎯 **1. Modes in Vim (Practice Steps)**

## **Normal Mode**

(Default mode — used for navigation commands)

Press:

```
Esc
```

You'll almost always return to Normal mode with `Esc`.

---

## **Insert Mode**

Try these inside Vim:

* `i` → insert before cursor
* `I` → insert at beginning of the line
* `a` → insert after cursor
* `A` → append at end of line
* `o` → new line below
* `O` → new line above

**Exercise:**
Type these commands in order inside Vim:

```
iHello World<Esc>
oThis is a new line<Esc>
OInsert above<Esc>
```

---

## **Command Mode**

Press:

```
:
```

Then try:

```
:w     (save)
:q     (quit)
:wq    (save and quit)
:q!    (quit without saving)
```

---

# 🎯 **2. Navigation Practice**

Open a multi-line text inside Vim:

```
:read !seq 20
```

This inserts numbers 1 to 20 for practice.

Now try:

| Movement | Try This        |
| -------- | --------------- |
| `h`      | Move left       |
| `l`      | Move right      |
| `j`      | Move down       |
| `k`      | Move up         |
| `0`      | Start of line   |
| `^`      | First non-blank |
| `$`      | End of line     |
| `w`      | Next word       |
| `b`      | Previous word   |
| `gg`     | First line      |
| `G`      | Last line       |
| `:10`    | Go to line 10   |

---

# 🎯 **3. Insert Mode Shortcuts (Hands-On)**

While in normal mode:

| Shortcut | What to Do            |
| -------- | --------------------- |
| `i`      | Insert before cursor  |
| `I`      | Insert at beginning   |
| `a`      | Insert after cursor   |
| `A`      | Insert at end of line |
| `o`      | New line below        |
| `O`      | New line above        |
| `Esc`    | Return to Normal      |

**Exercise:**

```
Go to line 5 → press A → type " - edited" → Esc
```

---

# 🎯 **4. Editing Text (Practice Commands)**

Try the following on any line:

| Command  | Action                  |
| -------- | ----------------------- |
| `x`      | delete character        |
| `X`      | delete before cursor    |
| `dw`     | delete word             |
| `dd`     | delete line             |
| `d$`     | delete to end of line   |
| `d0`     | delete to start of line |
| `u`      | undo                    |
| `Ctrl+r` | redo                    |
| `yy`     | copy line               |
| `p`      | paste below             |
| `yw`     | copy word               |
| `P`      | paste above             |

**Exercise:**

```
Go to any line → type: dd → deletes line
Press: p → pastes it back
```

---

# 🎯 **5. Search & Replace**

Try:

```
/text     → search forward
?text     → search backward
n         → next match
N         → previous match
```

Replace examples:

Replace "foo" with "bar" in entire file:

```
:%s/foo/bar/g
```

Replace only in the current line:

```
:s/foo/bar/g
```

---

# 🎯 **6. Multiple Files in Vim**

Open another file:

```
:e file2.txt
```

Horizontal split:

```
:split file2.txt
```

Vertical split:

```
:vsplit file2.txt
```

Switch windows:

```
Ctrl + w + w
```

---

# 🚀 COMPLETE PRACTICE SESSION (DO THIS IN ORDER)

Copy and follow this:

1. Open Vim

   ```
   vim practice.txt
   ```
2. Enter some text using `i`, `A`, `o`
3. Navigate using `h j k l`, `$`, `gg`, `G`
4. Delete lines with `dd`, undo with `u`
5. Yank/paste using `yy`, `p`
6. Search inside file using `/word`
7. Replace using `:%s/old/new/g`
8. Practice splits

   ```
   :vsplit
   Ctrl+w w
   ```
9. Save and exit

   ```
   :wq
   ```
