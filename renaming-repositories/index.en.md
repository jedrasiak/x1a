---
id: 019bf231-775c-717c-8f0e-84382cb45be1
title: Renaming Repositories
slug: renaming-repositories
draft: false
links:
- "[Git & GitHub](/git-github/index.en.md?label=parent)"
---

# Renaming Repositories

## Overview

Renaming a repository involves changing both the local Git repository name and, if applicable, the remote repository name on platforms like GitHub. This process requires careful coordination to avoid breaking existing references and clone URLs.

## Renaming a Local Git Repository

To rename a local Git repository, simply rename the directory that contains the `.git` folder:

```bash
mv old-repo-name new-repo-name
```

This operation is safe and does not affect the Git history or configuration. However, you will need to update any scripts or configurations that reference the old path.

## Renaming a GitHub Repository

### Steps

1. **Navigate to Repository Settings**
   - Go to your repository on GitHub
   - Click on "Settings" tab
   - Find the "Repository name" field in the General section

2. **Enter New Name**
   - Type the new repository name
   - Click "Rename" button

3. **Important Considerations**
   - GitHub automatically redirects requests from the old name to the new name
   - However, this redirect may not work indefinitely
   - All existing clones, forks, and pull requests will continue to work
   - Issue links and references are automatically updated

### Updating Local Clones

After renaming a repository on GitHub, update your local repository's remote URL:

```bash
# Check current remote URL
git remote -v

# Update remote URL
git remote set-url origin https://github.com/username/new-repo-name.git

# Or for SSH
git remote set-url origin git@github.com:username/new-repo-name.git

# Verify the change
git remote -v
```

### Updating from Old Repository Name

If you cloned the repository before renaming, you can also update the local directory name:

```bash
# Rename the local directory
cd ..
mv old-repo-name new-repo-name
cd new-repo-name

# Update remote URL (as shown above)
git remote set-url origin https://github.com/username/new-repo-name.git
```

## Best Practices

1. **Communication**: Inform team members and collaborators before renaming
2. **Documentation**: Update all documentation that references the old name
3. **CI/CD Pipelines**: Update continuous integration and deployment configurations
4. **Dependencies**: Check if other projects reference this repository and update them
5. **Local Clones**: Ensure all team members update their local clones
6. **Bookmarks**: Update browser bookmarks and IDE project configurations

## Common Issues

### Broken Links
- Links to specific files or commits using the old repository name may break
- Update documentation and wiki links accordingly

### Submodules
If the renamed repository is used as a submodule in other projects:
```bash
# Update .gitmodules file
vim .gitmodules  # Change URL to new repository name

# Sync and update
git submodule sync
git submodule update --init --recursive
```

### Protected Branches
Protected branch rules are preserved during renaming, but any external systems referencing branch names by the full repository path will need updates.

## References

- Git official documentation: https://git-scm.com/docs
- GitHub documentation on renaming repositories: https://docs.github.com/en/repositories/creating-and-managing-repositories/renaming-a-repository