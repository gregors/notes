# See files in stash without popping

## latest
 ```
 git stash show
 ```

## 1, 2, 3 etc
 ```
 git stash show stash@{1}
 ```

# Difference of files between 2 branches
 ```
   git diff --name-only
 ```

## Diff between 2 branches with filter
 remove migrations from diff
 ```
 git diff --name-only develop | grep -v migrate |  xargs git diff develop..
 ```

## See first commit
 ```bash
 git log --reverse
 ```

## Ignore whitespace in diff
 ```bash
 git diff -w
 git diff --ignore-all-space
 git diff --ignore-blank-lines
 ```

## Pruning
```bash
git branch --merged | egrep -v "(^\*|master|main|dev)" | xargs git branch -d
git branch -vv | grep ': gone]' | grep -v '\*' | awk '{ print $1; }' | xargs -r git branch -d
git remote prune origin
git prune
```

### Show users & emails
#### Current branch
```bash
git shortlog --summary --numbered --email
git shortlog -sne
```

#### All branches
```bash
git shortlog -sne --all
```
