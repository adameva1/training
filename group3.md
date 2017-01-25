Exercise:
Explain the following commands with one sentence:

    $ git diff : show all differences since the last commit
    $ git diff --staged : all changes that are staged but not commited
    $ git diff test.txt : difference between the current version of test.txt and the last commit before stage
    $ git diff --theirs : show difference in a file from other user in case of a conflict
    $ git diff --ours : show my difference in a file compared to other user highlighted in green in case of a conflict
    $ git log : get log of the git repository
    $ git log --oneline : get all changes, every change in one line
    $ git log --oneline --all : get all details in one line
    $ git log --oneline --all --graph : get the log in a graph
    $ git log --oneline --all --graph --decorate : more beautiful
    $ git log --follow -p -- filename : show history of changes for one file
    $ git log -S'static void Main' : initial status of the file
    $ git log --pretty=format:"%h - %an, %ar : %s" : show the changes with hash and user name and time

Example:

    $ git status         Shows the current state of the repository

Add you answers to the file readme.md!
