# Bash and Running Scripts

Bash the default command shell for most linux based operating system. The shell provides the functionality to type in and execute commands. It can also run scripts, which are files containing commands.

**Example**

Open a new file called test.sh in a text editor

`nano test.sh`

Insert the following command into the file

`#!/bin/bash  
echo "Hello World!"`

Exit and save by pressing Ctrl+x and Y for yes. The first line defines the system that should be used to execute the command. he second line just displays some text.

To run this script, it needs to executed. We can add execute permissions by running the following [chmod](https://nowthistechnology.gitbooks.io/command-line-essentials/content/chmod.html) command.

`chmod +x test.sh`

The script can now be executed

`./test.sh`

