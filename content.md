## Content

### What is the difference between push, pull, and fetch?

- `git push` - sends changes from a local branch to a remote repository
- `git fetch` - adds changes from a remote repository into your tracking branch
- `git pull` - adds changes from a remote branch into your tracking branch and merges these changes into your local branch

`git push` first identifies if your tracking branch has a connection to a remote repository. If a connection exists, `git push` adds changes from your tracking branch to the remote branch, allowing you to share code with the remote repository and to make the remote branch remsemble your local branch. If the remote branch has diverged from your local branch, the push will fail. When this occurs, synchronize your local branch to the remote branch by using `git pull` or by executing `git fetch` followed by `git merge`. 

`git fetch` first identifies if your tracking branch has a connection to your local branch. If a connection exists, `git fetch` adds changes from the remote branch to your tracking branch without altering data in your local branch. To merge changes from the remote branch into your local branch, execute `git merge origin/[branch name]`.

`git pull` executes `git fetch` immediately followed by `git merge`. While this is often the desired result, many developers prefer to use `git fetch` followed by `git merge` to understand all code changes prior to the merge.