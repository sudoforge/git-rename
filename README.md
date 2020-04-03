# git-rename

`git-rename`provides a nice interface to `git branch -m` and the workflow
related to renaming a branch - including on the remote.

## Installation

### Arch Linux

* [git-rename][aurpkg]

[aurpkg]: https://aur.archlinux.org/packages/git-rename

For other distributions, see below.

### Build from source

Obtain the source by cloning [this repository][gh/sudoforge/git-rename] or
by downloading the tarball of a [release][gh/sudoforge/git-rename/releases].
Then run `make install` from the source root.

```
$ git clone https://github.com/sudoforge/git-rename.git
$ cd git-rename
```

#### Linux

```
$ [sudo] make install
```


#### BSD (and derivatives like OSX)

```
$ PREFIX=/usr/local make install
```

#### Other

As you can see from above, the standard `PREFIX= make install` pattern is
supported. Plop it anywhere in your `PATH`!

[gh/sudoforge/git-rename]: https://github.com/sudoforge/git-rename.git
[gh/sudoforge/git-rename/releases]: https://github.com/sudoforge/git-rename/releases

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
