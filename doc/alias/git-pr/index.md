+++
+++

# git pr

```gitconfig
# pull with rebase - to provide a cleaner, linear, bisectable history.
#
# To automatically do "pull --rebase" everywhere:
#
#     git config --global pull.rebase true
#
# To automatically do "pull --rebase" for any branch based on 
# the branch "main":
#
#    git config branch.main.rebase true
#
# To automatically do "pull --rebase" for any newly-created branches:
#
#     git config --global branch.autosetuprebase always
#
# To integrate changes between branches, you can merge or rebase.
#
# When we use "git pull", git does a fetch then a merge.
#
# If we've made changes locally and someone else has pushed changes
# to our git host then git will automatically merge these together
# and create a merge commit that looks like this in the history:
#
#    12345678 - Merge branch 'foo' of bar into main
#
# When we use "git pull --rebase", git does a fetch then a rebase.
#
# A rebase resets the HEAD of your local branch to be the same as
# the remote HEAD, then replays your local commits back into repo.
# This means you don't get any noisy merge messages in your history.
# This gives us a linear history, and also helps with git bisect.
#
pr = pull --rebase
```
