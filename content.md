## Content

### What is the difference between push, pull, and fetch?

- `git push` - sends changes from a local branch to a remote repository
- `git fetch` - adds changes from a remote repository into your tracking branch
- `git pull` - adds changes from a remote branch into your tracking branch and merges these changes into your local branch

`git push` first identifies if your tracking branch has a connection to a remote repository. If a connection exists, `git push` adds changes from your tracking branch to the remote branch, allowing you to share code with the remote repository and to make the remote branch remsemble your local branch. If the remote branch has diverged from your local branch, the push will fail. When this happens, synchronize your local branch to the remote branch by using `git pull` or `git fetch` followed by `git merge`. 

`git fetch` again takes our current branch, and checks to see if there is a tracking branch. If so, it looks for changes in the remote branch, and pulls them into the tracking branch. It does not change your local branch. To do that, you'll need to do `git merge origin/master` (for the "master" branch) to merge those changes into your branch - probably also called "master".`git pull` simply does a `git fetch` followed immediately by `git merge`. This is often what we desire to do, but some people prefer to use git fetch followed by git merge to make sure they understand the changes they are merging into their branch before the merge happens.