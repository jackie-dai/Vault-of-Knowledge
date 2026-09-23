
There are two kinds of merges
### Fast-forward Merge
![[Pasted image 20260914105103.png]]

### Three-way Merge
![[Pasted image 20260914105132.png]]It is called a three way merge because it looks at 3 commits to generate the new merge commit f4
- The splitting point b/w main and feature: 95
- The target branch (currently on and merging into) latest commit in main: 17
- The source branch (branch you're trying to merge) latest commit in feature: d2

```
git rm "filename.txt"
```
Opposite functionality from git add. Untracks file and removes from local repository

```
git tag
```
In order to push tags to remote, you need to use *git push origin --tags*


```
git switch -c branchname
```
similar to git checkout (TODO research: checkout overwrites files to new versions and discards untracked changes. but what does switch do with the untracked files?)

```
git commit --amend
```
For undoing commit messages


```
git log --oneline --graph
```
shows graph view of branches


## Undoing Changes

If haven't added yet
```
git restore
```
Good for discarding files from working directory

if added and staged
```
git restore --staged
```

if already committed and before push

```
git commit --amend
```

If you've already pushed your changes to the remote repository
```
git revert *commit id*
```
*This creates a new commit, so not modifying commit history* 

git revert HEAD  revert most recent comit
git revert HEAD~i - revert a **single** commit i commits back (can also use git revert HASHID)
git revert HEAD~i..head - reverts multiple commits in range (i, head)

*Rewrites history* Only use for local-use, don't use if it has already been pushed to remote.
```
git reset
```

git reset --soft
git reset --mixed
git reset --hard
