---
title: Basic Pentesting Box 
date: "2020-07-22"
---
#Basic Pentesting

##setup 
download openvpn then use your own try hack me openvn cofiguration file and connect to it 

##delopy
click on deploy the machine
now get the ip addess
`
nmap -sV -sC -v ip address
`
we go to know their is an port 80 open
we head over to our browser enter the machines ip address

back to the terminal
`
dirb http://ipaddres
`
first question solved
###hidden directory :- /development

now have to find username and password
how to do that???

do emumeration
`
enum4linux -u ipaddress
`
##users found
jay & kay

now we know a username we can do brutefource
`
hydra -l jay -P /root/rockyou.txt ssh://ipaddress
`
passowrd found armando

now we could do privilage escalation
`
scp linpe.sh ipaddress /root
`
found a ssh key of the kay user

now use john the ripper to find the ssh key phrase

ssh key phrase is beeswax

now login to the kay user
open the pass.bak file

and our last flag is
heresa************************************************$$
      
