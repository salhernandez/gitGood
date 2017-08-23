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

### Add a tag to HEAD
`git tag v1.0`
where the tag is "v1.0"

### Add an annotated tag to HEAD
`git tag v1.0 -m "This is the tag information"`
where the tag is "v1.0" and message is "This is the tag information"

### Add a tag to a specific commit
`git tag -a v1.1 12cd234`
where the tag is "v1.1" and the commit hash starts with 12cd234
you only need the first sever characters of the commit hash
