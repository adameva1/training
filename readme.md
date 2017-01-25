# git cheat sheet

Read your group instruction in the text files 

[group1.md](group1.md)

[group2.md](group2.md)

[group3.md](group3.md)

[group4.md](group4.md)

and place your solution in a fitting category in this file. It's best to create a branch while working on the exercise!

## Creating repositories

    $ git init                       #create a new git repository (creates the .git folder)
    $ git clone https://...          #copies remote repo to your local repo (git init should not be used when using git clone)

## Staging and committing

    $ git add test.txt               #adds the test.txt file to the staging area for commit
    $ git reset HEAD test.txt        #resets the file test.txt back to the last commited version in the local repo
    $ git add .                      #adds new or modified files from local directory to staging area for commit
    $ git add -u                     #adds modified files from the entire working copy (includes subdirs) to the staging area for commit
    $ git add -A                     #adds new or modified files from the entire working copy (includes subdirs) to the staging area for commit
    $ git diff --staged              #diffs the contents of the local repo and the contents current staged for commit
    $ git commit                     #commits all the modifications from the staging area & prompts for a message to add to the log
    $ git commit -a                  #essentially a "git add -u" + "git commit"  NOTE: new files are not included!
    $ git commit -m "My message"     #commits all the modifications from the staging area & adds the message to the log instead of prompting


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
