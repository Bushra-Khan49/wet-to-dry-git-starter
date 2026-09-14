# 7-Day Challenge — Zero to First Push

Target: 15 minutes per day. You got this.

**Important: Where are we working?**
It is incredibly common to get confused about *where* an action happens. Throughout this guide, pay attention to which of these three places we are using:
1. **GitHub Online (The Website):** Your web browser. This is the cloud where your secure copy lives.
2. **The Terminal:** The text-based command tool on your computer.
3. **GitHub Desktop (The App):** A visual program on your computer that does the exact same job as the Terminal, but with buttons. 

*Note: You only need to use **either** the Terminal **or** the Desktop App on your computer. You do not need to use both!*

---

## DAY 1 — GitHub + Git

**Goal:** Create an account, install the software, and sign your digital notebook.
**Time needed:** 15 minutes.
**Steps:** Follow the instructions in `02-how-to-install.md`.

**If using Terminal:**
```bash
git --version
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```
**If using GitHub Desktop App:**
Download the app, install it, and sign in with your GitHub account.

**Wet-lab analogy:** You bought a new lab notebook and wrote your name on the cover.

**Success:**
- [ ] I have a GitHub account
- [ ] Git (or GitHub Desktop) is installed
- [ ] Git has my name
- [ ] Git has my email

---

## DAY 2 — Create Your Private Lab Book

**Goal:** Create a repository on GitHub.
**Where:** **GitHub Online**
**Time needed:** 5 minutes.
**Steps:**
1. Go to GitHub in your web browser.
2. Click: **New** → **Repository**
3. Name: `my-first-lab-book`
4. Select: **Private**
5. Click **Create repository**.

**Explanation:** A repository is a project folder that Git watches.
**Wet-lab analogy:** You just placed a new binder on your shelf to hold your notes.

**Success:** You can see your new empty private repository on GitHub.

---

## DAY 3 — Clone It

**Goal:** Take the empty online folder and download a "linked" working copy to your computer.
**Time needed:** 10 minutes.

**Step 1: Get the link (GitHub Online)**
Copy the repository URL from GitHub (click the green **<> Code** button and copy the web URL).

**Step 2: Clone it to your computer (Choose Terminal OR App)**
*   **If using Terminal:**
    ```bash
    git clone YOUR_REPOSITORY_URL
    ```
    Then, open that folder:
    ```bash
    cd my-first-lab-book
    ```
    *(Explanation: **cd** means "change directory".)*
*   **If using GitHub Desktop App:**
    Go to **File** > **Clone Repository**. Click the **URL** tab, paste the link, and choose a folder on your computer to save it in. Click **Clone**.

**Step 3: Create a file (On your computer)**
Open your new `my-first-lab-book` folder using standard Windows Explorer or Mac Finder. Create a file named `first-note.md` and put this inside:
```markdown
# My First Lab Note
Today I created my first Git repository.
```
**Wet-lab analogy:** You are opening your binder and placing a loose piece of paper inside.

**Step 4: Check your status**
*   **If using Terminal:** Type `git status`. It will show `first-note.md` in red as an "untracked file".
*   **If using GitHub Desktop App:** Look at the left sidebar. You will see `first-note.md` appear there with a green `+`. The App runs `git status` for you visually!

**Success:** Git sees that `first-note.md` is a new, unrecorded file.

---

## DAY 4 — First Commit and Push

**Goal:** Tell Git to record the file you just made, and then upload that record to the internet.
**Time needed:** 10 minutes.

**Step 1: Stage and Commit (Recording locally)**
*   **If using Terminal:**
    ```bash
    git add first-note.md
    ```
    *(Explanation: **add** puts the file on the "tray" to be recorded).*
    ```bash
    git commit -m "Add my first lab note"
    ```
    *(Explanation: **commit** writes the record permanently into your local history).*
*   **If using GitHub Desktop App:**
    Make sure the box next to `first-note.md` is checked. At the bottom left in the "Summary" box, type *"Add my first lab note"*. Click the blue **Commit to main** button.

**Step 2: Push (Uploading to the cloud)**
*   **If using Terminal:**
    ```bash
    git push
    ```
    *(Explanation: **push** sends your committed history to GitHub).*
*   **If using GitHub Desktop App:**
    Click the **Push origin** button at the very top of the window.

**Step 3: Verify (GitHub Online)**
Refresh your GitHub repository in your web browser. You will now see `first-note.md` sitting securely on the internet!
**Wet-lab analogy:** You recorded your results permanently in the notebook, and stored a copy in the secure online locker.

**Success:**
- [ ] I created a file
- [ ] I checked status
- [ ] I staged the file
- [ ] I committed it
- [ ] I pushed it
- [ ] I can see it on GitHub

---

## DAY 5 — Learn Branches

**Goal:** Make a temporary "photocopy" where you can safely experiment without ruining the main project.
**Time needed:** 10 minutes.
**Wet-lab analogy:** Making a safe experimental copy of your main protocol to try a new reagent.

**Step 1: Create the Branch**
*   **If using Terminal:**
    ```bash
    git switch -c experiment
    ```
*   **If using GitHub Desktop App:**
    Click the **Current Branch: main** tab at the top. Click **New Branch**, name it "experiment", and click Create.

**Step 2: Make a change and save it**
Make a small change to your `first-note.md` file and save it.
*   **If using Terminal:** Run `git add first-note.md` then `git commit -m "Try an experiment"`.
*   **If using GitHub Desktop App:** Check the box, type a summary, and click **Commit to experiment**.

**Step 3: Return to the main branch**
*   **If using Terminal:**
    ```bash
    git switch main
    ```
*   **If using GitHub Desktop App:**
    Click the **Current Branch** tab at the top and select **main**.

*Magic moment:* Look at `first-note.md` on your computer. The experimental sentence is gone! Because you switched back to `main`, Git changed the physical file back to how it was. You can bring it back by merging later.

**Success:** I understand that a branch lets me experiment safely.

---

## DAY 6 — Explore a Real Scientific Repository

**Goal:** See how professional scientists use this system.
**Where:** **Strictly GitHub Online**
**Time needed:** 15 minutes.

**Steps:**
1. Choose one repository from the Free University list (`04-free-university-7-repos.md`).
2. Open the repository in your web browser.
3. Read the README and documentation.
4. Look at the **Issues** tab to see how they discuss bugs and problems.
5. Find one issue and identify the problem it describes.

**Wet-lab analogy:** An issue is similar to recording a problem with an experiment instead of silently forgetting it.

---

## DAY 7 — Build Your Own Digital Lab Notebook

**Goal:** Start a real project using your new skills.
**Time needed:** 15 minutes.

**Step 1: Prepare the file (On your computer)**
Copy `template/README_template.md` and move it into your `my-first-lab-book` folder. Rename it to `README.md` and fill in the sections for a real mini-project.

**Step 2: Record and Upload**
*   **If using Terminal:**
    ```bash
    git status
    git add README.md
    git commit -m "Add my first project notes"
    git push
    ```
*   **If using GitHub Desktop App:**
    Write "Add my first project notes" in the summary box. Click **Commit to main**, then click **Push origin** at the top.

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
