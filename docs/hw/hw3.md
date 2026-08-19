# Homework assignment HW3

## Homework log

Remember to create a new post with a new topic "HW3" in your homework log channel on Microsoft Teams. Make a reply to that topic whenever do some work on this assignment. You can also post questions there. Your posts should provide evidence that you spent several hours doing meaningful work.

## Objectives

This assignment continues to build on the command line skills you have been developing in HW1 and HW2. That emphasizes redirection shell scripts and pipes which allow you to combine basic command line utilities. 

Minimal knowledge and experience to acquire include the following:
* redirection of standard input and output using `<` and `>`, e.g.
  - `head --lines=2 > begin.txt`
  - `sort < words.txt`
  - `head -n4 < lines.txt > top.txt`
* Running a shell script from the command line, e.g. `./myscript.sh`
* Understand Unix permissions.
  - Understand the meaning of _user/owner_, _group_, _other_, _read_, _write_, _execute_ for Unix permissions.
  - Interpret the output of `ls -l` to determine the permissions of a file or directory, e.g., `rwxrwxr--`
  `rwxr-xr-x`, `rw-r-xr--`, `r--r--r--`, `r---w---x`.
* use of `chmod` to change permissions on files and directories, e.g. `chmod u+x myscript.sh`
* use of pipes to combine command line utilities, e.g. `cat words.txt | sort | head -n5`
* use of `wc` to count lines, words, and characters in a file, e.g. `wc -l words.txt`
* use of `cut` to extract columns of data from a file, e.g. `cut -f1,3 data.txt`
* use of `uniq` to remove duplicate lines from a file, e.g. `sort words.txt | uniq`
* use of `ps` to view running processes, e.g. `ps -ef`
* use of `kill` to terminate a process, e.g. `kill -KILL 12345`


## PB version

The Professor Braught version is available as:
* [03-A-FiltersScriptsPipes.docx](../materials/03-A-FiltersScriptsPipes.docx)

_Unless you already have familiarity with the above commands, it is a good idea to follow the PB version closely for this assignment._


## Likely quiz questions

* Give a Linux shell command that achieves each of the following:
  * Copy the first 10 lines of the file `abc.txt` to a new file called `xyz.txt`.
  * Change the permissions of the file `some-script.sh` so that it can be read by anyone but written or executed only by its owner.
  * Assume that the file `numbers.txt` contains only integers appearing in the format of one integer per line. Print out the five largest numbers in the file. If there are duplicates, they should be eliminated. So, we want the five largest unique numbers in descending order.
  * Kill the process whose process ID is `48271`.

* Explain what the following commands do.
  * `cut -f 2,3 -d, data.txt`
  * `wc -w words.txt`
  * `chmod a-w myfile.txt`
  * `chmod ug+w myfile.txt`
