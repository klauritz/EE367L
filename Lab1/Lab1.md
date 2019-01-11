# Lab 1: Introduction and UNIX Basics

This page can be viewed by going to https://bit.ly/2sky3Yc
Individual Assignment

Due Next Week Thursday at **12:00PM**

Make sure you've done the following before proceeeding:
 - Set up/get access to your wiliki account
 - Read or skim through the UNIX document associated with Lab 1.

## Part A: Introduction to UNIX
1. Log in to your wiliki account using putty or ssh.
    - If you want to use your terminal to remotely access wiliki, you can use the following command: 
 `ssh {$USERNAME}.wiliki.eng.hawaii.edu` then enter your password when prompted.

 2. Create a directory called EE367
    - You can use the `mkdir` command to create a directory in UNIX. [See here](https://www.techonthenet.com/unix/basic/mkdir.php) for more info on this command.

3.  Download the Lab1.tar.gz file from laulima and transfer it to your EE367 directory
    - To upload something to wiliki, you can either use FileZilla or the `scp` command (stands for **s**ecure **c**o**p**y). More info on the command [here.](https://www.computerhope.com/unix/scp.htm)
    - When using the `scp` command, please note that it does not work when you are within wiliki. Use this command on your local machine, **NOT** wiliki. 

4.  Ungzip and untar the file which should give you a Lab1 directory.   The rest of the lab deals with this directory. 
     - Once uploaded, you can decompress and unarchive the folder by using the `tar -xzf` command. More info [here.](http://www.rebol.com/docs/unpack-tar-gz.html)

5.  Find the file “egg.txt” (Easter Egg) in Lab1.  Navigate around using cd to find the egg.  Then go back to the Lab 1 
directory and then use the find command.  Open the file and find out what color it is.  You can review the file by using 
“more” or “cat”, or you can use a text editor like vi or pico. 

6. Find the file "letter.txt". Edit the file using `vi` or `pico`. Once finished download the file from wiliki to your local machine.
    - Although the handout says to use `vi`, I recommend using `vim`. It's a much more robust and updated text editor.
    - You can download files from wiliki by using the `scp` command, as seen on step 3.

7.  Go to Post Room 100.  Read the README file.  Compile and run the different files according to the README file. 
    - Program 2 does not have `#include <stdio.h>`, so it will throw a warning at you. 

8.  Go to Moore Room 307.  Read the README file.  Create a makefile according to the README file. 
    - hello c files do not have `#include <stdio.h>` so it will throw a warning at you.
    - For more information on how to create makefiles, please refer to [this website.](http://www.cs.colby.edu/maxwell/courses/tutorials/maketutor/)

9.  Go to Moore/RoomScript.  Read the README file.  Run the samplescript. 
    - test.c does not have `#include <stdio.h>` so it will throw a warning at you

10.  You should take the time to explore UNIX and trying things on your own.  The UNIX intro document is a starting point to explore.

## Part B: Shell Scripting

**Instructions:**  This is an exercise on using shell scripts to process data.  In laulima in this assignment, there should be a 
Lab1B.tar file.  Download the file and transfer it into your wiliki account.  Untar it and notice that it creates a directory 
Lab1‐2012, which has a files and a subdirectory.  Read the README file to learn the contents.   
 
Notice a subdirectory Data has ten data files:  “datafile‐0”, “datafile‐1”, etc.  Each of these data files can be processed by 
a program called “sum.c”, which has the executable “sum”.  The makefile will create the executable.  The “sum” 
program will sum the data values in a file and output the results. 
 
Your task is to create a shell script, named “scriptlab1”, that will run in the directory Lab1‐2012 on wiliki.  The script will 
use “sum” to process each data file in “Data”.  The outputs are put into a file (you create) called “lab1b‐results”, and its 
contents should look like this 
 
Sum from data file Data/datafile‐0 is 906 

Sum from data file Data/datafile‐1 is 1119 

... 

Sum from data file Data/datafile‐9 is 1176 

**What to turn in:**  After you’ve created your shell script, tar the file and gzip it.  Then upload it into laulima as part of the 
assignment.  Also demonstrate it to the teaching assistant (TA).

**Notes:**

 - Be careful with your whitespace in the scripts. *They actually matter*. For example: `x=0` is valid syntax but `x = 0` is not.
 - To compress and zip things, use:

   `tar -czvf name-of-archive.tar.gz /path/to/directory-or-file`

 - Don't forget to include letter.txt in your zipped folder as well!
