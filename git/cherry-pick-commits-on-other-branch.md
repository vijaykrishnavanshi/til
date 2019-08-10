# Cherry Pick commits on other branch

## What is cherry-pick

If you go by the name its basically copying commits from one branch to the top of other branch (Technically HEAD). 

Step 1: List the commit hash which you wnat to copy on your branch. 
`closure
say 
8d1c0a5d1f85f189cea6501c1c56fefbdedfd5ea
cb1aeb19b3e3117028fd98b9b8334f21a893a686
`
You can get these by running git log after checking out to the branch on which these commits are located.

Step 2: Check out to the branch you want to copy it on.

Step 3: Run the following command:

```closure
git cherry-pick <commit-hash>
```

Step 4: Run git log to confirm that commit is actually present on your current branch now. All the commit meta like author and code diff should be same. And congrats you did it.

### Reading Reference

* <https://git-scm.com/docs/git-cherry-pick>
