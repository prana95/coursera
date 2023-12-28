Study guide: diff and patch
The diff command
You use the diff command to find the differences between two files. On its own, it’s a bit hard to use; instead, use diff -u to find lines that differ in two files:

Using diff -u
You use the diff -u command to compare two files, line by line, and have the differing lines compared side-by-side in the same output. For an example of what this looks like, see below:

30
~$ cat menu1.txt 
Menu1:

Apples
Bananas
Oranges
Pears

~$ cat menu2.txt 
Menu:
…-Menu1:
+Menu:
 
 Apples
 Bananas
-Oranges
-Pears
+Grapes
+Strawberries

The patch command
The patch command is useful for applying file differences. See the example below, which compares two files. The comparison is saved as a .diff file, which is then patched to the original file!

123456789101112131415161718192021
 Hello World
+
+It's a wonderful day!
~$ diff -u hello_world.txt hello_world_long.txt > hello_world.diff
~$ patch hello_world.txt < hello_world.diff 
patching file hello_world.txt
~$ cat hello_world.txt 
Hello World

It's a wonderful day!

Resources for more information
There are other interesting patch and diff commands such as patch -p1 and diff -r . For more information on these commands, check out the following resources:

http://man7.org/linux/man-pages/man1/diff.1.html

http://man7.org/linux/man-pages/man1/patch.1.html
test git_github_google branch
