# Git Cheat Sheet
A basic cheatsheet that consists of the most commonly used and basic commands for Git version control!

## Version Control Systems:
VC Systems help us with:
* maintaining a healthy codebase
* helps avoid **quick fixes**
* keeps historical copies
* keeps track of changes

## Diffing files
``` 
diff file1 file2 
diff -u file1 file2
```

* The output of this on the command line shows the differences in the two files.
* The `-u` flag shows the additions and removals made in the second file, in a more organized way.

### Applying Changes

```
diff -u old_file new_file > change.diff
patch old_file < change.diff
```
* The first line of code here generates a file that contains all the changes made, and only the changes.
* The second command applies the changes generated in the `changes.diff` file to the `old_file`.

## Git!

Common first commands in Git are:

* `git init` : Initializes an empty Git repository in the current working directory
* `git add filename` : Lets the specified file be tracked by Git
* `git add .` : Adds all the files in the current working directory and subdirectories in the tracking radar for Git
* `git commit` : Commits our changes to the **local repository**
* `git status` : Tells us which category our file is in
    - Files used by Git can be in one of the following three categories:
    ``` Modified -> Staged -> Committed ```
    1. Modified files : Files that have been **locally changed and saved** in the computer.
    2. Staged files: Files that have been set for tracking by Git. (using the `git add` command)
    3. Committed files: Files that have had their changes saved in the **local repository**.


Other basic commands are:

* `git commit -a` : Shortcut to stage and commit changes to tracked files in one command and step.
* **HEAD alias** : Represents curently checked out snapshot of project
* `git log -p` : Gives information about patch.
* `git log --stat` : Shows stats about changes in commit.
* `git diff` : Similar to `diff -u` command, shows unstaged changes
* `git add -p` Shows unstaged changes and asks if you want to stage it
* `git diff --staged` : Shows staged changes

    
    


