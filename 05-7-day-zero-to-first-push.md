# 7-Day Challenge — Zero to First Push

Target: 15 minutes per day. You got this.

## DAY 1 — GitHub + Git

**Goal:** Create GitHub account, install Git, configure Git.
**Time needed:** 15 minutes.
**Steps:** Follow the instructions in `02-how-to-install.md`.

**Commands:**
```bash
git --version
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

**Explanation:** You are installing the software and signing your digital notebook.
**Wet-lab analogy:** You bought a new lab notebook and wrote your name on the cover.

**Success:**
- [ ] I have a GitHub account
- [ ] Git is installed
- [ ] Git has my name
- [ ] Git has my email

## DAY 2 — Create Your Private Lab Book

**Goal:** Create a repository on GitHub.
**Time needed:** 5 minutes.
**Steps:**
1. Go to GitHub.
2. Click: **New** → **Repository**
3. Name: `my-first-lab-book`
4. Select: **Private**
5. Click **Create repository**.

**Explanation:** A repository is a project folder that Git watches.
**Wet-lab analogy:** You just placed a new binder on your shelf to hold your notes.

**Success:** You can see your new empty private repository on GitHub.

## DAY 3 — Clone It

**Goal:** Copy the online repository to your computer.
**Time needed:** 10 minutes.
**Steps:**
Copy the repository URL from GitHub.

**Commands:**
```bash
git clone YOUR_REPOSITORY_URL
```
Replace `YOUR_REPOSITORY_URL` with the URL GitHub gives you.

Then:
```bash
cd my-first-lab-book
```
**Explanation:** **cd** means "change directory". You are opening the folder.

Create a file named `first-note.md` and put inside:
```markdown
# My First Lab Note
Today I created my first Git repository.
```

Then run:
```bash
git status
```
**Explanation:** Git tells you what changed in your folder.
**Wet-lab analogy:** You are opening your binder and placing a loose piece of paper inside.

**Success:** Git tells you that `first-note.md` is an untracked file.

## DAY 4 — First Commit and Push

**Goal:** Save your work and send it to GitHub.
**Time needed:** 10 minutes.
**Commands:**

```bash
git status
```

Then:
```bash
git add first-note.md
```
**Explanation:** **add** tells Git which change you want to include in the next recorded version.

Then:
```bash
git status
```

Then:
```bash
git commit -m "Add my first lab note"
```
**Explanation:** **commit** records a version in Git history.

Then:
```bash
git push
```
**Explanation:** **push** sends your committed history to GitHub.

Now, refresh GitHub in your browser.
**Wet-lab analogy:** You recorded your results permanently in the notebook, and stored a copy in the secure online locker.

**Success:**
- [ ] I created a file
- [ ] I checked git status
- [ ] I staged the file
- [ ] I committed it
- [ ] I pushed it
- [ ] I can see it on GitHub

## DAY 5 — Learn Branches

**Goal:** Make a safe experimental copy.
**Time needed:** 10 minutes.

**Explanation:** A **branch** is a separate line of work.
**Wet-lab analogy:** Making a safe experimental copy of your main protocol to try a new reagent.

**Commands:**
```bash
git switch -c experiment
```
Make a small change to your `first-note.md` file.

Then:
```bash
git status
git add first-note.md
git commit -m "Try an experiment"
```

Return to the main branch:
```bash
git switch main
```
The experimental change may no longer appear in the working file. You can bring it back by merging later.

**Success:** I understand that a branch lets me experiment separately from the main line.

## DAY 6 — Explore a Real Scientific Repository

**Goal:** Learn from others.
**Time needed:** 15 minutes.
**Steps:**
1. Choose one repository from the Free University list (`04-free-university-7-repos.md`).
2. Open the repository.
3. Read the README.
4. Look at the documentation.
5. Look at Issues if available.
6. Find one issue.
7. Identify what problem the issue describes.

**Explanation:** Issues are where projects can track bugs, questions, tasks and improvements.
**Wet-lab analogy:** An issue is similar to recording a problem with an experiment instead of silently forgetting it.

## DAY 7 — Build Your Own Digital Lab Notebook

**Goal:** Start a real project.
**Time needed:** 15 minutes.
**Steps:**
Copy `template/README_template.md` and use it for a real mini-project.

Fill in:
* Goal
* Date
* What I tried
* What broke
* How I fixed it
* Next

**Commands:**
```bash
git status
git add README.md
git commit -m "Add my first project notes"
git push
```

**Success:** I now have a real GitHub project containing my own scientific thinking and its history.

You finished. ✅

You now know:
* **status**
* **add**
* **commit**
* **push**
* **pull**
* **clone**
* **branch**
