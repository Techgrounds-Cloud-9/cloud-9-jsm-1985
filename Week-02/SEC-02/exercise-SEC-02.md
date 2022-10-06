#  Firewalls

Firewalls mainly a part of network security controls the traffic by allowing or denying it.It examines each data packet and decide if the packet is a source of threat and discards the packets accordingly.

## Key terminologies

Stateful firewall - Can moitor and detect staes of all traffic based on traffic patterns and flows even those not manually given by the administrator.

Stateless firewall - Can focus only on individual data packet and check its source, destination and other parameters set by the administrator beforehand.

Hardware firewall - Physical devices each with its own computing resources. More suitable for organisations with large networks.

Software firewall -Installed on individual devices. Are more expensive because of the resources utilization,but gives more control.

ufw - uncomplicated firewall. It i the default firewall configuration for ubuntu.

## Exercise
1. Install a web server on your VM.View the default page installed with the web server.

2. Set the firewall to block web traffic, but allow ssh traffic. Make sure the firewall is working.


### Sources

https://linuxize.com/post/how-to-setup-a-firewall-with-ufw-on-ubuntu-20-04/#:~:text=Ubuntu%20ships%20with%20a%20firewall,as%20the%20name%20says%2C%20uncomplicated.

https://www.digitalocean.com/community/tutorials/how-to-set-up-a-firewall-with-ufw-on-ubuntu-20-04

https://www.cdw.com/content/cdw/en/articles/security/stateful-versus-stateless-firewalls.html#:~:text=Stateful%20firewalls%20are%20capable%20of,preset%20rules%20to%20filter%20traffic.

https://www.fortinet.com/resources/cyberglossary/stateful-vs-stateless-firewall


### Overcome challenges
Had to find out how the firewalls work on ubuntu server. Understood it while implementing the ufw commands. The default page of apache2 was accessible initially. After denying the traffic by setting the deny rule, the page became inaccessible.

### Results


##### ![SEC-02-01-Installnmapimg](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-02/SEC/SEC-02-01-ITWorks.PNG)

##### ![SEC-02-02-ufwEnablenmapimg](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-02/SEC/SEC-02-02-ufwEnable.PNG)

##### ![SEC-02-03-denyApachepimg](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-02/SEC/SEC-02-03-denyApache.PNG)

##### ![SEC-02-04-unreachableWebsiteimg](https://github.com/Techgrounds-Cloud-9/cloud-9-jsm-1985/blob/main/00_includes/Week-02/SEC/SEC-02-04-unreachableWebsite.PNG)












