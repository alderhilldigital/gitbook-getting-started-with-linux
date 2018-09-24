# cron

cron is short for '**C**h**ron**os' which is the greek word for time. It is used to execute commands or scripts based on a schedule specified by the user. The schedule can run from every minute through to a specific date and time of the year. It can also specify the day of the week Monday through Sunday. Cron schedules or 'crontab's as they are known are user specific so the root crontab will be a different one to the user1 crontab. crontab is short for 'cron table'.

cron can be enabled by creating a crontab. The crontab command can be used to create a crontab by passing the '-e' option.

**Example**

`crontab -e`

A task is scheduled by configuring the 5 parameters for the schedule followed by the parameters of the task that is to be performed. The following example will output 'Hello World' to the 'hello.txt' file every minute.

**Example**

`* * * * * echo 'Hello World' > '/home/USERNAME/hello.txt'`

Each asterisk represents a time unit as follows:

| Position | Unit of Time |
| :--- | :--- |
| First | Minute |
| Second | Hour |
| Third | Day \(of Month\) |
| Fourth | Month |
| Fifth | Day \(of Week\) |

To make certain schedules easier to run, linux includes a number of fixed schedule files that tasks can be added to. These include daily, hourly, weekly and monthly. They can be accessed by navigating to the /etc directory and creating a file that contains the commands that are to be executed. The following example will create a file called 'myschedule.sh' in the hourly cron directory. This will execute the command '/dir/path/script.sh' every hour.

**Example**

`echo '/dir/path/script.sh' | sudo tee --append /etc/cron.hourly/myschedule.sh`



Time units in cron can also be set at intervals by adding '/interval' to the configuration unit. The following example will output 'Hello World' to the 'hello.txt' file every 10 minutes.

**Example**

`*/10 * * * * echo 'Hello World' > '/home/USERNAME/hello.txt'`



There are also extensions that allow for quick use of predefined events.

| Extension | Event |
| :--- | :--- |
| @hourly | Every hour |
| @weekly | Every week |
| @monthly | Every month |
| @yearly | Every year |
| @annually | Every year \(same as @yearly\) |
| @reboot | On system restart |



