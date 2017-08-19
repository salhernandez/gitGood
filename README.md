# gitGood
A collection of git commands I find useful.

### Shows all of the commits for a file as well as the changes
`git log -p -M --follow --stat -- path/to/your/file`

### Lists all commits for a specific file
`git log --follow filename path/to/your/file`

### Shows all local branches, commit hash, and commit message on its HEAD
`git branch -v`

### Checks out a branch from remote, and sets tracking for it
schema:
`git checkout --track -b <local branch> <remote>/<tracked branch>`
example:
`git checkout --track -b aBranch origin/aBranch`
