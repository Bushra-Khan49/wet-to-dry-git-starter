# Data Storage Rules

This folder is intentionally kept small. 

* Git repositories are not the right place for huge sequencing datasets.
* Keep tiny sample/test data only when appropriate.
* Follow institutional data-storage rules.
* Store real datasets in approved local, institutional or cloud storage.

⚠️ **IMPORTANT**: The right approach depends on size, project requirements and storage policy, but beginners should not upload large raw sequencing datasets (like FASTQ files) into ordinary Git history.

## What is `.gitkeep`?

Git does not normally track empty folders. `.gitkeep` is simply a placeholder file so this folder exists in the repository.
