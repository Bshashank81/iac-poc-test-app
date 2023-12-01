# Project Iac_Poc

## Shared Configuration Files

This project utilizes a shared configuration directory named `.git-shared` to manage certain files that are specific to the development environment but should not be committed to the repository. Developers are required to manually copy these files to their local `.git` directory.

### Shared Files in `.git-shared`

The `.git-shared` directory contains the following essential files:

- `config`: Append the file configuration in .git/config file. 
- `hooks/commit-msg`: Append the file if exist or copy it.
- `hooks/pre-commit`: Append the file if exist or copy it.
- `hooks/prepare-commit-msg`: Append the file if exist or copy it.

### Instructions for Developers

#### 1. Ignore the Shared Configuration Directory

Ensure that the `.git-shared/` directory is added to your `.gitignore` file to avoid accidentally committing its contents:

```plaintext
# .gitignore

.git-shared/
2. Manual Copying of Files
Certain files from the .git-shared directory are essential for the project. Follow these steps to manually copy these files to your local .git directory:

bash
Copy code
# If files do not exist in .git directory
cp -r .git-shared/* .git/

# If files exist in .git directory, append content
cp -r -n .git-shared/* .git/
Replace * with specific file names as needed.
