# JUMP SERVER
 A jump server, jump host or jumpbox is a computer on a network used to access and manage devices in a separate security zone. The most common example is managing a host in a DMZ from trusted networks or computers.  

 Jump servers are typically placed between a secure zone and a DMZ to provide transparent management of devices on the DMZ once a management session has been established. The jump server acts as a single audit point for traffic and also a single place where user accounts can be managed. A prospective administrator must log into the jump server in order to gain access to the DMZ assets and all access can be logged for later audit.

 A typical configuration is a hardened Unix (or Unix-like) machine configured with SSH and a local firewall. An administrator connects to a target machine in the DMZ by making an SSH connection from the administrator's personal computer to the jump server and then using SSH forwarding to access the target machine.

 Using an SSH tunnel to the target host allows the use of insecure protocols to manage servers without creating special firewall rules or exposing the traffic on the inside network.
 > ![Jump Server](https://github.com/GitanjaliRavichandran/git/blob/master/bastion.png)
# Steps to Create a Jump Server
1. Create a VM instance with default network by giving an external IP which acts as a host.
1. Copy and paste the ssh key for the above newtowrk(JumpServer)
1. Generate the firewall rule to the above network inorder to allow other instances to that network.
1. Create another VM instance with default network without giving an external IP(Client)
1. SSH Key should be generated for the above instance too and this key should also be pasted in the host network  
1. Create the VPC Peering rule such that the  host is peered with a default network and vice versa.
![Peering](https://github.com/GitanjaliRavichandran/git/blob/master/Selection_017.png)
> Now we can access the client by using the jump server ssh. 



 
