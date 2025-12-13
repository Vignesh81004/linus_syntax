 📁 Linux File & Directory Management Commands

## 1️⃣ `ls` – List files and directories

**Syntax**

```bash
ls
ls [options] [path]
```

**Examples**

```bash
ls            # list items in current directory
ls -l         # long listing
ls -a         # show hidden files
ls /etc       # list contents of /etc
```

---

## 2️⃣ `cd` – Change directory

**Syntax**

```bash
cd path/to/directory
```

**Examples**

```bash
cd /home          # go to /home
cd ..             # go back one folder
cd ~              # go to your home directory
cd /var/log       # go to /var/log
```

---

## 3️⃣ `pwd` – Print working directory

**Syntax**

```bash
pwd
```

**Example**

```bash
pwd   # shows /home/vignesh
```

---

## 4️⃣ `mkdir` – Create a directory

**Syntax**

```bash
mkdir directory_name
mkdir -p parent/child
```

**Examples**

```bash
mkdir test_folder
mkdir -p cloud/linux/commands
```

---

## 5️⃣ `rmdir` – Remove an empty directory

**Syntax**

```bash
rmdir folder_name
```

**Example**

```bash
rmdir empty_folder
```

> ⚠️ Only works if the folder is **empty**.

---

## 6️⃣ `rm` – Remove files or directories

**Syntax**

```bash
rm file_name
rm -r folder_name
rm -f file_name
```

**Examples**

```bash
rm test.txt               # delete file
rm -r project_folder      # delete folder + contents
rm -f force.txt           # delete without confirmation
```

> ⚠️ **Dangerous:** Files deleted with `rm` cannot be recovered.

---

## 7️⃣ `cp` – Copy files

**Syntax**

```bash
cp source destination
```

**Examples**

```bash
cp file1.txt file2.txt
cp file.txt /home/vignesh/
```

---

## 8️⃣ `cp -r` – Copy directories recursively

**Syntax**

```bash
cp -r source_dir destination_dir
```

**Example**

```bash
cp -r folder1 folder2
```

---

## 9️⃣ `mv` – Move or rename files/directories

**Syntax**

```bash
mv old_name new_name
mv file /path/to/location
```

**Examples**

```bash
mv old.txt new.txt
mv file.txt /tmp/
mv folder1 folder2
```

---

# 📄 File Viewing & Editing Commands

## 🔟 `cat` – Show file content

**Syntax**

```bash
cat file.txt
```

**Example**

```bash
cat notes.txt
```

---

## 1️⃣1️⃣ `tac` – Show file content in reverse

**Syntax**

```bash
tac file.txt
```

**Example**

```bash
tac logs.txt
```

---

## 1️⃣2️⃣ `less` – View file with scrolling

**Syntax**

```bash
less file.txt
```

**Controls**

* `q` → quit
* `↑ / ↓` → scroll
* `/text` → search

---

## 1️⃣3️⃣ `more` – View file page by page

**Syntax**

```bash
more file.txt
```

> Less powerful than `less`.

---

## 1️⃣4️⃣ `head` – Show first lines of a file

**Syntax**

```bash
head -n number file.txt
```

**Examples**

```bash
head -n 5 file.txt
head file.txt        # default: 10 lines
```

---

## 1️⃣5️⃣ `tail` – Show last lines of a file

**Syntax**

```bash
tail -n number file.txt
```

**Examples**

```bash
tail -n 20 logs.txt
tail -f logs.txt      # live updating logs
```

---

## 1️⃣6️⃣ `nano` – Simple text editor

**Syntax**

```bash
nano file.txt
```

**Controls**

* `Ctrl + O` → Save
* `Ctrl + X` → Exit

---

## 1️⃣7️⃣ `vi` / `vim` – Advanced text editor

**Syntax**

```bash
vi file.txt
```

### Basic Usage

**Insert mode**

```
i
```

**Command mode**

```
Esc
```

**Save & Quit**

```
:w     # save
:q     # quit
:wq    # save & quit
:q!    # force quit without saving
```

---

## 1️⃣8️⃣ `echo` – Write or append text

### Overwrite file

```bash
echo "Hello" > file.txt
```

### Append to file

```bash
echo "Hello" >> file.txt
```

---
