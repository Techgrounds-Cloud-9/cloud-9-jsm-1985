#  Processes

The 3 modes in which a process can be run in a Linux are

Deamons - A process that runs continuously in the background and wakes up to handle periodic service request from remote processes.Its usually non interactive

Services- A combination of resources to provide some functionality, responding to requeats from programs.Can be interactive.

Programs-Run and used by users to accomplish a task.

## Key terminologies

  1. ps -aux -  to get the detailed list of all the processes running on the system like  user account under which its running,pid, %CPU, %memory etc. Combined with grep it helps to filter the process of interest for us.

  2. top - to see the real time view of running processes 

  3. kill - to kill the unwanted processes.
   
  
## Exercise
### Sources


https://en.wikipedia.org/wiki/Telnet#:~:text=Telnet%20is%20a%20client%2Dserver,application%20(telnetd)%20is%20listening.

https://linuxhint.com/find-process-id-ubuntu/

https://askubuntu.com/questions/104903/how-do-i-kill-processes-in-ubuntu

https://help.interfaceware.com/v6/differences-between-processes-daemons-and-services

https://linux-audit.com/running-processes-and-daemons-on-linux-systems/


### Overcome challenges

Had to look up on how to install and start the telnetd (telent deamon) server in ubuntu. Understood it while implemeting the command "sudo apt install telnetd" and checked the status of inted using systemctl status command.

### Results


##### ![LNX-06-01img](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/LNX-06/LNX-06-01.PNG)


##### ![LNX-06-02img](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/LNX-06/LNX-06-02.PNG)


##### ![LNX-06-03img](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/LNX-06/LNX-06-03.PNG)


##### ![LNX-06-04img](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/LNX-06/LNX-06-04.PNG)



