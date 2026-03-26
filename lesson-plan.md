Here's the full plan — 4 in-person sessions spaced two weeks apart, each with a 2-hour digital lesson in between.

---

# 🔐 Python + Cybersecurity: Foundational Course Plan

**Structure:** 4 × 4-hour in-person lessons | 3 × 2-hour digital lessons between them
**Audience:** Students with HTML/CSS experience and basic networking knowledge
**Goal:** General foundational knowledge in Python and cybersecurity

---

## 🏫 Lesson 1 (In-Person, 4 hrs) — "Python Thinks Like a Hacker"

**Theme:** Python basics through a web security lens — leverages their existing HTML knowledge immediately.

| Time | Activity |
|---|---|
| 0:00–0:30 | Intro: What is cybersecurity? The attacker/defender mindset. Ethics & the law. |
| 0:30–1:15 | Python fundamentals: variables, strings, lists, loops — using HTML snippets as data |
| 1:15–2:00 | The `requests` library: fetch a real web page and print its content with Python |
| 2:00–2:15 | Break |
| 2:15–3:00 | Reading HTTP headers — what do they tell us? Writing a script to check for security headers |
| 3:00–3:45 | Intro to XSS: manually find a `<script>` tag in sample HTML, then automate the search with Python |
| 3:45–4:00 | Wrap-up: what did we learn, Q&A, preview of digital homework |

**Key Python Concepts:** variables, strings, lists, loops, `print()`, `requests`, basic conditionals

**Key Security Concepts:** HTTP, security headers, XSS basics, ethical use

**Students leave with:** A working script that fetches a URL and reports whether key security headers are present or missing

---

## 💻 Digital Lesson A (Homework, 2 hrs) — "Reading the Web Like a Machine"
*Completed in the two weeks between Lesson 1 and Lesson 2*

- **Hour 1 — Guided:** Video/walkthrough extending the header-checker: add functions, loop over multiple URLs from a list, output results neatly
- **Hour 2 — Independent:** Students modify the script to also flag pages that contain inline `<script>` tags or missing `<meta charset>` tags

**Deliverable:** Submit their extended scanner script + a short paragraph explaining one security header they researched

---

## 🏫 Lesson 2 (In-Person, 4 hrs) — "Data, Files & Digital Forensics"

**Theme:** Python data structures and file handling — taught by analyzing real-looking server logs.

| Time | Activity |
|---|---|
| 0:00–0:20 | Homework review: students demo their scanners, class discussion |
| 0:20–1:00 | Python dictionaries and file I/O: reading a `.txt` log file line by line |
| 1:00–1:45 | Parsing log data: extract IP addresses, timestamps, and status codes using `split()` and string methods |
| 1:45–2:00 | Break |
| 2:00–2:45 | Counting with dictionaries: which IPs appear most often? Flag anything over a threshold |
| 2:45–3:30 | Security tie-in: what does a brute-force login attempt look like in a log? Students hunt for the pattern |
| 3:30–3:50 | Intro to `csv` module — logs often come as CSVs in the real world |
| 3:50–4:00 | Wrap-up, Q&A, preview of digital homework |

**Key Python Concepts:** dictionaries, file I/O, string methods, `csv` module, functions

**Key Security Concepts:** Log analysis, brute-force attack patterns, IP reputation, anomaly detection

**Students leave with:** A log analysis script that reads a provided sample log and flags suspicious IPs

---

## 💻 Digital Lesson B (Homework, 2 hrs) — "Secrets & Hashing"
*Completed in the two weeks between Lesson 2 and Lesson 3*

- **Hour 1 — Guided:** Intro to `hashlib` — what is a hash? Hash some strings, show that the same input always produces the same output. Demonstrate why you can't hash-and-store passwords without salting
- **Hour 2 — Independent:** Students write a script that takes a list of common passwords, hashes them with SHA-256, and checks if any match a provided "stolen hash" — a simplified dictionary attack simulation

**Deliverable:** Submit their dictionary attack script + a written reflection: why is salting important?

---

## 🏫 Lesson 3 (In-Person, 4 hrs) — "Cryptography & Secrets in Code"

**Theme:** Functions, modules, and cryptography — students learn how real systems protect (and fail to protect) data.

| Time | Activity |
|---|---|
| 0:00–0:20 | Homework review: demo the dictionary attack scripts, discuss real-world data breaches |
| 0:20–1:00 | Python functions deep-dive: parameters, return values, scope — building reusable crypto utilities |
| 1:00–1:45 | `hashlib` in depth: MD5 vs SHA-1 vs SHA-256, why MD5 is broken, salting passwords properly |
| 1:45–2:00 | Break |
| 2:00–2:45 | Symmetric encryption with the `cryptography` library (Fernet): encrypt and decrypt a message |
| 2:45–3:30 | Build a simple "password vault": store encrypted credentials in a file, retrieve and decrypt them |
| 3:30–3:50 | Security tie-in: what went wrong in famous breaches (LinkedIn, RockYou)? Tie back to code |
| 3:50–4:00 | Wrap-up, Q&A, preview of digital homework |

**Key Python Concepts:** functions, modules, `hashlib`, `cryptography` (Fernet), file I/O revisited

**Key Security Concepts:** Hashing vs encryption, salting, symmetric encryption, real-world breach analysis

**Students leave with:** A working (simple) password vault they built themselves

---

## 💻 Digital Lesson C (Homework, 2 hrs) — "Talking to the Network"
*Completed in the two weeks between Lesson 3 and Lesson 4*

- **Hour 1 — Guided:** Python `socket` basics — what is a socket? Write a simple TCP client that connects to a server and reads a banner. Tie back to their TCP/IP knowledge
- **Hour 2 — Independent:** Students write a script that attempts to connect to ports 22, 80, and 443 on a provided local VM IP, and reports which are open — a mini port scanner

**Deliverable:** Submit their port scanner script + a diagram or written explanation of what happens at the TCP level during each connection attempt

---

## 🏫 Lesson 4 (In-Person, 4 hrs) — "Building Your Security Toolkit"

**Theme:** Bringing everything together — networking in Python, tool-building, and thinking like a professional.

| Time | Activity |
|---|---|
| 0:00–0:20 | Homework review: demo port scanners, discuss what banners reveal and why attackers love them |
| 0:20–1:00 | Expand the port scanner: loop over a range of ports, add timing, format output cleanly |
| 1:00–1:45 | Intro to classes (OOP basics): refactor the scanner into a reusable `Scanner` class |
| 1:45–2:00 | Break |
| 2:00–2:45 | Combining tools: build a mini "recon script" that takes a target URL, checks headers, resolves the IP, and scans common ports |
| 2:45–3:15 | Live demo: run the toolkit against DVWA (local VM) — students see their code work on a real target |
| 3:15–3:45 | Where to go next: TryHackMe, PicoCTF, Python for pentesters, career paths in security |
| 3:45–4:00 | Final Q&A, course wrap-up, certificates / recognition |

**Key Python Concepts:** OOP basics (classes), combining modules, argparse (optional), clean output formatting

**Key Security Concepts:** Reconnaissance, responsible disclosure, professional ethics, attack surface

**Students leave with:** A multi-function personal security toolkit and a roadmap for continued learning

---

## 📦 What Students Build Across the Course

| # | Project | Skills Demonstrated |
|---|---|---|
| 1 | Security Header Scanner | HTTP, `requests`, loops, functions |
| 2 | Log Analyser & IP Flagging Tool | File I/O, dictionaries, anomaly detection |
| 3 | Password Vault | Hashing, encryption, functions, modules |
| 4 | Mini Recon Toolkit | Sockets, OOP, combining all prior tools |

---

## 🛠️ Setup Checklist for Instructors
- Python 3.10+ installed on all student machines
- VS Code with Python extension
- Libraries: `requests`, `cryptography` (`pip install` in class)
- VirtualBox + DVWA or a pre-configured TryHackMe room for Lesson 4
- Sample files ready: a fake log file (CSV + TXT), a set of pre-hashed passwords for the dictionary attack exercise

---

This is designed to be **immediately practical** at every stage — students are never just reading theory, they're always running something. Want me to create any specific handouts, starter code templates, or a student-facing syllabus for any of the lessons?