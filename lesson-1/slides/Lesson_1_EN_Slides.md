---
marp: true
theme: default
class: invert
---

# 🔐 Python + Cybersecurity
## Lesson 1: Python Thinks Like a Hacker

---

# Agenda

1. **Mindset:** Attacker vs. Defender
2. **Setup:** Python & VS Code
3. **Basics:** Variables, Loops, & Lists
4. **Tool:** The `requests` Library
5. **Recon:** Reading HTTP Headers
6. **Attack:** Intro to XSS (Cross-Site Scripting)

---

# 🧠 The Cybersecurity Mindset

<div class="columns">
<div>

### The Attacker ⚔️
- Needs to find **one** open door.
- Looks for patterns and mistakes.
- "How can I break this?"

</div>
<div>

### The Defender 🛡️
- Must secure **all** doors.
- Needs to know how the attacker thinks.
- "How can I fix this?"

</div>
</div>

---

# 🐍 Python Fundamentals

### Variables
Containers for storing data values.

```python
target_url = "https://example.com"
port = 80
is_secure = False
```

### Lists
Ordered collection of items.

```python
admin_pages = ["/admin", "/login", "/config"]
```

---

# 🔄 Loops (Automation)

Hackers don't type manually; they script!

```python
for page in admin_pages:
    print("Scanning: " + page)
```

**Output:**
```
Scanning: /admin
Scanning: /login
Scanning: /config
```

---

# 🌐 The `requests` Library

Python's way of browsing the web.

```python
import requests

response = requests.get("https://example.com")

print(response.status_code) # 200 = OK, 404 = Not Found
print(response.text)        # The HTML content
```

---

# 🕵️ Reading HTTP Headers

Hidden metadata sent by the server.

**Key Security Headers:**
- `Strict-Transport-Security`: Enforce HTTPS
- `X-Frame-Options`: Prevent site from being put in an iframe (Clickjacking)
- `Content-Security-Policy`: Restrict where resources can load from and reduce XSS risk

Missing a header is a reason to investigate further, not automatic proof of a bug.

---

# 💥 Intro to XSS (Cross-Site Scripting)

Injecting malicious scripts into trusted websites.

**A Red Flag:** `<script>` tags in user input.

A `<script>` tag alone does not prove XSS. What matters is whether attacker-controlled input can be injected and executed.

```python
# Simple Python check
if "<script>" in response.text:
    print("⚠️ Review needed: <script> pattern found.")
```

---

# 🎓 Wrap Up

- **Python** is a powerful tool for automation.
- **Modules** like `requests` let us interact with the network.
- **Security Headers** are the first line of defense.
- **XSS** checks often start with simple patterns, but real verification needs context.

**Next time:** Files, Logs, and Digital Forensics!
