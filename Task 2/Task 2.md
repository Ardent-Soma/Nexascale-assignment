## Task 2: System Monitoring & Performance Analysis

### Indentifying top consuming process
The "top" command is use to check the processes that are running. In this case it is "Xorg" using a memory of 7% and CPU of 1%.
It is a neccessary process because it is the graphical server for Linux that is it's responsible for displaying the desktop environment.
### Checking the disk usage
The command "df -h" is used to check the disk space and "du -sh /var/log/*" to see if the logs are consuming too much space.
### Checking real time logs
"sudo journal -f" was used to check real time logs and no anomalies was detected