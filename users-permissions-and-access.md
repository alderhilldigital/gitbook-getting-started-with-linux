# Users, Permissions and Access

Linux based operating systems allow for multiple users at one time. User accounts can be set up with permissions based on a specific user or a group of users. Groups can have zero or more users and permissions can be allocated to any group.

## Basic Permissions

There are 3 basic permissions when it comes to what a user can do, read, write and execute.

**Read \(r\)** - this allows a user or group to view a file which includes the name, content, size, etc. Read access on a directory allows the user or group to list the contents of the directory and view the some information about the contents.

**Write \(w\)** - this allows a user or group to modify a file. Write access on a directory allows a user or group to modify the contents of the directory i.e. add and delete files.

**Execute \(x\)** - this allows a user or group to run a file and execute a script or application. Execute access on a directory allows the user or group to change to that directory and make it their current working directory.

To view these permissions we can use the 'ls' command which lists the content of a directory. Adding the '-l' flag will show the permissions information. Each file in the directory will be listed with a 10 character string that indicates it's permissions.

**Example**

`ls -l /home      
-rwxrw-r-- 2 root admin 2045 9 Mar 2017 test.txt`

Running the 'ls -l' command on the 'home' directory has listed the files and 10 pieces of information about each file.

1. File permissions in a 10 character format
2. Number directories or links in the subdirectory \(1 if it is a file\)
3. User who is designated as the owner
4. Group that is designated as the owner
5. File size in bytes
6. Last modified date
7. File name

## Understanding File Permissions

The 10 character format for file permissions breaks down into 1 special character and 3 sets of 3 characters. The special character is not covered in this content. Each set of 3 characters \(triad\) corresponds to an owner, group or all. The first triad is for the owner, the second for the group and the third for all users.

**Example**

-rwxrw-r-- splits into:

\[-\] special character  
\[rwx\] permissions for the owner \(read, write and execute\)  
\[rw-\] permissions for the group \(read and write\)  
\[r--\] permissions for all users \(read only\)

## The Octal Format for Permissions

Each triad can be represented as a number using an octal numbering system i.e. there are 8 combinations of 3 characters and the characters can have an assigned number that can be added to get the total

r = 1  
w = 2  
x = 4

0 = ---  
1 = r--  
2 = -w-  
3 = rw- \(1+2\)  
4 = --x  
5 = r-x \(1+4\)  
6 = -wx \(2+4\)  
7 = rwx \(1+2+4\)

This numeric notation can also be used to set permissions using the 'chmod' command

**Example**

chmod 750 test.txt

This will set the permissions of 'test.txt' as follows

| Numeric | Symbolic | Permission |
| :--- | :--- | :--- |
| 7 | wrx | Read, write and execute for owner |
| 5 | r-x | Read and execute for group |
| 0 | --- | No permissions for all other users |

## Permission Shortcuts

There are some command shortcuts that allow for permissions to be assigned without the need to know what permissions currently exist. There are characters assigned to owner, group and all users \(u,g,a\) that can have permissions added or substracted from them using the read, write execute characters \(r,w,x\).

**Example**

`chmod g+w test.txt`

This will add write permissions to the group for the 'text.txt'.

## Managing Users





