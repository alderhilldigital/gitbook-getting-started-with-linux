# Services

Linux services are applications that run in the background waiting for events to initiate particular processes or providing regular functionality. Common services on a linux system include apache and cron. For the majority of linux distributions, initialisation scripts for these services are located in either the /etc/init.d directory or the /etc/init directory.



**Initialization file**

The initialisation file for a service can implement a number of functions that are used to carry out different tasks for the service. The minimum requirement for an initialisation file is that is contains a start and stop function. Other common functions include restart, reload and status.



**service command**

The service command provides the user with a high level way of managing services. It is used to call methods in a service initialisation file.  It will check both the /etc/init.d and /etc/init directories for an existing initialisation file. Once it has found an initialisation file it will run the command to execute the function in the file. The following example will restart the apache2 service:

**Example**

`sudo service apache2 restart`

This would be the same as calling the script directly:

`sudo /etc/init.d/apache2 restart`

Or through systemctl command which is the old way of calling systemd scripts:

`sudo systemctl restart apache2`



**systemctl command**

The systemctl command is used to manage functions within the systemd suite. The service command does provide a helpful wrapper for a few systemctl commands but most of its functions can only be done form systemctl. Couple of useful ones are enable/disable and show



**Enable/Disable**

The enable and disable commands will add and remove the service from startup process so that if the system is rebooted the service will either be automatically started or not. The following example will stop mysql from running when the system is restarted.

**Example**

`sudo service mysql disable`



**Show**

The show command lists all the properties of a particular service.

**Example**

`sudo service mysql show`

