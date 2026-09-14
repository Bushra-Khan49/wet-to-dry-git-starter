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

### Command Breakdown:
*   `git --version`
    *   **What it is:** A basic check to see if Git is installed.
    *   **How to read it:** "Hey Git, what version of yourself is installed?"
    *   **What it does / Why we use it:** It asks your computer to print the version number of Git. We use it to verify the installation worked.
    *   **Result:** Prints something like `git version 2.39.2`.
*   `git config --global user.name "Your Name"`
    *   **What it is:** A configuration setting.
    *   **How to read it:** "Hey Git, configure my global settings so my username is 'Your Name'."
    *   **What it does / Why we use it:** It tells Git what name to attach to your future saves (commits). It is like writing your name on the cover of the lab notebook.
    *   **Result:** Silent success (no output means it worked perfectly).

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

**Success:**
- [ ] I logged into GitHub online
- [ ] I clicked 'New Repository'
- [ ] I named my repository `my-first-lab-book`
- [ ] I set the visibility to 'Private'
- [ ] I successfully created the repository and can see its empty page online

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
    
    ### Command Breakdown:
    *   `git clone YOUR_REPOSITORY_URL`
        *   **What it is:** The download command.
        *   **How to read it:** "Hey Git, clone (copy) the repository found at this web address."
        *   **What it does / Why we use it:** It downloads the empty folder from GitHub and connects your local folder to the online locker.
        *   **Result:** A new folder appears on your computer containing the repository.
    *   `cd my-first-lab-book`
        *   **What it is:** A Terminal navigation command (stands for "change directory").
        *   **How to read it:** "Change directory into the folder named my-first-lab-book."
        *   **What it does / Why we use it:** It moves your Terminal's active view into the folder, so your future Git commands apply to this specific project.
        *   **Result:** Your Terminal prompt path updates to show you are inside the folder.

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
    ### Command Breakdown:
    *   `git status`
        *   **What it is:** The most important checking tool in Git.
        *   **How to read it:** "Hey Git, what is the current status of my files?"
        *   **What it does / Why we use it:** It tells you what files are new, changed, or ready to be saved. Always run this if you are confused!
        *   **Result:** Prints a list of changed/new files (often in red if unrecorded).
*   **If using GitHub Desktop App:** Look at the left sidebar. You will see `first-note.md` appear there with a green `+`. The App runs `git status` for you visually!

**Success:**
- [ ] I copied the GitHub URL
- [ ] I cloned the repository to my computer
- [ ] I navigated into the folder
- [ ] I created `first-note.md`
- [ ] I checked my status and saw Git recognized the new file

---

## DAY 4 — First Commit and Push

**Goal:** Tell Git to record the file you just made, and then upload that record to the internet.
**Time needed:** 10 minutes.

**Step 1: Stage and Commit (Recording locally)**
*   **If using Terminal:**
    ```bash
    git add first-note.md
    ```
    ```bash
    git commit -m "Add my first lab note"
    ```
    
    ### Command Breakdown:
    *   `git add first-note.md`
        *   **What it is:** The staging command.
        *   **How to read it:** "Hey Git, add `first-note.md` to the tray of things I want to save next."
        *   **What it does / Why we use it:** It tells Git specifically *which* file you are ready to record. (It does not save it permanently yet).
        *   **Result:** Silent success. If you run `git status` again, the file turns green.
    *   `git commit -m "Add my first lab note"`
        *   **What it is:** The saving command.
        *   **How to read it:** "Hey Git, commit (save) the files on the tray, and attach this message (-m): 'Add my first lab note'."
        *   **What it does / Why we use it:** It permanently writes the snapshot of your work into your local history book on your computer.
        *   **Result:** Prints a confirmation that 1 file was changed.

*   **If using GitHub Desktop App:**
    Make sure the box next to `first-note.md` is checked. At the bottom left in the "Summary" box, type *"Add my first lab note"*. Click the blue **Commit to main** button.

**Step 2: Push (Uploading to the cloud)**
*   **If using Terminal:**
    ```bash
    git push
    ```
    ### Command Breakdown:
    *   `git push`
        *   **What it is:** The upload command.
        *   **How to read it:** "Hey Git, push my local saved history up to the internet."
        *   **What it does / Why we use it:** It syncs your local computer's history with your GitHub online locker so it is backed up and shareable.
        *   **Result:** Prints progress text showing the upload to `https://github.com/...`.

*   **If using GitHub Desktop App:**
    Click the **Push origin** button at the very top of the window.

**Step 3: Verify (GitHub Online)**
Refresh your GitHub repository in your web browser. You will now see `first-note.md` sitting securely on the internet!
**Wet-lab analogy:** You recorded your results permanently in the notebook, and stored a copy in the secure online locker.

**Success:**
- [ ] I staged the file using `add` (or a checkbox)
- [ ] I committed the file with a message
- [ ] I pushed the file to the internet
- [ ] I refreshed my browser and saw the file on GitHub Online

---

## DAY 4 (Part 2) - Core Loop Summary
The core loop of using Git is:
Change something → `git status` → `git diff` → `git add` → `git commit` → `git push`

The scientific loop is:
Question → Experiment → Observation → Mistake → Fix → Record → Commit → Next experiment

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
    ### Command Breakdown:
    *   `git switch -c experiment`
        *   **What it is:** The branch creation command.
        *   **How to read it:** "Hey Git, switch to a new branch and create (-c) it with the name 'experiment'."
        *   **What it does / Why we use it:** It makes a safe, independent copy of your project where you can make changes without affecting the main version.
        *   **Result:** Prints "Switched to a new branch 'experiment'".

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
    ### Command Breakdown:
    *   `git switch main`
        *   **What it is:** The branch navigation command.
        *   **How to read it:** "Hey Git, switch my files back to how they look on the 'main' branch."
        *   **What it does / Why we use it:** It physically changes the files on your computer to reflect the main history. 
        *   **Result:** Prints "Switched to branch 'main'".

*   **If using GitHub Desktop App:**
    Click the **Current Branch** tab at the top and select **main**.

*Magic moment:* Look at `first-note.md` on your computer. The experimental sentence is gone! Because you switched back to `main`, Git changed the physical file back to how it was. You can bring it back by merging later.

**Success:**
- [ ] I created the 'experiment' branch
- [ ] I made a change to my file
- [ ] I committed the change to the new branch
- [ ] I switched back to the 'main' branch and saw my experimental change disappear

---

## DAY 6 — Explore a Real Scientific Repository

**Goal:** See how professional scientists use this system in the real world. You will learn to navigate the online interface of a major project to understand how collaboration works.
**Where:** **Strictly GitHub Online** (No terminal or app needed today!)
**Time needed:** 15 minutes.

**Detailed Exploration Steps:**
1. **Choose a repository:** Pick one repository from the Free University list (`04-free-university-7-repos.md`). For example, click on the Biopython link.
2. **Read the README:** When you open a repository on GitHub, the main page automatically displays the `README.md` file. This is the "front door" of the project. Read through it to understand the project's goal.
3. **Explore the Documentation:** Look for links in the README that point to "Docs" or "Wiki". Scientific projects put their methods and instructions here.
4. **Open the Issues Tab:** Click the **Issues** tab near the top of the GitHub page. Issues are basically a giant, public to-do list and troubleshooting log. 
    *   **What they are:** This is where scientists report bugs, ask for help, or suggest new features. 
    *   **Why they matter:** It prevents problems from being silently forgotten.
5. **Find one issue:** Click on an open issue and read the conversation. Notice how people describe the problem and propose fixes.
6. **Look at Pull Requests (Optional):** Click the **Pull Requests** tab. This is where someone has done an "experiment" on a branch and is asking to "merge" it into the main project.

**Wet-lab analogy:** Exploring a repository is like walking into another scientist's lab. The README is the introductory poster on the wall, the files are the organized benches, and the Issues tab is the whiteboard where the lab meets to discuss problems and protocols.

**Success:**
- [ ] I chose a scientific repository and opened it online
- [ ] I read through the README to understand the project's goal
- [ ] I located the 'Issues' tab and opened it
- [ ] I read at least one issue to see how scientists report problems
- [ ] I understand how issues act as a public troubleshooting log

---

## DAY 7 — Build Your Own Digital Lab Notebook

**Goal:** Put everything you have learned together to start a real, ongoing project. You will repeat the "core loop" of Git from scratch to solidify your skills.
**Time needed:** 15 minutes.

**Step 1: Prepare the file (On your computer)**
*   Open your computer's file explorer.
*   Navigate to your `my-first-lab-book` folder.
*   Find the `template/README_template.md` file that comes with this starter repository.
*   Copy it into the main directory of your `my-first-lab-book` folder.
*   Rename the copy to `README.md`.
*   Open it and fill in the sections (Goal, Date, What I tried, etc.) for a real mini-project or experiment you are currently working on.

**Step 2: Record and Upload**
Now, apply the commands you learned in Day 4 to save and upload your new file.

*   **If using Terminal:**
    1. Check what changed:
       ```bash
       git status
       ```
    2. Tell Git to prepare the new file:
       ```bash
       git add README.md
       ```
    3. Save it to your history:
       ```bash
       git commit -m "Add my first project notes"
       ```
    4. Upload it to GitHub:
       ```bash
       git push
       ```

*   **If using GitHub Desktop App:**
    1. Open the app and look at the left sidebar to see `README.md`.
    2. Write "Add my first project notes" in the summary box.
    3. Click **Commit to main**.
    4. Click **Push origin** at the top.

**Step 3: Celebrate (GitHub Online)**
Open your web browser and refresh your GitHub repository. Your new, organized digital lab notebook is live, backed up, and tracking your history.

**Success:**
- [ ] I copied the template file
- [ ] I filled out the template with my own project notes
- [ ] I ran `git status` (or checked the app) to see the new file
- [ ] I ran `git add` to stage the file
- [ ] I ran `git commit` to record the history
- [ ] I ran `git push` to upload it securely
- [ ] I viewed my finished, documented project on GitHub online

You finished. ✅

You now know:
* **status**
* **add**
* **commit**
* **push**
* **pull**
* **clone**
* **branch**
