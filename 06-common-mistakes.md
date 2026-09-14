# Mistakes Everyone Makes

You will make mistakes. That is normal. Every single programmer and scientist has made these same errors.

The golden rule: **Read the error first, and do not panic.**

---

## What CAN and CANNOT go on GitHub? (Size & Security Limits)

A huge source of beginner mistakes is misunderstanding what GitHub is meant to hold. Git is designed for tracking *text*, not massive databases or secrets.

**✅ YES (Good to upload):**
*   Text notes (`.txt`, `.md`)
*   Code scripts (`.py`, `.R`, `.sh`)
*   Small data tables (e.g., a `.csv` file that is a few Megabytes)
*   Lab protocols and standard operating procedures

**❌ NO (Do NOT upload):**
*   **Massive Files:** GitHub has a hard limit. **It will block any single file larger than 100 Megabytes (100 MB)**. Do not upload raw sequencing data (FASTQ, BAM), uncompressed microscopy images, or giant Excel spreadsheets.
*   **Secrets:** Never upload passwords, API keys, or access tokens. Hackers scan GitHub 24/7 looking for accidentally uploaded passwords.
*   **Sensitive Data:** Never upload Patient Identifiable Information (PII), confidential clinical data, or unpublished data that your institution prohibits sharing.

---

## Mistake 1: "I accidentally added a massive FASTQ file (or it says my file is over 100MB)."

*   **Why it happened:** You probably told Git to save a folder without realizing a massive file was hiding inside it. Git tried to upload it, and GitHub threw a wall of red error text because it exceeds the 100MB limit. 
*   **How to fix it:** 
    *   If you just see it sitting in your `git status` as green, you can tell Git to unstage it.
    *   If you already ran `git commit`, Git is now "stuck" trying to push a file that is too big. 
    *   **Beginner Guidance:** Do not copy-paste dangerous commands from the internet to fix this. If this is a brand-new repository, it is sometimes easiest to delete the folder on your computer, clone it again, and start over. Otherwise, ask an experienced colleague or IT support to help you "remove a large file from Git history."
*   **Prevention:** Always run `git status` to look at the list of files *before* you run `git add`. Use a `.gitignore` file to make Git permanently blind to `.fastq` files.
*   **Wet-lab analogy:** Accidentally gluing a 10-pound gel directly into the pages of your paper notebook.

## Mistake 2: "I accidentally uploaded a password or API key."

*   **Why it happened:** You wrote a script that logs into a database, typed your password directly into the code, and pushed it to GitHub.
*   **How to fix it:** 
    1. **Deactivate the password immediately.** Go to the website where the password belongs and change it, or revoke the API key. Do this *before* you try to fix Git.
    2. Once the password is dead and can't be used by hackers, you can safely remove the password from your code file, commit the fix, and push. 
*   **Prevention:** Never type passwords into code. Store them in special files on your computer that are listed in your `.gitignore` file.
*   **Wet-lab analogy:** Taping the key to the hazardous chemicals cabinet on the front door of the lab.

## Mistake 3: "I made my repository public by accident."

*   **Why it happened:** You clicked the wrong button when creating the repository online. Now anyone on the internet can read your notes.
*   **How to fix it:** Go to your repository on the GitHub website. Click the **Settings** tab at the top → Scroll all the way down to the "Danger Zone" → Click **Change repository visibility** → Select **Make private**.
*   **Prevention:** Always double-check visibility settings every time you create a new repository.
*   **Wet-lab analogy:** Leaving your private lab notebook on a park bench.

## Mistake 4: "I have files named final_v1, final_v2, final_v3."

*   **Why it happened:** You are treating files the old-fashioned way by renaming them every time you make a change.
*   **How to fix it:** Stop renaming the file! Keep the name simple (e.g., `analysis.py`). Let Git handle the versions. You can view your past versions anytime by typing:
    ```bash
    git log --oneline
    ```
*   **Prevention:** Commit regularly. If you make a mistake, Git can always time-travel back to a previous commit. 
*   **Wet-lab analogy:** Writing "Final" on a protocol, then crossing it out and writing "Really Final", then crossing that out and writing "Actually Final".

## Mistake 5: "I know I changed something, but I can't remember what."

*   **How to fix it:** 
    ```bash
    git diff
    ```
    This command prints out exactly what text you deleted (in red) and what text you added (in green) since your last save.
*   **Wet-lab analogy:** Holding yesterday's protocol notes and today's protocol notes side-by-side to spot the difference.

## Mistake 6: "I am totally lost. I don't know what Git thinks is happening."

*   **How to fix it:** 
    ```bash
    git status
    ```
    This is your compass. It tells you if you have unsaved changes, if you are on a branch, or if you are ready to push. Run this constantly.
*   **Wet-lab analogy:** Checking your tray to see what samples you are about to record in the log.

## Mistake 7: "Git says 'Merge Conflict' and won't let me pull or push."

*   **Why it happened:** You changed a line of text on your laptop, but someone else (or you, on a different computer) changed *the exact same line* online. Git doesn't know whose change is correct.
*   **How to fix it:** Git will open the file and put *both* versions of the text inside it, separated by weird symbols like `<<<<<<<`. Just open the file in a text editor, read both versions, delete the one you don't want (and delete the weird symbols), save the file, and run `git add` and `git commit`. 
*   **Prevention:** Always run `git pull` *before* you start working for the day to make sure your computer has the newest online changes.
*   **Wet-lab analogy:** Two scientists trying to write in the exact same box of the lab notebook at the exact same time.

## Mistake 8: "My laptop died or was stolen."

*   **Why it happened:** Computers break. Coffee spills happen.
*   **How to fix it:** As long as you ran `git push`, your work exists safely on GitHub. You can buy a new computer, install Git, run `git clone`, and pick up exactly where you left off.
*   **Prevention:** Run `git push` at the end of every work day. (But remember: GitHub is not a complete backup system for your massive datasets, just your text and code).
*   **Wet-lab analogy:** Losing your notebook in a fire, but remembering you made photocopies and put them in a safe at the library.
