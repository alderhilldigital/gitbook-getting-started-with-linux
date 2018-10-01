# Exercise \(Services\)

1. Log into Linux either directly to VM or through SSH
2. Run the 'ps ax' command to see a list of all processes running
3. Pipe the 'ps ax' command into the grep command and search for 'cron'
4. List the contents of the /etc/init.d directory
5. As super user pass the restart option to the cron initialisation script
6. As super user pass the restart option to the service command for cron \(this will do the same as No. 5\)
7. Run the following command 'ls -al /etc/rc5.d' and take note of the service for 'ssh'
8. As super user pass the disable option to the systemctl command for ssh
9. Re-run the 'ls -al /etc/rc5.d' command and take note of the _absence_ of the service for 'ssh'
10. As super user pass the enable option to the systemctl command for ssh to re-enable the ssh on reboot



