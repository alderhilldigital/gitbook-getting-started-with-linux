# ssh

SSH is short for "**S**ecure **Sh**ell". It is used to communicate securely between a client and a server. The client PC must have ssh tools available. The most common tool for using ssh are in the OpenSSH package. Most linux based systems will have OpenSSH installed by default and the ssh tool can be used without any additional requirements. The ssh server must have ssh server tools installed. This can be done on OSX by turning on "remote login" in preferences &gt;&gt; network or installing the open-ssh package in linux.

`sudo apt-get install openssh-server`

or

`sudo yum install openssh-server`

Using the ssh tool to connect to a remote server requires the location and authentication credentials. The most basic authentication is using a user name and password. The username can be passed in as part of running the ssh command and then the user would be prompted to enter the password.

`ssh user@server_address`

# scp and sftp

Two other tools in the OpenSSH suite are scp and sftp. scp, which is short for "**S**ecure **C**o**p**y", is used to copy files to and from the ssh client and server.

**Example**

`scp /my-files/hello.txt user@server_address:/remote-files`

This will copy the hello.txt file from the local directory 'my-files' to the 'remote-files' directory or the server.

sftp is a tool that can also be used to send and receive files over a secure connection. It has an interactive mode that once the connection is established, the user can run commands to select and transfer files. For more information on these interactive commands, view the manual at [http://man.openbsd.org/OpenBSD-current/man1/sftp.1](http://man.openbsd.org/OpenBSD-current/man1/sftp.1)

