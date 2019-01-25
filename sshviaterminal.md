#SSH VIA TERMINAL UBUNTU

1. execute "ssh-keygen -b 4096".
2. navigate to ".ssh".
3. copy the content of "id_rsa.pub".
4. paste it in instance "ssh-keys" box in the VM or navigate to ".ssh" then crea   te "authorized_keys".
5. now connect to VM via terminal using "ssh username@external_ip".

#SSH PORTCHANGE

1. navigate to "/etc/ssh".
2. open ".sshd_conf" change the port "2222(or any port no)".
3. then create the firewall rule under vpc networks with following 
   i)target tags-for which VM instance
   ii) source ip-for specific ip range to access or all ip.
   iii)specified port-tcp:2222(or port no changed in sshd_conf)
   iv)click  create.

#IPWHITELISTING

1. to block particular ip or range of ip to specified port or multiple port
2. here we whitelist for ssh
   i) to allow specific ip
      sudo iptables -A INPUT -p tcp -s external ip  --dport 22 -j ACCEPT
      sudo iptables -A INPUT -p tcp -s internal ip  --dport 22 -j ACCEPT
   ii)to block all other ip
      sudo iptables -A INPUT -p tcp -s 0.0.0.0/0 --dport 22 -j DROP.
3. similarly for all other ports 
4. multiple ports use , after port no.

 
 
