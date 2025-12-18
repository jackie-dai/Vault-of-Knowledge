
### Scrums
Frequent short meetings at the same time everyday (standups), everybody takes turns answering a few questions:
- What have you done since yesterday?
- What are you planning to do today?
- Are there any impediments or stumbling blocks?

## Git and Branches

![[Pasted image 20251217180920.png]]
*Example of using branches to implement features*

![[Pasted image 20251217180939.png]]*Example release branches*

### Git Rebasing
Scenario: you want to ensure your PR does not encounter any merge conflicts

Rebasing is a git operation that makes your world look as if you had branched from a later commit. Git will first apply all commits during the original commit you branched off to the current commit.  Then, git will attempt to apply commits from your feature branch. You may have to manually resolve merge conflicts if there are any.

*Be careful: rebasing rewrites the git repositories history*

## Git Merge
An alternative to git rebasing. It will merge new changes from the main branch into your feature branch. *It is nondestructive because it doesn't rewrite history* but it does add additional merge commits to your branch.