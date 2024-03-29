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

or

`git checkout -u origin aBranch`

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

## push all tags to remote
`git push --tags`

### Create a branch from origin, track it, and checkout branch
`git checkout --track origin/aBranch`
This will create a local branch of "aBranch", track it, and then it will
checkout the branch

### Show logs with only the abbreviated commit hash and commit subject
`git log --format="%h: %s"`

### Show logs with only the abbreviated commit hash, commit subject, and branch location
`git log --format="%h%d: %s"`

### Show logs on a graph only the abbreviated commit hash, commit subject, and branch location
`git log --graph --format="%h%d: %s"`

### Check differences between the local branch and the remote (when you are in the local branch)
`git diff origin/<branch_name>`

## Delete a local tag
`git tag -d <tag>`

## Delete a remote tag
`git push origin :refs/tags/<tag>`

## Change the message of the last commit (before pushing)
`git --ammend -m "<message>"`

## Show all branches from remote
`git branch -r`

## Show branches that have been merged into the current branch
`git branch --merged`

## Update branch without checking out the branch
`git fetch <remote> <sourceBranch>:<destinationBranch>`

## Pick through the commits that you want to stage
`git add -p .` or `git add -p <path/to/file>`

## Rename a file in git
`git mv <original name> <new name>`

## Show log and files changed per commit
`git log --stat`