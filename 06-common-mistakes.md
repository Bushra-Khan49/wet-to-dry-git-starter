# Mistakes Everyone Makes

You will make mistakes. That is normal. Read the error first.

## Mistake: "I pushed a FASTQ file."

**Why it happened:** You added a huge file without realizing it. `.gitignore` helps prevent untracked files from being staged, but it does not undo history.
**Fix:** Use `git status` to see what is happening. If the file is already committed or pushed, stop and ask for help, especially if the file contains sensitive information or is very large. Do not run dangerous internet commands without understanding them.
**Prevention:** Always check `git status` before you `git add`.
**Wet-lab analogy:** Accidentally gluing a giant gel directly into your notebook.

## Mistake: "I made my repository public."

**Why it happened:** You clicked the wrong button when creating the repository.
**Fix:** On GitHub: **Settings** → **General** → **Change repository visibility** → **Make private**.
**Prevention:** Visibility changes should be checked carefully every time you make a repo.
**Wet-lab analogy:** Leaving your private lab notebook on a park bench.

## Mistake: "I have final_v1, final_v2, final_v3."

**Why it happened:** You are treating files the old way.
**Fix:** Teach yourself to use:
```bash
git log --oneline
```
Git history replaces many confusing filename versions.
**Prevention:** Commit regularly. Keep the filename the same, let Git track the versions.
**Wet-lab analogy:** Writing "Final" on a protocol, then crossing it out and writing "Really Final".

## Mistake: "I changed something and want to know what changed."

**Fix:** Use:
```bash
git diff
```
**Wet-lab analogy:** Comparing yesterday's protocol notes to today's side-by-side.

## Mistake: "I do not know what Git thinks changed."

**Fix:** Use:
```bash
git status
```
**Wet-lab analogy:** Checking your tray to see what samples you are about to record.

## Mistake: "I want the latest version from GitHub."

**Fix:** Use:
```bash
git pull
```
Pulling brings the online changes to your computer. Note that pulling can cause conflicts if you also made changes to the exact same lines.
**Wet-lab analogy:** Getting the newest protocol from the lab supervisor's desk.

## Mistake: "My laptop died."

**Why it happened:** Computers break.
**Fix:** If the committed and pushed work exists on GitHub, you can clone the repository onto another computer.
**Prevention:** Push often. But remember: GitHub is not a complete backup system.
**Wet-lab analogy:** Losing your notebook in a fire, but remembering you made photocopies in the library.
