# If You Get Stuck, Do This

Stop. Do not randomly delete files or run commands from the internet.

Follow this sequence:

## Step 1
Read the error.

## Step 2
Run:
```bash
git status
```

## Step 3
Copy the complete error message.

## Step 4
Check whether you are inside the repository.
Mac/Linux/Git Bash:
```bash
pwd
```
Windows Command Prompt alternative:
```cmd
cd
```

## Step 5
If necessary, ask for help using:
* Operating system
* Command you ran
* Complete error message
* What you expected
* What actually happened

## Common beginner errors:
* `git is not recognized` / `command not found`: You haven't installed Git or your Terminal can't find it.
* `not a git repository`: You are in the wrong folder. Use `cd` to navigate to your repo.
* `nothing to commit`: You haven't changed any files, or you forgot to `git add` them.
* `rejected` / `failed to push`: Someone else pushed changes to GitHub. You need to `git pull` first.
* `merge conflict`: You and someone else changed the exact same line of a file.

**Wet-lab analogy:** If a machine beeps a red error code, you don't start hitting it with a wrench. You read the screen and check the manual. Do the same with Git!
