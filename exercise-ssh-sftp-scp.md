# Exercise \(SSH, SFTP, SCP\)

1. Generate a public/private key pair using ssh-keygen or PUTTYgen
2. Connect to linux vm via ssh with username and password or identity file credentials
3. Copy the contents of the public key file created in step one into /home/USERNAME/.ssh/authorized\_keys
   1. If you are on a linux based system or a OSX based system you can use the ssh-copy-id command
4. Exit the ssh connection by typing exit and pressing enter
5. Connect to linux vm via ssh without specifying any credentials
   1. If this doesn't work, try specifying the path to the private key file created in step one using the '-i' option
6. Connect to the linux vm using sftp
7. Copy a file from the local folder to the remote folder via sftp using the put command
8. While still connected via sftp, confirm the file has been copied using the ls command
9. Copy a file from a remote folder on the linux vm to a local folder using the scp command
10. Copy a file from a local folder to a remote folder on the linux vm using the scp command



