# Shell Scripting Tutorial
<p align = "center">
<img width = 200 height = 200 src ='https://www.techasoft.com/debug/img/shell-script.png'>
</p>

 If you are a beginner in shell scripting, you are in the right place to learn it from scratch.

 So, let's get started :muscle:

## *WHAT IS SHELL SCRIPTING* :computer:
Shell scripting is a way to automate tasks in a **Unix/Linux** environment by writing a series of commands in a text file (called a script). These scripts are executed by the **shell**, which is a program that interprets and runs commands.

### <u>Basics</u>
- #### Making/Removing directory

  📍`mkdir` -> To make a new directory.

  For example:
  ```
  mkdir newfolder
  ```
  
  📍`rmdir` -> To delete directory.

  For example:
  ```
  rmdir newfolder
  ```
  #
- #### Making/Removing File
  
  📍`touch` -> To make a new file.

  For example:
  ```
  touch testfile
  ```
  📍`rm` -> To delete a file.

  For example:
  ```
  rm testfile
  ```
  #
- #### Navigating Directories

  📍`cd ~` -> Go to **Home** directory.

  📍`cd directory` -> Change directory.

  For example:
  ```
  cd UART
  ```
  📍`cd ..` -> Go up one directory.

  📍`pwd` -> Print current directory path.
#

  *Here is the example code to see current directory, make new directory, go inside that directory and make new file. Then delete that file and directory*

  ```
  pwd
  mkdir newfolder
  ls
  cd newfolder
  pwd
  touch testfile
  ls
  rm testfile
  ls
  cd ..
  pwd
  rmdir newfolder
  ```
  #
### <u>Primary shell scripting</u>

  - #### Making & Running shell script
   1. Create new file in your editor (e.g. Vim or VS code) and save it with the extension `.sh`.
   2. Make it executable by writing `chmod +x filename.sh` in editor's terminal.
   3. To run the file, write `./filename.sh` in **shell**.
   #
  - #### Commands
    📍`echo` -> To display text.

    For example:
    ``` 
    echo "Hello world!"
    ```
    📍`$` -> To display variables.

    For example:
    ```
    #!/bin/bash

    name="Aleeza"
    echo "Hello! I am $name"
    ```
    Output:
    ``` 
    Hello! I am Aleeza
    ```
    📍`-e` and `\n` -> To enter new line.

    For example:
    ```
    echo -e "line1 \n line2"
    ``` 
    📍`-n` -> To suppress newline.

    For example:
    ```
    echo -n "Hello"
    echo " World"
    ```
    Output:
    ```
    Hello World
    ```
   # 
  - #### Comments
    📍 `#` -> For comments in code

    For example:
    ```
    #This is a comment that only shows in code, not in output when file is run
    ```
  #
  - #### Conditionals
    📍 `if`,`then`, `else`

    Example:
    ```
    if [ $name == "Aleeza" ]; then
       echo "Name matches"
    else
       echo "Name does not match"
    ```
    📍 `fi` -> To end if block.

   #
  - #### Loops
    📍 `for`,`do`,`done` -> For *for loop*.

    Example:
    ```
    for i in {1..5}
    do
      echo "Loop iteration $i"
    done
    ```
    📍 `while` -> For while loop.

    📍 `-le` -> used as **less than or equal to** operator.

    For example:
    ```
    i=1
    while [ $i -le 5 ]
    do
      echo "Number: $i"
      i=$((i + 1))
    done
    ```
#
- #### Reading User Input</u> 

  📍 `read` -> To take input from user.

  📍 `-p` -> Prompts the user to provide input (displays a message on the screen).

  For example:

  ```
  read -p "Enter your name: " username
  echo "Hello, $username!"
  ```
#
### <u>File Manipulation</u>

- #### Viewing Files Content: 

  📍`cat` -> Viewing File contents.

   For example:
   ```
   cat testfile.txt
   ```
  📍`head` –> Show the first 10 lines of a file.

   For example:
   ```
   head testfile.txt
   ```
  📍`head -n` -> To view a custom number of lines.

   For example:
   ```
   head -n 5 testfile.txt  # Show first 5 lines 
   ```
  📍`tail` –> Show the last 10 lines of a file.

   For example:
   ```
   tail testfile.txt
   ```
  📍`tail -n` -> To view a custom number of lines.

   For example:
   ```
   tail -n 5 testfile.txt  # Show last 5 lines
   ```
#

- #### File operations: 
  
   📍`cp` -> To copy a file.
   
   For example:
   ```
   cp file1.txt file2.txt 
   ```
   *Copies file1 in the same directory with the name file2.*
   ```
   cp file1.txt /home/aleeza/Documents/
   ```
   *Copies file1 in this directory with same name.*
   ```
   cp file1.txt /home/aleeza/Documents/newname.txt
   ```
   *Copies file1 in this directory with the name newname.*
   
   📍`mv` -> To move or rename a file.

   For example:
   ```
   mv oldname.txt newname.txt
   ```
   *Rename a file from oldname to newname*
   ```
   mv file.txt /path/to/destination/
   ```
   *Move a file to another directory.*
### <u>Searching in files</u>
   *In shell scripting, `grep` is a powerful command-line utility used to search for patterns in text depending on our needs.*

   📍`grep` -> To find a word in lines in a file.

   For example:
   ```
   grep "word" filename
   ```
   📍`grep -i` -> Makes the search case **insensitive**.

   For example:
   ```
   grep -i "error" filename
   ```   
   *It will find all words regardless of letters being uppercase or lowercase e.g. ERROR, error, Error.*

   📍`grep -v` -> Prints lines that do not match the pattern.

   For example:
   ```
   grep -v "DEBUG" file.txt

   ```
   📍`grep -r` or `grep -R` -> To search for the pattern recursively through all files in the directory and subdirectories.

   For example:
   ```
   grep -r "lahore" ./src/

   ```
   *This will search for the word **lahore** in all files under the src directory, including subdirectories.*

   📍`grep -n` -> Shows the line number in the output where the match is found.

   For example:
   ```
   grep -n "function" newfile.sh

   ```
 
   📍`grep -c` -> Prints the number of lines that match the pattern.
   For example:
   ```
   grep -c "word" file.txt

   ```
  
   📍`grep -l` -> Shows the names of files that contain the matching pattern.

   For example:
   ```
   grep -l "lahore" *.sh
   ```
   *Names all shell files containing the word **lahore**.*
   ```
   grep -l "lahore" *.js
   ```
   *Names all JavaScript files containing the word **lahore**.*

   📍`grep -L` -> Shows the names of files that do not contain the matching pattern.

   For example:
   ```
   grep -L "word" *.sh

   ``` 
  ## References
  You can learn more shell scripting [here](https://missing.csail.mit.edu/2020/shell-tools/).
  
  Some other websites to learn shell scripting from are [tutorialspoint](https://www.tutorialspoint.com/unix/shell_scripting.htm) and [geeksforgeeks](https://www.geeksforgeeks.org/introduction-linux-shell-shell-scripting/).

  
