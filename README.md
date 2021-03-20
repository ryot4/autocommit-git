# autocommit-git

autocommit-git is a simple shell script to commit changes in Git repositories noninteractively.

It checks changes in the specified working directory, and commit changes if exist.
Optionally, it can push changes to the remote repository.

## Prerequisites

 * `git` command must be available
   * `user.name` and `user.email` must be configured
 * The repository must be already initialized
   * When you use `-p` (push) option, the target remote repository must be already configured

## Usage

The following example commits changes in `directory` with the specified commit message.

    $ autocommit-git -m 'Automatic daily commit' /path/to/directory

If you omit `-m` option, the predefined message is used.

You can push changes to the remote repository with `-p` option.

    $ autocommit-git -p origin /path/to/directory

If you want to override the commit author, use `-a` option.

    $ autocommit-git -a 'author <author@example.com>' /path/to/directory
