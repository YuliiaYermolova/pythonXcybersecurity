[🇳🇴 Norsk Versjon](README_NO.md)

# Python + Cybersecurity Course

Welcome to the Python + Cybersecurity course! This repository contains all the lesson materials, notebooks, and slides.

## Student Workflow

Follow these steps to set up your own copy of the course materials and keep it updated as new lessons are released.

### 1. Fork the Repository
First, create your own copy of this repository on GitHub.
1. Go to the main repository page: [https://github.com/Cha-IT/pythonXcybersecurity](https://github.com/Cha-IT/pythonXcybersecurity)
2. Click the **Fork** button in the top right corner.
3. This creates a copy under your own GitHub account.

### 2. Clone Your Fork in VS Code
Now, download your copy to your computer.
1. Open **VS Code**.
2. Press `Ctrl+Shift+P` (or `Cmd+Shift+P` on Mac) to open the Command Palette.
3. Type `Git: Clone` and select it.
4. Paste the URL of **YOUR FORKED REPOSITORY** (e.g., `https://github.com/YOUR_USERNAME/pythonXcybersecurity.git`).
5. Choose a folder on your computer to save it.
6. When asked, click **Open** to open the new repository in VS Code.

### 3. Add the Upstream Remote
To get updates from the teacher (new lessons), you need to tell Git where the original repository is.
1. Open the Terminal in VS Code (`Ctrl+` ` or `Terminal > New Terminal`).
2. Run the following command exactly:
   ```bash
   git remote add upstream https://github.com/Cha-IT/pythonXcybersecurity.git
   ```
3. To verify it worked, run:
   ```bash
   git remote -v
   ```
   You should see both `origin` (your fork) and `upstream` (the teacher's repo).

### 4. How to Get Updates (New Lessons)
When a new lesson is released, follow these steps to download it into your project:

1. Open the Terminal in VS Code.
2. Run these commands:
   ```bash
   git fetch upstream
   git merge upstream/main
   ```
3. Push the updates to your own GitHub fork:
   ```bash
   git push origin main
   ```

Now you have the latest files!

## Troubleshooting
- **Merge Conflicts:** If you edited a file that was also changed in the update, Git might complain about a "conflict". Since you will be working in your own files or localized notebooks, this shouldn't happen often. If it does, VS Code will help you resolve it.
- **Branch Name:** This guide assumes the main branch is named `main`. If it is named `master`, simply replace `main` with `master` in the commands above.
- **Permission Denied:** Make sure you are logged into GitHub in VS Code.
