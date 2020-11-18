# Shell Snippets

## Shell

```bash
# Cut output text
cut -f 1 #First Column, tab delimiter
cut -d' ' -f 1  # Space delimiter
cut -f 5- # Columns after 5
cut -f -4,7- # Columns before 4 and after 7
cut -f 1,4,5 # Columns 1,4,5


# Remove First line
sed 1d

# Helm2 delete all deployments
helm2 list | sed 1d | cut -f 1 | xargs | xargs helm2 delete --purge

# Diff between two folders
diff -rub ~ ./dotfiles

# Keep doing something
while true; do; k get deployments >> d.log; sleep 5 ; done
```

## Git

```bash
# No pager
git --no-pager diff

# Files changed between branches
git diff --name-only master #With Master
git diff --name-only HEAD~1 #Last commit
git diff --name-only HEAD~5 HEAD~10 #Last 5-10 commits
```

## Docker

```bash
#Override entrypoint
docker run -it --entrypoint /bin/bash [docker_image]

```

