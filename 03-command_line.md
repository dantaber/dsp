# Learn command line

Please follow and complete the free online [Command Line Crash Course
tutorial](https://web.archive.org/web/20160708171659/http://cli.learncodethehardway.org/book/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. Each "chapter" focuses on a command. Type the commands you see in the _Do This_ section, and read the _You Learned This_ section. Move on to the next chapter. You should be able to go through these in a couple of hours.

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

> > **CHEAT SHEET**  
**cd**: change directory  
**pwd**: show current directory  
**mkdir**: create directory  
**rmdir**: delete directory  
**touch**: create a file  
**rm**: deleting a file  
**mv**: renaming a file  
**ls**: listing hidden files  
**cp**: copying a file from one directory to another  
**less**: display a file  


---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > `ls` - lists files  
`ls -a` - list all files including hidden files  
`ls -l` - list all files in long format     
`ls -lh` - list all files in long format, with readable file size  
`ls -lah` - list all files, including hidden, in long format with readable file size  
`ls -t` - list files sorted by time and date  
`ls -Glp` - list files in long format, marking directories with '/'  

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > `ls -1` - list files, 1 per line  
`ls -d` - list only directories  
`ls -R` - list sub-directories  
`ls -g` - list in long format without the owner  
`ls -r` - list files in reverse order  

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > `xargs` executes a command on all of the items that are read from standard input. It's useful for repeating an operation on many files at once. For example, if I wanted to search my ds directory for every Python file where I mention 'nutmeg', I could type:

`find ds -name "*.py" | xargs grep "nutmeg"`

 

