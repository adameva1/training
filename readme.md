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

... put commands and explanation here

## Managing branches

    $ git checkout master       # Switch to the master branch
    $ git branch feature1       # Creates a new branch feature1
    $ git checkout -b work      # Creates a new branch called work and switch to it 
    $ git checkout work         # Switch to branch work
    $ git branch                # List all local branches
    $ git branch -v             # List branches with the last commit
    $ git branch -a             # List all local and remote branches
    $ git branch --merged       # Show all branches merged to the current one
    $ git branch --no-merged    # Show all branches not merged to the current one
    $ git branch -d work        # Delete branch work
    $ git branch -D work        # Force deletion of unmerged branch work

## Merging


    $ git checkout work       # Switch to branch work
    $ git checkout master     # Switch to the master branch
    $ git merge work          # Merge branch work with the current branch
    $ git merge --abort       # Abort merge process and reconstruct pre-merge state
    $ git cat-file -p a3798b  # Shows a formated output of the git objects


Example 1:

    A - B (master)
         \
          C (work)
    
    $ git checkout master
    $ git merge work

Result and explanation here:



 A - B (master)     - D (master)    
          \         /
	    C (work)

Fast forward merge

Example 2:

    A - B - C - D (master)
         \
          X - Y (work)
    
    $ git checkout master
    $ git merge work

Result and explanation here:


    A - B - C - D (master) -  E (master)
             \              /
	      X - Y (work)

Merge-Commit



Example 3:

    A - B - C - D (master)
         \
          X - Y (work)
    
    $ git checkout work
    $ git merge master
    $ git checkout master
    $ git merge work

Result and explanation here:

    A - B - C - D (master)           - E (master)
             \             \         /
	      X - Y (work) - Z (work)

Merge conflict



Add you answers to the file readme.md!
