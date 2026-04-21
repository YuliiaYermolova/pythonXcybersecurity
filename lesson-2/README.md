[🇳🇴 Norsk Versjon](README_NO.md)

# Lesson 2: Data, Files & Digital Forensics

This lesson focuses on how to handle data in Python by reading files and analyzing server logs to detect cyber attacks.

## 📂 Contents

- **notebooks/**: Interactive Jupyter Notebooks.
  - `Lesson_2_EN.ipynb`: English version.
  - `Lesson_2_NO.ipynb`: Norwegian version.
- **slides/**: Presentation slides.
  - `Lesson_2_EN_Slides.md`
  - `Lesson_2_NO_Slides.md`
- **data/**: Sample log files for analysis.
  - `server_logs.txt`: A simulated server log file containing normal traffic and a brute-force attack.

## 🚀 Getting Started

1.  **Open the Notebook:** Open `notebooks/Lesson_2_EN.ipynb` in VS Code.
2.  **Check the Data:** Ensure you can access `data/server_logs.txt`. The notebook is configured to look for `../data/server_logs.txt`.
3.  **Run the Cells:** Follow the instructions to learn how to open, read, and parse files.

## 🔍 Key Concepts

-   **File I/O:** `open()`, `read()`, `readlines()`.
-   **String Parsing:** `.split()`, `.strip()`.
-   **Dictionaries:** Key-Value pairs for counting data.
-   **Log Analysis:** Identifying suspicious patterns (Brute Force).

## Learning Goals

After this lesson, students should be able to:

- Read a log file into Python and explain why `with open(...)` is useful.
- Split a log line into meaningful parts such as IP address and status code.
- Use a dictionary to count repeated events.
- Explain why repeated `401` responses from the same IP can indicate a brute-force attack.

## Quick Self-Check

- What does the `with` statement help us do when working with files?
- Why do we split each log line before analyzing it?
- Why can many failed logins from one IP be suspicious?
