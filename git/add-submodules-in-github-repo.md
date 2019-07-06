# Add Submodules in GitHub Repo

## What are submodules

Submodules are basically remote git initialised repositories copied/cloned as a reference in your codebase.

Step 1: Get the remote repo url of the repo you want as a submodule in your repo. Let's call that *remote-repo-url* from now.

Step 2: change directory and go inside the repo in which you want to add the submodule.

Step 3: Add the remote-repo as submodule using the command:

```closure
git submodule add <remote-repo-url> <path-name>
```

### Reading Reference

* <https://gist.github.com/gitaarik/8735255>
