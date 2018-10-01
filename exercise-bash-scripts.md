# Exercise 1 \(Bash Scripts\)

1. Log into Linux either directly to VM or through SSH
2. Create a file called 'Hello.sh' containing the following text:
   `!#/bin/bash`
   `echo 'Hello World'`
3. Add execute permissions on the 'Hello.sh' file
4. Run the Hello.sh file
5. Change the text in the 'Hello.sh' file to the following:
   `!#/bin/bash`
   `time=$(date +%Y-%m-%d)`
   `echo 'Hello World it is $time'`
6. Run the Hello.sh file
7. Change the text in the 'Hello.sh' file to the following:
   `!#/bin/bash`
   `time=$(date +%Y-%m-%d)`
   `echo 'Hello $1 it is $time'`
8. Run the Hello.sh file and pass in your name after the script call e.g. ./Hello.sh Joe
9. What will the following script do?
   `MAX=95`
   `EMAIL=server@127.0.0.1`
   `PART=xvda1`

   ``USE=`df -h | grep $PART | awk '{ print $5 }' | cut -d'%' -f1```
   `if [ $USE -gt $MAX ]; then`
   ` echo "Percent used: $USE%" | mail -s "Running out of disk space" $EMAIL`
   `fi`
10. Update the script from step 9 to return a separate output when the conditions of the if statement are not met





