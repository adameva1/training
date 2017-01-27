# git cheat sheet

Read your group instruction in the text files 

[group1.md](group1.md)

[group2.md](group2.md)

[group3.md](group3.md)

[group4.md](group4.md)

and place your solution in a fitting category in this file. It is best to create a branch while working on the exercise!

## Creating repositories

    $ git init           Create an empty Git repository or reinitialize an existing one
    $ git clone          Clone a repository into a new directory


## Staging and committing

    $ git add test.txt   Add file contents to the index

    $ git add .         Adds content from all files under Documentation directory and its subdirectories
    $ git add -u        Update the index just where it already has an entry matching <pathspec>. This removes as well as modifies
                        index entries to match the working tree, but adds no new files

    $ git add -A        Update the index not only where the working tree has a file matching <pathspec> but also where the
                        index already has an entry. This adds, modifies, and removes index entries to match the working tree


    $ git commit        Record changes to the repository
    $ git commit -a     Tell the command to automatically stage files that have been modified and deleted, but new files you have not told
                        Git about are not affected.
    $ git commit -m "My message"
                        Use the given <msg> as the commit message. If multiple -m options are given, their values are concatenate as separate paragraphs.

    $ git reset HEAD test.txt  Reset current HEAD to the specified state
    $ git diff --staged This form is to view the changes you staged for the next commit relative to the named <commit>.

## Inspecting the repository and history

    $ git status         Shows the current state of the repository


## Managing branches


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
    

