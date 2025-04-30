# Shell Scripting Tutorial
<p align = "center">
<img width = 200 height = 200 src ='https://www.techasoft.com/debug/img/shell-script.png'>
</p>

 If you are a beginner in shell scripting, you are in the right place to learn it from scratch.

 So, let's get started :muscle:

## *WHAT IS SHELL SCRIPTING*
Shell scripting is a way to automate tasks in a **Unix/Linux** environment by writing a series of commands in a text file (called a script). These scripts are executed by the **shell**, which is a program that interprets and runs commands.

### Basics
- #### Making/Removing directory

  `mkdir` -> To make a new directory.

  For example:
  ```
  mkdir newfolder
  ```
  
  `rmdir` -> To delete directory.

  For example:
  ```
  rmdir newfolder
  ```
- #### Making/Removing File
  
  `touch` -> To make a new file.

  For example:
  ```
  touch aleeza
  ```
  `rm` -> To delete a file.

  For example:
  ```
  rm aleeza
  ```
- #### Navigating Directories

  `cd ~` -> Go to **Home** directory.

  `cd directory` -> Change directory.

  For example:
  ```
  cd UART
  ```
  `cd ..` -> Go up one directory.

  `pwd` -> Print current directory path.
#

  *Here is the example code to see current directory, make new directory, go inside that directory and make new file. Then delete that file and directory*

  ```
  pwd
  mkdir newfolder
  ls
  cd newfolder
  pwd
  touch aleeza
  ls
  rm aleeza
  ls
  cd ..
  pwd
  rmdir newfolder
  ```

