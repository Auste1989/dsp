# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> >
Command description | Command
------------------- | -------
show current working directory path | pwd
creating a directory | mkdir *directory_name*
deleting a directory | rm -r *directory_name*
creating a file using 'touch' command | touch *file_name*
deleting a file | rm *file_name*
renaming a file | mv *old_file_name* *new_file_name*
listing hidden files | ls -a
copying a file from one directory to another | cp /*source_file* /*destination_directory*
counting lines, words and charachters in the file | wc *file_name*
returning a list of unique lines in a file | uniq *file_name*
search for lines matching the given pattern and return results | grep **pattern** *file_name* 
find and replace | sed **action/search_string/replacement_string/[g]** *file_name*

---

### Q2.  List Files in Unix   

What do the following commands do:  
'ls'   
`ls -a`   
`ls -l`  
`ls -lh`   
`ls -lah`   
`ls -t`  
`ls -Glp`  

> > 
Command | Description
------- | -----------
`ls` | lists directories and files in the working directory
`ls -a` | lists	 all contents of  working directory, including hidden files
`ls -l`	 | lists all contents of  working directory in long format
`ls -lh` | lists working directory contents in long human readable format
`ls -lah` | lists all working directory contents (incl. hidden) in long human readable format
`ls -t` | lists	contents of working directory sorted by	last modified date and time
`ls -Glp` |  lists contents of the working directory in long format, adds '/' at the end of each directory name and enables colourized output

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > **My Favourite ls options are:**

Command | Description
------- | -----------
ls -m   | Displays the names as a comma-separate list
ls -R   | Displays sub-directories as well
ls -u   | Displays files by the file access time.
ls -F   | Flags filenames
ls -p   | Displays directories with /

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > 'xargs' command allows iteration through a list (item by item).  It can be used for updating multiple files at once or searching for text in each file in the directory.

 

