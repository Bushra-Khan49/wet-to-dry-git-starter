# Install Git

## Windows

1. Go to: https://git-scm.com
2. Download Git.
3. Install it using the normal recommended options.
4. Open Git Bash or Command Prompt.
5. Run:

```bash
git --version
```

If you see a version number, you were successful! ✅

## Mac

**Option 1:**
Open Terminal and run:

```bash
git --version
```

If macOS asks to install the required developer tools, click Install.

**Option 2:**
Install Git using the official Git installer/package manager if needed.

## Linux

For common distributions, open Terminal and run the commands for your system. Commands differ between Linux distributions.

**Example for Ubuntu/Debian:**
```bash
sudo apt update
sudo apt install git
```

## GitHub Desktop

For beginners who dislike commands, you can use GitHub Desktop.

1. Go to: https://desktop.github.com
2. Download
3. Install
4. Sign in
5. Use it to clone, commit and push

## Configure Git

Before you record history, Git needs to know who you are. Open Terminal or Git Bash and run:

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

This is the name and email Git records with your commits. Think of this as signing a lab notebook entry.

Then verify it worked:

```bash
git config --global user.name
git config --global user.email
```
