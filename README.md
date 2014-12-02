apt-get install dnsmasq -y


56 # Example of routing PTR queries to nameservers: this will send all
57 # address->name queries for 192.168.3/24 to nameserver 10.1.2.3
58 #server=/3.168.192.in-addr.arpa/10.1.2.3

/etc/hosts

/etc/hostname

/etc/reslov.com


2 # Add the IPs of all queries to yahoo.com, google.com, and their
73 # subdomains to the vpn and search ipsets:
74 #ipset=/yahoo.com/google.com/vpn,search

fully qualified domain names


Ubuntu14.04修改DNS服务

http://www.netroby.com/view.php?id=3630#.U4aRT_mSzVo

Persist dns nameserver for ubuntu 14.04

If you are using ubuntu 14.04, you may find you can not setting dns on your /etc/resolv.conf

This is because ubuntu using resolvconf to manage the dns setting, every times system boot, resolvconf will regenerate resolv.conf file.

But there always have way to do this.



vim /etc/resolvconf/resolv.conf.d/head  


put your nameserver list in



nameserver 8.8.8.8
nameserver 8.8.4.4
then run




resolvconf -u


this command tell resolvconf to regenerate the resolve file

enjoy it.
