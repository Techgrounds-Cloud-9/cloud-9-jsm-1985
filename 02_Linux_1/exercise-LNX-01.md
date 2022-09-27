#  Connecting to remote server

  Connection to a remote server can be either password based authentication or key-based authentication. For this exercise, the given pem file was used to connect to the remote ubuntu server.
  On the

## Key terminology

 1. ssh-A networking protocol used to access remote servers securely.
 2. port number -in a network of connected devices, port number helps to identify the unique processes or applications running on it

 
## Exercise
### Sources

https://www.simplified.guide/ssh/connect-to-different-port

https://stackoverflow.com/questions/34045375/connect-over-ssh-using-a-pem-file

https://superuser.com/questions/1666505/how-to-set-600-permission-on-a-pem-file-in-w10


### Overcome challenges
The connection to the remote server was made using mobaXterm(a tool similar to putty for remote-connections) for the first time . Had to give the path to the pem and change the default port number from 22 to 58007.

For the second time, remote-server access was done via windows power shell. Had to search how to specify the pem file location and how to specify a different port number in CLI.(If done via windows power shell for the first time, the permission of the key needs to be set to 600. else it throws bad permissions error.)



### Results


##### ![LNX-01-01img](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/LNX-01-01.PNG)


##### ![LNX-01-02img](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/LNX-01-02.PNG)













