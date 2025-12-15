```
https://sms.trainocate.com/manage-attendance?ClassId=12210

All shortcut keys
ctrl+z end
ctrl+c cancel/break
ctrl+a cursor at beginning of line
ctrl+e cursor at end of line
ctrl+u erase everything to the left
ctrl+k erase everything to the right
ctrl+w erase last word
cltr+shift+6 . break while command is looping
cltr+^ .

Hub
- L1
- do not understand MAC
vs
Bridge
- L2
- understand MAC in frame
vs
Switch
- L2
- understand MAC in frame

TX+
TX-
RX+
RX-

Straight thru
- Server/PC to SW/Hub
- Router to SW/Hub

Cross-Over
- PC/Server to PC/Server
- Hub to hub
- sw to sw
- ro to ro
- SW to hub
- PC/Server to Router

IETF (under IEEE)
- creates OUI and assign to vendor

Vendor
- creates the EUI

Reason why configure IP on switch:
1. enable remote management 
2. Multi-level switch (3000 series model), enable routing.


show run
- recent data in RAM
show start
- saved data in NVRAM

copy run start = write memory
- save data from RAM into NVRAM

copy start run
- restore back to last saved state/data



9am int fa0/1
    shutdown
copy run start
...
...
9:15am int fa0/1 
    no shut
copy start run
   shutodwn


0.0.0.0 - 255.255.255.255

2^32 = 4 billion...


IP  = Internet Protocol

numbering
decimal (base 10) 0-9
binary (base 2) 0 1
hexadecimal (base 16) 0-9, a-f
octal (base 8) 0-7

150 --> 1001 | 0110 -->  96

0 - 9 
10 = a
11 = b
..



Given 192.168.1.100/18
calculate and find out
- network ID
- first usable IP
- last usable IP
- broadcast IP
- netmask 
- number of clients (2^c-2)
- number of networks

192.168.100.100/24
nnnn nnnn.nnnn nnnn.nnnn nnnn.cccc cccc
8n.8n.8n.8c

192.168.100.100/8
nnnn nnnn.cccc cccc.cccc cccc.cccc cccc
8n.8c.8c.8c

192.168.100.100/21n
8n.8n.5n 3c.8c

192.168.100.100/30n
8n.8n.8n.7n 1c
255.255.255.252

number of client
2^1-2 = 0




















if all n is 1 this is netmask
if all c is 1 this is broadcast ip
if all c is 0 this is network ID




1000 0000
1100 0000
1110 0000
1111 1111











































