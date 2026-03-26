---
marp: true
theme: default
class: invert
---

# 🔐 Python + Cybersecurity
## Lesson 2: Data, Files & Forensics

---

# Agenda

1.  **Process:** Digital Forensics ("What happened?")
2.  **Input:** Reading Files in Python
3.  **Data:** Parsing Strings & Lists
4.  **Logic:** Dictionaries & Counting
5.  **Output:** Identifying an Attack

---

# 🕵️ Digital Forensics

When a system is hacked, we don't guess. We look for **evidence**.

**Evidence is usually found in Logs.**

A **Log** is a file where a server writes down what it is doing.
> "10:00 AM - User 'Admin' logged in."
> "10:05 AM - User 'Hacker' failed password."

---

# 📂 Reading Files

Python makes it easy to open files.

```python
# The 'with' block handles closing the file automatically
with open("logs.txt", "r") as file:
    content = file.read()
    print(content)
```

- `"r"` = Read Mode
- `"w"` = Write Mode (Overwrites!)
- `"a"` = Append Mode (Adds to end)

---

# ✂️ Parsing Strings

Logs are just long strings of text. We need to cut them up.

**The `.split()` method:**

```python
line = "192.168.1.5 - GET /index.html"
parts = line.split(" - ")
# Result: ["192.168.1.5", "GET /index.html"]

ip = parts[0]
action = parts[1]
```

---

# 📚 Dictionaries (Key-Value Pairs)

If we want to count how many times an IP appears, a **List** is hard to use.
A **Dictionary** is like a real dictionary: You look up a word (Key) to get a definition (Value).

```python
# Key: IP Address, Value: Count
counts = {
    "192.168.1.1": 5,
    "10.0.0.5": 120
}

# Accessing data
print(counts["10.0.0.5"]) # Prints 120
```

---

# ⚔️ The Attack Pattern: Brute Force

**Brute Force:** Trying every possible password until one works.

**The Log Signature:**
1.  Same IP address...
2.  Trying to `POST /login`...
3.  Getting `401 Unauthorized` errors...
4.  ...**Hundreds** of times per minute.

---

# 🎓 Summary

- **Forensics** is about reading the history (logs).
- **Files** are opened with `open()` and usually read with loops.
- **Parsing** turns text into data (`.split()`).
- **Dictionaries** help us count and group data.
- **Brute Force** attacks are loud and easy to spot in logs!

**Next Lesson:** Encryption & Secrets!
