Great question 👍
You’re learning the **right things at the right time**.
Let’s clearly cover **ALL condition operators in shell scripting**, with **examples** and **how to use them** (very beginner-friendly).

---

# 🔹 1. Number (Integer) Comparison Operators

Used **inside `[ ]`** for comparing numbers.

| Operator | Meaning               |
| -------- | --------------------- |
| `-eq`    | Equal to              |
| `-ne`    | Not equal to          |
| `-gt`    | Greater than          |
| `-lt`    | Less than             |
| `-ge`    | Greater than or equal |
| `-le`    | Less than or equal    |

---

### ✅ Example: Number comparison

```bash
#!/bin/bash

echo "Enter a number:"
read num

if [ $num -ge 10 ]
then
    echo "Number is 10 or greater"
else
    echo "Number is less than 10"
fi
```

### 🧠 How it works

* `-ge` → checks **greater than OR equal**
* Always keep **spaces** inside `[ ]`

📌 **Syntax to remember**

```bash
[ number1 -operator number2 ]
```

---

# 🔹 2. String Comparison Operators

Used to compare **text / words**.

| Operator | Meaning             |
| -------- | ------------------- |
| `=`      | Equal               |
| `!=`     | Not equal           |
| `-z`     | String is empty     |
| `-n`     | String is NOT empty |

---

### ✅ Example: String equals

```bash
#!/bin/bash

echo "Enter your name:"
read name

if [ "$name" = "admin" ]
then
    echo "Welcome Admin"
else
    echo "You are a normal user"
fi
```

### 🧠 Why quotes?

```bash
"$name"
```

* Prevents errors if input is empty or has spaces

---

### ✅ Example: Check empty string

```bash
#!/bin/bash

echo "Enter something:"
read text

if [ -z "$text" ]
then
    echo "You entered nothing"
else
    echo "You entered: $text"
fi
```

---

📌 **Syntax to remember**

```bash
[ "$string1" = "$string2" ]
[ -z "$string" ]
[ -n "$string" ]
```

---

# 🔹 3. File & Directory Test Operators (VERY IMPORTANT)

Used to check **files & folders**.

| Operator | Meaning                  |
| -------- | ------------------------ |
| `-f`     | File exists              |
| `-d`     | Directory exists         |
| `-e`     | File or directory exists |
| `-r`     | Read permission          |
| `-w`     | Write permission         |
| `-x`     | Execute permission       |
| `-s`     | File is NOT empty        |

---

### ✅ Example: Check file exists

```bash
#!/bin/bash

if [ -f "/etc/passwd" ]
then
    echo "File exists"
else
    echo "File does not exist"
fi
```

---

### ✅ Example: Check directory

```bash
#!/bin/bash

echo "Enter directory name:"
read dir

if [ -d "$dir" ]
then
    echo "Directory exists"
else
    echo "Directory not found"
fi
```

---

### ✅ Example: Check permissions

```bash
#!/bin/bash

file="test.sh"

if [ -x "$file" ]
then
    echo "Executable permission present"
else
    echo "No execute permission"
fi
```

---

📌 **Syntax to remember**

```bash
[ -f file ]
[ -d directory ]
[ -r file ]
[ -w file ]
[ -x file ]
```

---

# 🔹 4. Logical Operators (Multiple Conditions)

| Operator | Meaning         |   |                |
| -------- | --------------- | - | -------------- |
| `-a`     | AND             |   |                |
| `-o`     | OR              |   |                |
| `&&`     | AND (preferred) |   |                |
| `        |                 | ` | OR (preferred) |
| `!`      | NOT             |   |                |

---

### ✅ Example: AND condition

```bash
#!/bin/bash

echo "Enter age:"
read age

if [ $age -ge 18 ] && [ $age -le 60 ]
then
    echo "Eligible"
else
    echo "Not eligible"
fi
```

---

### ✅ Example: OR condition

```bash
if [ "$user" = "root" ] || [ "$user" = "admin" ]
then
    echo "Access granted"
fi
```

---

### ✅ Example: NOT condition

```bash
if [ ! -f "data.txt" ]
then
    echo "File does not exist"
fi
```

---

📌 **Syntax to remember**

```bash
[ condition1 ] && [ condition2 ]
[ condition1 ] || [ condition2 ]
[ ! condition ]
```

---

# 🔹 5. Command Exit Status Condition

Every command returns:

* `0` → success
* `non-zero` → failure

---

### ✅ Example

```bash
#!/bin/bash

ls /tmp

if [ $? -eq 0 ]
then
    echo "Command successful"
else
    echo "Command failed"
fi
```

📌 `$?` → stores last command result

---

# 🧠 VERY IMPORTANT RULES (EXAM & REAL LIFE)

✔ Space is **mandatory**

```bash
[ $a -eq $b ]   # correct
[$a -eq $b]     # wrong ❌
```

✔ Always quote strings

```bash
"$var"
```

✔ Use `&&` and `||` instead of `-a` `-o`

---

# 📌 Final Quick Cheat Sheet

```bash
# Numbers
-eq -ne -gt -lt -ge -le

# Strings
= != -z -n

# Files
-f -d -e -r -w -x -s

# Logical
&& || !

# Exit status
$?
```

---

## 🎯 Practice Task (Do Now)

Write a script that:

1. Asks for a filename
2. Checks:

   * file exists
   * file is writable
3. Prints appropriate message

Send your script here — I’ll correct it like a mentor 👨‍🏫
