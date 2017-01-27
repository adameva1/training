Exercise:

Explain the following commands with one sentence:

    $ git diff										Show changes between commits, commit and working tree
    $ git diff --staged								Shows all staged changes
    $ git diff test.txt								Shows the changes on the given file between the local version and the commited version
    $ git diff --theirs								In case of conflict shows the other people changes
    $ git diff --ours								In case of conflict shows our changes
    $ git log										Shows the history of all commits of this branch
    $ git log --oneline								Shows the history of all commits of this branch using one line for each commit
    $ git log --oneline --all						Shows the history of all commits of all branches using one line for each commit
    $ git log --oneline --all --graph				Shows the history of all commits of all branches using one line for each commit with additional visual info (graph)
    $ git log --oneline --all --graph --decorate    Shows the history of all commits of all branches using one line for each commit with additional visual info (graph) and with branch name
    $ git log --follow -p -- filename				Shows the complete history of a file including if filename changed	
    $ git log -S'static void Main'					Search the full contents of the files for all history 
    $ git log --pretty=format:"%h - %an, %ar : %s"  Shows the history showing the short hash, the author, the author date (relative to current date) and the commit comment

Example:

    $ git status         Shows the current state of the repository

Add you answers to the file readme.md!