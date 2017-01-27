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
    

