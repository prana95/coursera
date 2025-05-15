# when to use git commit -am "some message"
if the file in question is already tracked by git we can use -a otherwise we cant use the -a for the new files. 
def: a shortcut to stage any changes to tracked files and commit them in one step.
if the new file is not staged we need to use git add new_file and then commit the file

# HEAD
def: git use the HEAD alias to represent the currently checked-out snapshot of your project.
HEAD is like a bookmark (for a book) that you can use to keep track of where you are. even if you have multile books to read, the 
