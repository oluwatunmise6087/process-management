# process-management
Start a long-running process in the background
sleep 300 &
![process01](process01.PNG)

List all running processes.
ps aux
![process02](process02.PNG)

Find the process ID (PID) of the sleep process and kill it.
ps aux | grep sleep
kill <PID>
![process03](process03.PNG)

Monitor System Resources
Use top to monitor system resources.
top
![process04](process04.PNG)

# Change Process Priority
Start a new sleep process and change its priority using nice and renice.

nice -n 10 sleep 300 &
![process05](process05.PNG)

renice -n 5 -p 34199
this will not work because I did not add sudo command
![process06](process06.PNG)

sudo renice -n 5 -p 34199
![process07](process07.PNG)