# Security and Research Data

A private repository does not mean "anything is safe to upload."

⚠️ **IMPORTANT**: `.gitignore` is not a security guarantee. It just prevents you from accidentally adding files, but it does not protect data if you force it.

## Never commit:
* Passwords
* API keys
* Access tokens
* Private keys
* Login credentials
* Patient-identifying information
* Confidential clinical information
* Confidential institutional data
* Data that your institution does not allow you to upload
* Sensitive unpublished information when policy prohibits uploading it

Follow your institutional rules. A private GitHub repository is not permission to upload information that your institution, supervisor, ethics board, employer, or data provider says must not be uploaded.

Never put a password or API key directly into a code file.

If a secret is accidentally pushed:
1. Do not simply delete the line and assume the secret is gone. Deleting the file later does not automatically remove it from Git history.
2. Revoke/rotate the secret first (change the password, delete the API key on the provider's website).
3. Then follow proper secret-removal guidance.

## Before You Push

- [ ] No passwords
- [ ] No API keys
- [ ] No patient identifiers
- [ ] No prohibited data
- [ ] No huge raw datasets
- [ ] I checked `git status`
- [ ] I checked the files I am committing
