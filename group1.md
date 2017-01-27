Exercise:

Explain the following commands with one sentence:

    $ git init
    $ git clone https://...
    $ git add test.txt
    $ git reset HEAD test.txt
    $ git add .
    $ git add -u
    $ git add -A
    $ git diff --staged
    $ git commit
    $ git commit -a 
    $ git commit -m "My message"

Example:

    $ git status         Shows the current state of the repository

Add you answers to the file readme.md!
    
    $ git init     	 Create an empty Git repository or reinitialize an existing one

    $ git clone   	 Clone a repository into a new directory

    $ git add test.txt	 Add file contents to the index

    $ git reset HEAD test.txt  Reset current HEAD to the specified state
    $ git add .		Adds content from all files under Documentation directory and its subdirectories
    $ git add -u	Update the index just where it already has an entry matching <pathspec>. This removes as well as mo			   difies index entries to match the working tree, but adds no new files
    $ git add -A	Update the index not only where the working tree has a file matching <pathspec> but also where the  			   		    index already has an entry. This adds, modifies, and removes index entries to match the working tree
    $ git diff --staged This form is to view the changes you staged for the next commit relative to the named <commit>.  

    $ git commit	Record changes to the repository
    $ git commit -a	Tell the command to automatically stage files that have been modified and deleted, but new files you have not told G			    it about are not affected.
    $ git commit -m "My message" Use the given <msg> as the commit message. If multiple -m options are given, their values are concatenated 				as separate paragraphs.


 $ git add
