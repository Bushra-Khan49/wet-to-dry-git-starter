# If You Get Stuck, Do This

**Stop.** Take a deep breath. 
Do not randomly delete files. Do not copy and paste random commands from the internet hoping they will fix the problem. 

Follow this safe, 5-step emergency sequence:

---

## Step 1: Read the red text
When Git throws an error, it usually tells you exactly what went wrong in plain English at the very bottom of the text. Read it carefully.

## Step 2: Ask Git where you are
Type this and press Enter:
```bash
git status
```
This is your compass. It will tell you if you have unsaved changes, if you are in the middle of a mistake, or if you just need to commit.

## Step 3: Check your location
Many errors happen simply because you are typing commands in the wrong folder. 
Check what folder your Terminal is currently looking at:

*   **Mac / Linux / Git Bash:** Type `pwd` and press Enter.
*   **Windows Command Prompt:** Type `cd` and press Enter.

*If the folder path that prints out does not end in your project's name (like `my-first-lab-book`), you are in the wrong place! Use the `cd` command to navigate to the correct folder.*

## Step 4: Copy the complete error message
Use your mouse to highlight the *entire* error message you got and copy it. You can paste this directly into Google, or send it to a colleague.

## Step 5: Ask for help the right way
If you need to ask a colleague, a professor, or IT support for help, give them this exact information. It will save everyone hours of time:

*   **My Operating System:** (e.g., Mac, Windows 11)
*   **The command I typed:** (e.g., `git push`)
*   **The complete error message:** (Paste what you copied in Step 4)
*   **What I expected to happen:** (e.g., "I wanted to upload my new notes.")
*   **What actually happened:** (e.g., "It said 'rejected'.")

---

## The 5 Most Common Beginner Errors

Here is a cheat sheet of the most common errors and what they actually mean:

### 1. `git: command not found` or `git is not recognized`
*   **What it means:** Your computer doesn't know what Git is. 
*   **The fix:** You either haven't installed Git yet, or you need to close your Terminal window and open a brand new one so it can refresh.

### 2. `fatal: not a git repository`
*   **What it means:** You are standing in the wrong room. Git is looking for a project folder, but your Terminal is looking at your Desktop or Documents folder. 
*   **The fix:** Use the `cd` command to open the specific folder you cloned (e.g., `cd my-first-lab-book`).

### 3. `nothing to commit, working tree clean`
*   **What it means:** You are trying to save, but there is nothing new to save. 
*   **The fix:** You either haven't changed any files, or you forgot to run `git add` to stage them first.

### 4. `Updates were rejected...` (Failed to push)
*   **What it means:** Someone else (or you, on a different computer) uploaded changes to GitHub. Git won't let you overwrite them.
*   **The fix:** You must download their changes first by running `git pull`.

### 5. `Merge conflict`
*   **What it means:** You and someone else edited the exact same line of the same file. Git doesn't know which version to keep.
*   **The fix:** Open the file in a text editor. Git has pasted both versions inside. Delete the one you don't want, save the file, then run `git add` and `git commit`.

---

**Wet-lab analogy:** If a $50,000 sequencing machine beeps and flashes a red error code, you don't start hitting it with a wrench. You read the screen, check the manual, and call a technician if you are confused. Do the exact same thing with Git!
