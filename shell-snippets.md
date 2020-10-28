# Shell Snippets

```bash
# Cut output text
cut -f 1
cut -d' ' -f 1

# Remove First line
sed 1d

# Helm2 delete all deployments
helm2 list | sed 1d | cut -f 1 | xargs | xargs helm2 delete --purge

# Diff between two folders
diff -rub ~ ./dotfiles
```

## Git

```bash
# No pager
git --no-pager diff

# Files changed between branches
git diff --name-only master #With Master
git diff --name-only HEAD~1 #Last commit
git diff --name-only HEAD~5 HEAD~10 #Last 5-10 commits

# 
```

