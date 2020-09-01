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


