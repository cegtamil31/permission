#JUMPSERVER

##WITHIN DEFAULT NETWORK

1. create a VM instance with default network with external IP to act as a host.
2. create another VM instance with default network without external IP to act as host.
3. paste the host sshkey to VM .
4. now we cannot access ssh of client directly.
4. now connect to host instance to access client.
 
##AMONG MULTIPLE NETWORKS

1. create the new vpc network.
2. create the new VM instance with the new network without external IP.
3. create the firewall rule to new network to allow other instance to the network.
3. create the network peering rule from default network to new network.
3. similarly network peering rule from new network to deafult network.
3. copy the host key in default network to VM in new network.
3. now we can access the VM client through host.
