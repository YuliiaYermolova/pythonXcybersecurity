---
marp: true
theme: default
class: invert
---

# 🔐 Python + Cybersecurity
## Lesson 3: Cryptography & Secrets in Code

---

# Agenda

1. **Functions:** Writing reusable code
2. **Hashing:** The one-way trip
3. **Salting:** Defeating Rainbow Tables
4. **Encryption:** Locking and Unlocking
5. **Project:** Building a Password Vault

---

# 1. Functions
Stop coping and pasting code!

```python
def greet(name):
    return f"Hello, {name}!"

print(greet("Hacker"))
```

- **Define** once (`def`)
- **Call** many times
- **Return** a value

---

# 2. Hashing (One-Way)
A hash function turns data into a "fingerprint".
**You cannot reverse a hash.**

Good for:
- Storing passwords
- Checking file integrity

**Golden Rule:** NEVER store passwords in plain text!

---

# 3. Salting
If two users have the password `password123`, they get the same hash.
Hackers use **Rainbow Tables** to look up these common hashes.

**The Fix: Salting**
Add random data (salt) to the password before hashing.
`Hash(Salt + Password)` = Unique Hash

---

# 4. Encryption (Two-Way)
Unlike hashing, encryption is reversible... if you have the **Key**.

We use **Symmetric Encryption** (Fernet):
- One key to lock (encrypt)
- Same key to unlock (decrypt)

---

# 5. Project: Password Vault
We will build a script that:
1. Generates a secret key
2. Encrypts your passwords
3. Saves them to a file
4. Decrypts them when you need them

Educational demo only: a real password manager also needs secure key storage and authentication.

---

# Real World Failures
- **LinkedIn (2012):** Used SHA-1 (fast) without salt. Millions of passwords cracked.
- **RockYou (2009):** Stored passwords in plain text. Complete disaster.

**Takeaway:** meaningful security requires layers (Hashing + Salting + Encryption).
Our vault here is for learning, not production use.
