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

    $ git add test.txt   Add file contents to the stage

    $ git add .         Adds content from all files under Documentation directory and its subdirectories
    $ git add -u        Update the stage just where it already has an entry matching <pathspec>. This removes as well as modifies
                        stage entries to match the working tree, but adds no new files

    $ git add -A        Update the stage not only where the working tree has a file matching <pathspec> but also where the
                        stage already has an entry. This adds, modifies, and removes stage entries to match the working tree


    $ git commit        Record changes to the repository
    $ git commit -a     Tell the command to automatically stage files that have been modified and deleted, but new files you have not told
                        Git about are not affected.
    $ git commit -m "My message"
                        Use the given <msg> as the commit message. If multiple -m options are given, their values are concatenate as separate paragraphs.

    $ git reset HEAD test.txt  Reset current HEAD to the specified state
    $ git diff --staged This form is to view the changes you staged for the next commit relative to the named <commit>.


Add you answers to the file readme.md!
## Inspecting the repository and history

    $ git status         Shows the current state of the repository
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

    $ git checkout master          Switch to master branch
    $ git branch feature1          Create a new branch feature1
    $ git checkout -b work         Create a new branch and switch to it
    $ git checkout work            Switch to branch work
    $ git branch                   List branches
    $ git branch -v                List branches and commit messages with short checksum 
    $ git branch -a                List all branches including remotes
    $ git branch --merged          List branches already merged
    $ git branch --no-merged       List branches not yet merged
    $ git branch -d work           Delete only branches that are already merged
    $ git branch -D work           Delete branches and do not consider status 


## Merging

    $ git checkout work         Switch to work branch
    $ git checkout master       Switch to master branch
    $ git merge work            Joins work directory with master
    $ git merge --abort         Aborts the merge during conflicts
    $ git cat-file -p a3798b    Provide content or type and size information for repository objects


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
    

