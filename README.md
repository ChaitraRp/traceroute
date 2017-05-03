# This repository contains implementation of traceroute

Some operating systems like Windows 10, Windows Server OS do not have traceroute in it. These operating systems come with an alteranative to traceroute named  as "tracert".

This was developed for learning purposes and is in favour of those people who love UNIX and would like to stick to the word "traceroute" even under circumstances when they are using Windows and other OS that do not have traceroute in it.

The main aim of this project is to develop a network tool which can be used to show the route taken by packets across an IP network. This tool would inject an IP packet into the available network interface and wait for the reply from the intermediate routers and the destination IP, giving information about the network setup and the firewall configuration on each intermediate node.

UDP datagram are used as probe packets and waiting for an ICMP-ECHO-REPLY. This UDP datagram passes through every intermediate router which in turn replies with an ICMP message. From the received message the address of the intermediate routers are retrieved. Hostnames are mainly displayed however in certain exceptions only IP addresses is displayed. This algorithm does not suffer from a changing path and allows the response to the Return Packet to be traced.

Traceroute is a program that can be used to send packets of information to remote computers for the purpose of retrieving information useful for testing Internet connection. In general a traceroute tracks the path that a packet takes from your computer to a destination address. A traceroute also shows how many times your packets are being rebroadcast by other servers until it gets to the final destination.

# How to Use

The code can be run in the following ways:

python traceroute.py -h will give all the options that can be used.    
python traceroute.py www.google.com will give the traceroute for www.google.com    
python traceroute.py www.google.com -m 5 will set the maximum hop limit to 5 and will exit if it is not able to find a route within that hp limit (default hop is 30)    
python traceroute.py www.google.com -p 9000 will set the port to be used (default port is 33434)    
