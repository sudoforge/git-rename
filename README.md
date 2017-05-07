# git-rename

`git-rename`provides a nice interface to `git branch -m` and the workflow
related to renaming a branch - including on the remote.

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
