+++
+++

# git diff-*

```gitconfig
### git diff-* ###

diff-all = !"for name in $(git diff --name-only $1); do git difftool $1 $name & done"
diff-changes = diff --name-status -r
diff-stat = diff --stat --ignore-space-change -r
diff-staged = diff --cached

# Diff using our preferred options. A.k.a. `dd`.
diff-deep = diff --check --dirstat --find-copies --find-renames --histogram --color
```