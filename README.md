# git-rename

`git-rename`provides a nice interface to `git branch -m` and the workflow
related to renaming a branch - including on the remote.

## Installation

Obtain the source by cloning [this repository][repo-uri] or by downloading a
tarball of a [release][repo-releases]. Then run `make install` from the source
root.

```
$ git clone https://github.com/sudoforge/git-rename.git
$ cd git-rename
$ git checkout $(git describe --tags $(git rev-list --tags --max-count=1))
$ [sudo] make install
```

[repo-uri]: https://github.com/sudoforge/git-rename.git
[repo-releases]: https://github.com/sudoforge/git-rename/releases

## Usage

```text
git rename [options] <name>

OPTIONS
        -d, --dry-run
            Print debugging information and show what commands will be
            executed, without actually taking any actions.

        -u <remote>, --update-remote <remote>
            In addition to renaming the branch locally, using this option
            will perform the following actions to synchronize the specified
            remote:

            1. Push the newly renamed local branch to the remote
            2. If pushing was successful, delete the old branch from the remote

ARGUMENTS
        name
            The new name to change your current branch to.

```
