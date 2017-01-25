Exercise:

Explain the following commands with one sentence:

    $ git checkout work       # Switch to branch work
    $ git checkout master     # Switch to the master branch
    $ git merge work          # Merge branch work with the current branch
    $ git merge --abort       # Abort merge process and reconstruct pre-merge state
    $ git cat-file -p a3798b  # Shows a formated output of the git objects

Example:

    $ git status         Shows the current state of the repository


Here are some standard situations, and a git command. Draw the result, and add some explanation:

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
