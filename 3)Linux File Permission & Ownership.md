Got it — you want a **clean, general list of commands** (not your full story), just the essential commands you learned today.

Here is the **simple, general-purpose command cheat sheet** 👇
Perfect for GitHub, studying, or quick reference.

---

# 📘 **Linux File Permission & Ownership — Command Cheat Sheet**

## 👤 **User Switching Commands**

```
su - <username>
exit
whoami
```

---

# 📂 **File & Directory Commands**

```
ls
ls -l
ls -ld <directory>
cat <file>
echo "text" > <file>
mv <source> <destination>
```

---

# 🔐 **Permission Commands (`chmod`)**

### Change permissions (symbolic)

```
chmod u+r <file>      # add read for owner
chmod g+w <file>      # add write for group
chmod o+r <file>      # add read for others
chmod u-x <file>      # remove execute for owner
```

### Change permissions (numeric)

```
chmod 600 <file>      # owner read/write
chmod 644 <file>      # owner read/write, others read
chmod 755 <file>      # owner all, others read/execute
chmod 770 <dir>       # owner/group full access
```

---

# 👑 **Ownership Commands (`chown`, `chgrp`)**

```
chown <user> <file>
chown <user>:<group> <file>
chgrp <group> <file>
```

---

# 👥 **Group Management**

```
groupadd <groupname>
usermod -aG <groupname> <username>
```

---

# 🗂️ **Directory Permission Practice**

```
chmod 755 <directory>     # allow others to enter directory
chmod 700 <directory>     # restrict directory to owner
```

---

# 📦 **Moving Files Between Users**

```
mv <file> <destination>         # normal move
sudo mv <file> <destination>    # if moving into another user's home
```

---

# 🧭 **Useful Concepts**

These are not commands, but essential knowledge:

* `r` = read
* `w` = write
* `x` = execute / enter directory
* Directory needs `x` permission to access files inside
* `chown` changes file **owner**, not location
* `chmod` changes file **permissions**
* `mv` moves or renames files

---

If you want, I can format this as a **GitHub README.md** or provide a **PDF cheat sheet**.
