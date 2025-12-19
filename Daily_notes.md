```
https://sms.trainocate.com/manage-attendance?ClassId=12210


IPv4
- 32 bits
- 4 billion
- 0.0.0.0 - 255.255.255.255
vs
IPv6
- 128 bits
- 3.4 TTT
- 0000x8 - FFFFx8

2 c
0010 1110

a 10
b 11
c 12
d 13
e 14







Find 		- 192.168.1.9 255.255.255.240
networkID	- 192.168.1.0
first usable	- 192.168.1.1
last usable	- 192.168.1.14
broadcast 	- 192.168.1.15

Next usable
networkID	- 192.168.1.16
first usable	- 192.168.1.17
last usable	- 192.168.1.30
broadcast 	- 192.168.1.31

floating route

access mode
- belong one vlan
- connect to PC/Server/router
vs 
trunk mode
- send multiple vlan
- connect to another switch / interVLAN router

2^12 =4096 (0,1001-1104)

EGP
- Border Gateway Protocol.
- implemented by ISP , CSP.

Distance Vector
- RIP & EIGRP
- hop count
- care about routing table (best route)

Link-State
- OPSF & IS-IS
- bandwidth / delay / mtu / reliability / Tx and RX load
- care about
  - neighboring table (neighbors)
  - topology table / Link State DataBase (All routes)
  - routing table (best route)
- heavy resource consumption (cpu/memory)





Course Start Date: 2025-12-15 01:00:00 (UTC)
Course End Date: 2025-12-19 13:00:00 (UTC)
 
Lab :	https://htdlab.cisco.com

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

https://github.com/jasonwcc/learntocisco


1000 0000
1100 0000
1110 0000
1111 1111







Example 1:
PC1 - 192.168.100.1/26 (255.255.255.192)
PC2 - 192.168.100.2/26 (255.255.255.192)

Q. Are they in same subnet / network?
A. Yes

Step 1. Convert all IP and Netmask into binary
192.168.100.1 --> 1100 0000.1010 1000.0110 0100.0000 0001
255.255.255.192-> 1111 1111.1111 1111.1111 1111.1100 0000
ANDing         -> 1100 0000.1010 1000.0110 0100.0000 0000 
Network ID    --> 192      .168      .100      .0

192.168.100.2 --> 1100 0000.1010 1000.0110 0100.0000 0010
255.255.255.192-> 1111 1111.1111 1111.1111 1111.1100 0000
ANDing         -> 1100 0000.1010 1000.0110 0100.0000 0000
Network ID    --> 192      .168      .100      .0

Example 2:
PC1 - 192.168.100.100/29 (255.255.255.248)
8n.8n.8n.5n 3c

PC2 - 192.168.100.114/29 (255.255.255.248)

Q. Are they in same subnet / network?

100	-> 0110 0100
248	-> 1111 1000
AND	-> 0110 0000
NID  	-> 192.168.100.96

133	-> 1000 0101
248	-> 1111 1000
AND	-> 1000 0000
NID	-> 192.168.100.128

Find following?
NID
Broad IP













8n.8n.2n 6c.8c
228 --> 1110 0100
	nncc cccc
        1100 0000 = 192

8n.8n.5n 3c.8c
	nnnn nccc
228 --> 1110 0100
        1110 0000 = 224

nnnn nnnc
1110 0100 = 172.28.228.1

Router (NAT)

https://github.com/jasonwcc/learntocisco
\

0.0.0.0 - 0.255.255.255

2^24-2 = 16777...

If multiple route info comes,
then ur router choose best info
1. If use same routing protocol then we use metric
2. If use different routing protocol then we use AD
3. IF same routing and same metric then we use longest prefix

If disable CDP globally
en
conf t
  no cdp run
  end
wr

If disable CDP per interface
en
conf t
  int range fa0/1-10
    no cdp enable
  int fa0/5
    no cdp enable
  end
wr

Source MAC
Destination MAC
Source IP 
Destination IP



HostA send TCP data to Host B. On returning traffic, what is the destination MAC address inbound router?
A. 0222:2222
B. 0333:2222
C. 0333:1111
D. 0222:1111
Answer: 





reference-bw / actual-bw

100M / 10M = 10

100M / 100M = 1

100M / 1000M = 0.1

en
conf t
  router ospf 1
    network 192.168.100.16 0.0.0.

  int fa0/0
    ip add 192.168.100.16 255.255.255.240

  int fa0/1
    ip add 192.168.100.32 255.255.255.240

  int fa0/1
    ip add 192.168.100.48 255.255.255.240

  int fa0/1
    ip add 192.168.100.64 255.255.255.240

  int fa0/1
    ip add 192.168.100.80 255.255.255.240


  end
wr

Election to select DR (designated router)
1. router-id
2. highest IP in any loopback interface
3. highest IP in any active physical interface


Switch  - STP
1. Elected Switch
   - Priority (0-65535)
   - lowest MAC address
2. Port Role - Designated / Root 
3. Port status - FWD / BLK


802.1D
- 1x spanning tree for all VLANs (4095)


PVST+ 
- Per VLAN spanning tree protocol
- 1x spanning tree for each vlan  



en
conf t
  vlan 20
  vlan 300
  int range fa0/20-24
     switchport mode trunk
end
wr

old time
0-65535 (16 bits)

new time

!switch3
en
conf t
spanning-tree vlan 1-300 root primary = priority 28672

!switch6
conf t
spanning-tree vlan 20 priority 0


BPDU Guard
- if received bpdu , shutdown port immediately forever
BPDU filter
- if received bpdu , shutdown port temporary
Loop Guard
- if multiple ports / switch restart at same time,  shutdown ports immediately forever
Root Guard
- if received bpdu and only if it wants to become root, shutdown port 
forever permanently


Netmask
- identify network / host
- must be continous/contigous
vs
Wildcard mask
- used in OSPF / ACL-->NAT / EIGRP 
- non-contigous
- select certain network range from existing subnet

192.168.100.64/26 (255.255.255.192)
networkID : 192.168.100.64
first usable: 192.168.100.65
last usable : 192.168.100.126
broadcast   : 192.168.100.127

scenario 1 : block the whole subnet
access list 1 deny 192.168.100.64 0.0.0.63

scenario 2 : block/deny only 192.168.100.80 - 192.168.100.95
access list 2 deny 192.168.100.80 0.0.0.15 

Step Convert IPs into Binaries
80 --> 0101 0000
95 --> 0101 1111

Step find network ID by looking at matching bits
0101 cccc 
0101 0000 --> 192.168.100.80


Step find wild-cardmask by convert not matching bits convert into 1's 
0000 1111 -> 0.0.0.15




scenario 3 : block/deny only 192.168.100.64 - 192.168.100.95
access list 2 deny <network ID?> <wild-cardmask?>
access list 3 deny 192.168.100.64 0.0.0.31

Step Convert IPs into Binaries
64 --> 0100 0000
95 --> 0101 1111
       nnnc cccc

Step find network ID by looking at matching bits
nnnc cccc
0100 0000 --> 192.168.100.64

Step find wild-cardmask by convert not matching bits convert into 1's 
nnnc cccc
0001 1111 --> 0.0.0.31


scenario 4 : permit only 192.168.100.48 - 192.168.100.55
access list 4 permit <network ID?> <wild-cardmask?>
access list 4 permit 192.168.100.48 0.0.7.0


Step Convert IPs into Binaries
48 --> 0011 0000
55 --> 0011 0111
       nnnn nccc

Step find network ID by looking at matching bits
       nnnn nccc
       0011 0000 --> 192.168.100.48

Step find wild-cardmask by convert not matching bits convert into 1's 
       nnnn nccc
       0000 0111 --> 0.0.0.7


PC1 193.168.110.64

access list 5 permit 192.168.100.48 0.0.0.0
or
access list 4 permit host 192.168.100.48 

access list 4 permit any = 0.0.0.0 255.255.255.255
```


