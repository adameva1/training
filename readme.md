# git cheat sheet

Read your group instruction in the text files 

[group1.md](group1.md)

[group2.md](group2.md)

[group3.md](group3.md)

[group4.md](group4.md)

and place your solution in a fitting category in this file. It's best to create a branch while working on the exercise!

## Creating repositories

... put commands and explanation here

## Staging and committing

... put commands and explanation here

## Inspecting the repository and history

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

## Managing branches

... put commands and explanation here

## Merging

    $ git checkout work		Switch to work branch
    $ git checkout master	Switch to master branch
    $ git merge work		Joins work directory with master
    $ git merge --abort		Aborts the merge during conflicts
    $ git cat-file -p a3798b    Provide content or type and size information for repository objects

Example:

    $ git status         Shows the current state of the repository

Here are some standard situations, and a git command. Draw the result, and add some explanation:

Example 1:

    A - B (master)
         \
          C (work) 
    
    $ git checkout master
    $ git merge work


Result and explanation here: Fast Forward

    A - B 
         \
          C (work) (master)



Example 2:

    A - B - C - D (master)
         \
          X - Y (work)
    
    $ git checkout master
    $ git merge work

Result and explanation here: Merge or Conflict


    A - B - C - D - E  (master)
         \         /
          X   -   Y (work)    


Example 3:

    A - B - C - D (master)
         \
          X - Y (work)
    
    $ git checkout work
    $ git merge master
    $ git checkout master
    $ git merge work

Result and explanation here:


    A - B - C -  D 
         \        \
          X - Y  - Z (work)(master)
    

