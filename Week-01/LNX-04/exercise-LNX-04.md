#  Users and Groups

Linux supports multiple users simultaneously. Each user has their own account. The root user has all the permissions to execute any  command whereas other users have only restricted previleges. The priveleges of a user can be changed by adding them to the sudoers list. Similarly when a user is created,he belongs to a group with the same name. A user can be added or deleted to/from a group. 

## Key terminology

  1. useradd- to create a new user
  2. groupadd- to create a group
  3. passwd -to set the password for the user
  4. usermod -aG - add user to a group.
  5. /etc/group - file in all groups are stored
  6. /etc/passwd-file in which all users are stores
  7. /etc/shadow- file which stores encryoted passwords.
  8. visudo-file to which users can be added to change their permisssions.
   
  
## Exercise
### Sources

https://www.digitalocean.com/community/tutorials/how-to-edit-the-sudoers-file

https://manpages.ubuntu.com/manpages/bionic/en/man5/passwd.5.html

https://www.cyberciti.biz/faq/howto-linux-add-user-to-group/

https://medium.com/analytics-vidhya/how-to-add-users-to-sudoers-file-in-ubuntu-e89c24b7369d


### Overcome challenges
Had to look up how to add a user to a sudoer list so as change the privileges.Understood by using the visudo command which opens the /etc/sudoers file using vi editor. I was able to add a new user to the file and grant the user the same previleges as the root user and enabled passwordless authentication to execute the commands. 

### Results


##### ![LNX-04-01img](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/LNX-04/LNX-04-01.PNG)


##### ![LNX-04-02img](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/LNX-04/LNX-04-02.PNG)


##### ![LNX-04-03img](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/LNX-04/LNX-04-03.PNG)


##### ![LNX-04-04img](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/LNX-04/LNX-04-04.PNG)

##### ![LNX-04-05img](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/LNX-04/LNX-04-05.PNG)

##### ![LNX-04-06img](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/LNX-04/LNX-04-06.PNG)


##### ![LNX-04-07img](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/LNX-04/LNX-04-07.PNG)


##### ![LNX-04-08img](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/LNX-04/LNX-04-08.PNG)


##### ![LNX-04-09img](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/LNX-04/LNX-04-09.PNG)

