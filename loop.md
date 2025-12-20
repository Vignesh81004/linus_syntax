Great 👍 since you’re **just starting with shell scripting**, let’s learn **loops step-by-step** in a **simple and practical way**.

---

## 🔁 What is a Loop in Shell Scripting?

A **loop** is used to **repeat a block of code multiple times** until a condition is met.

In shell scripting, the **main loops** are:

1. `for` loop
2. `while` loop
3. `until` loop

---

# 1️⃣ `for` Loop (Most Common & Beginner-Friendly)

### 👉 Use when you **know how many times** to repeat

### 🔹 Basic Syntax

```bash
for variable in list
do
  commands
done
```

---

### ✅ Example 1: Print numbers from 1 to 5

```bash
#!/bin/bash

for i in 1 2 3 4 5
do
  echo $i
done
```

📌 **Explanation**

* `i` → variable
* `1 2 3 4 5` → list
* `$i` → current value

---

### ✅ Example 2: Print Hello 5 times

```bash
#!/bin/bash

for i in 1 2 3 4 5
do
  echo "Hello"
done
```

---

### ✅ Example 3: Using range `{ }`

```bash
#!/bin/bash

for i in {1..10}
do
  echo "Number: $i"
done
```

📌 `{1..10}` → generates numbers from 1 to 10

---

### ✅ Example 4: Print files in a directory

```bash
#!/bin/bash

for file in *
do
  echo $file
done
```

📌 `*` → all files and folders in current directory

---

# 2️⃣ `while` Loop

### 👉 Use when you **don’t know** how many times to repeat

(loop runs **while condition is true**)

### 🔹 Syntax

```bash
while [ condition ]
do
  commands
done
```

---

### ✅ Example 1: Print numbers 1 to 5

```bash
#!/bin/bash

i=1
while [ $i -le 5 ]
do
  echo $i
  i=$((i+1))
done
```

📌 **Explanation**

* `-le` → less than or equal
* `i=$((i+1))` → increment

---

### ✅ Example 2: Read input until user types "exit"

```bash
#!/bin/bash

while true
do
  read -p "Enter something (type exit to quit): " input
  if [ "$input" = "exit" ]; then
    break
  fi
  echo "You typed: $input"
done
```

---

# 3️⃣ `until` Loop

### 👉 Opposite of `while`

(loop runs **until condition becomes true**)

### 🔹 Syntax

```bash
until [ condition ]
do
  commands
done
```

---

### ✅ Example: Print numbers 1 to 5

```bash
#!/bin/bash

i=1
until [ $i -gt 5 ]
do
  echo $i
  i=$((i+1))
done
```

📌 `-gt` → greater than

---

# 4️⃣ Loop with C-Style Syntax (Very Common)

```bash
#!/bin/bash

for ((i=1; i<=5; i++))
do
  echo "Count: $i"
done
```

📌 Similar to **C / Java / Python range loop**

---

# 🔥 Loop Control Statements

## 🛑 `break` (stop loop)

```bash
for i in {1..10}
do
  if [ $i -eq 5 ]; then
    break
  fi
  echo $i
done
```

---

## ⏭️ `continue` (skip current iteration)

```bash
for i in {1..5}
do
  if [ $i -eq 3 ]; then
    continue
  fi
  echo $i
done
```

---

# 📌 Common Test Conditions (Very Important)

| Operator | Meaning            |
| -------- | ------------------ |
| `-eq`    | equal              |
| `-ne`    | not equal          |
| `-lt`    | less than          |
| `-le`    | less than equal    |
| `-gt`    | greater than       |
| `-ge`    | greater than equal |

---

# 🧠 Beginner Practice Tasks (Try These 💪)

1. Print numbers from **1 to 50**
2. Print **even numbers only**
3. Print **Hello 10 times with count**
4. Loop through files and print only `.txt` files
5. Ask user a number and print its **multiplication table**

---

If you want 👉 next I can teach:

* **Loops with arrays**
* **Nested loops**
* **Real-time examples (log monitoring, services check)**
* **Mini shell script projects**

Just tell me 👍
