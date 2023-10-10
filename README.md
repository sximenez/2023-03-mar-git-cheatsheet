# Git cheatsheet

- [Git cheatsheet](#git-cheatsheet)
  - [Revert to specific commit](#revert-to-specific-commit)
  - [Pushing from repo A to repo B](#pushing-from-repo-a-to-repo-b)
  - [Replace main with different or unrelated branch](#replace-main-with-different-or-unrelated-branch)

## Revert to specific commit

```git
git log --oneline
git checkout <commit>

<!-- This reverts back to that commit but doesn't save it -->
<!-- To save it create a new branch -->
git checkout -b <new-branch-name>
```

## Pushing from repo A to repo B


```git
git remote add {{repoB}}
git checkout -b {{new-branch}}
git push {{repoB}} {{new-branch}}

<!-- Rename repoB to origin -->
git remote remove origin
git remote rename {{repoB}} origin
```

## Replace main with different or unrelated branch

```git
git checkout develop
git checkout -b {{new-main}}
git branch -d main
git branch -m main
git push origin main
```