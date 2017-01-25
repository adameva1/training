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

... put commands and explanation here

## Merging

.. put commands and examples here
