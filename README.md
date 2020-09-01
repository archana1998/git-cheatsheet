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
* `git status` : Tells us which category our file is in. Files used by Git can be in one of the following three categories:

   ```Modified                ->             Staged         ->                    Committed                             ```


   1. Modified files : Files that have been **locally changed and saved** in the computer.
   2. Staged files: Files that have been set for tracking by Git. (using the `git add` command)
   3. Committed files: Files that have had their changes saved in the **local repository**.


Other basic commands and information are:

* `git commit -a` : Shortcut to stage and commit changes to tracked files in one command and step.
* **HEAD alias** : Represents curently checked out snapshot of project
* `git log -p` : Gives information about patch.
* `git log --stat` : Shows stats about changes in commit.
* `git diff` : Similar to `diff -u` command, shows unstaged changes
* `git add -p` Shows unstaged changes and asks if you want to stage it
* `git diff --staged` : Shows staged changes


### Deleting and Renaming Files
* `git rm file_name` : Deletes file specified.
* `git mv old_name new_name`: Renames the file

### Undoing changes

* `git checkout` : reverts changes to modified files before they are changed
* ` git reset` : reverts staged changes
* `git commit --amend` : edits previous commit and overwrites the previous commit with edited version

Note: Do not amend **public commits**!

### Rollbacks

* `git revert HEAD` : creates new commit with inverse changes
* `git revert commit_ID`: reverts the commit specified

### Branching and Merging

* `git branch new_branch_name` : creates new branch with name specified
* `git checkout branch_name` : switches to the branch specified (changes where HEAD points to)
* `git checkout -b new_branch_name`: one command to create a new branch and switch to it in one step
* `git branch -d branch_name`: deletes branch specified
* `git merge branch_to_be_merged`: merges branch specified to the branch HEAD is currently pointing to
* `git log --graph --oneline` : summarized view of commit history
* `git merge --abort`: prevents merge if conflicts arise

### Working with remote repositories

* `git clone link_to_repo.git` : gets copy of remote repository onto your local machine
* `git config --global credential.helper cache` : caches remote repo's credentials in local machine for 15 minutes
* `git remote` : lists remote repositories
* `git fetch` : downloads specific objects from remote and doesn't merge
* `git pull` : downloads updates from the remote branch and merges
* `git pull -a ` : downloads updates from all remote branches and merges
* `git rebase branch_name` : does fast-forward merge of current branch with the specified branch
* `git push -u origin` : pushes changes to the remote object origin, in accordance with current working branch.

## Squashing changes

* `git rebase -i` : Interactive rebasing, offers complete control over the branch's commit history. Helps clean up messy history
* `git push -f` : Forces a push to the remote repository


### Other Notes

* **Forking** : Creates a copy of the given repository so that it belongs to our user
* **Pull request** : Way to send and suggest changes to original owner of repository

Workflow of Pull Request:

- Fork project and clone the fork
- Make changes locally and commit
- Push change while making new branch
- Open pull request on Github/GitLab and check if the changes can be merged (this shows automatically)
    


