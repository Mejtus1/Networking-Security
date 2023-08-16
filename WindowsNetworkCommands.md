# Networking-Security
---------------------

Basic Networking commands for Windows 

ping
ping google.com = sends ICMP packets to DNS address google.com
- it is used detecting devices on network and troubleshooting network problems
- It will help to see the connection between your device and another device on the network
- if we receive a reply from the device then the device is working properly

ipconfig
ipconfig /all = displays IP configuration settings of all known devices
ipconfig /flushdns = clears the DNS resolver cache
- find network information local devices like IP Address and default gateway

netstat
netstat -a = displays active network connections 
- network statics, diagnostics, and analysis
- By running this command, will show the number of active connections on the system.

arp
arp -a 
- MAC address and hardware address

nslookup
nslookup google.com
- performs DNS queries to retrieve information about domain names and IP addresses.

route print
- displays or modifies the local IP routing table, showing how network traffic is directed

tracert
tracert google.com = traces route to google.com from your device
- traces the route that packets take to reach a destination
- showing each hop's IP address and response time

netsh wlan show interfaces
- displays detailed information about your wireless network interfaces
netsh wlan show profiles
- displays the list of wireless network profiles saved on your computer
netsh advfirewall show currentprofile
- displays the currently configured Windows Firewall settings
netsh int ipv4 show dynamicportrange tcp
- shows dynamic range for tcp port connection (example from 16384 to 49152)
