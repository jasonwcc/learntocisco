MCQ
- eliminate wrong answer

Performance-based question
copy run start
or
wr

click and drag

wa.me/0122736143
https://github.com/jasonwcc/learntocisco

Download and install exam formatter
convert pdf into rtf

vce 
import from rtf 

default route
- 0.0.0.0/0
- 

floating static route 
- backup route
- 

Routing Table [ad/metric]
B BGP [20/x]
C Directly connected [0/0]
O OSPF [110/x]
D EIGRP [90/x]
R RIP [120/x]
S Static Route [1/x]
S* Default Static route [1/x] (last resort)

[administrative distance/metric]

Best Route selection
- multiple protocol
  - choose from smallest AD
- same protocol
  - choose from smallest metric
- closest and longest prefix 
- 

10.10.13.0-127/25
10.10.13.128-143/28
10.10.13.144-159/28
10.10.13.160-167/29
10.10.13.208-215/29

8c/1111 1111 = 255
7c/0111 1111 = 127
6c/0011 1111 = 63
5c/0001 1111 = 31 
4c/0000 1111 = 15
3c/0000 0111 = 7
2c/0000 0011 = 3

FTP
- TCP/20 and TCP/21
- send data plain text
- has separate control and data connections
- requires authentication / username+password

TFTP
- UDP/69
- backup Cisco IOS or configuration/nvram to TFTP server
- upgrade Cisco IOS
- convenient : no need authentication / username+password

Interface - slow / poor performance
- lots of CRC/frame 	: physical / hw error
- lots of collision 	: duplex mismatch
- lots of runts		  : small frame (<64 bytes)
- lots of giants		: large frame (>mtu)
- late collision		: occurs in first 64 bytes. 


172.28.228.144/18n (left)
8n.8n.2n 6c.8c

nn cccccc
11 000000  192
11 111111  255

172.288.228.144/21n
8n.8n.5n 3c.8c

nnnn nccc
1110 0000 224.1
1110 0111 231.254

172.28.228.144/23n
8n.8n.7n 1c.8c

nnnn nnnc
1100 0100 228.1
1100 0101 229.254

172.28.228.144/25
8n .8n.8n .1n 7c

1ccc cccc
1000 0000 128
1111 1111 254


1000 0000 128 1n
1100 0000 192 2n
1110 0000 224 3n
1111 0000 240 4n
1111 1000 248 5n
1111 1100 252 6n 
1111 1110 254 7n

TCP
- reliable, statefull, connection-oriented (three way handshake)
- use sequential, acknowledge
- has control bits 
- can use checksum
- ftp, smtp, ssh, www, database, pop3, dns

UDP
- unreliable, stateless, connection-less
- can use checksum
- fast, less overhead
- snmp, tftp, voice, audio, dns, NTP


ipv6 add autoconfig
- FE80::<64 bits comes from mac>
- link local (not routable to internet)
- MAC 48-bits -- convert --> EUI-64
- 
IPv6
- link local/stateless address autoconfiguration : FE80::eui-64/10
  - not routable to anywhere
- unique/site local : FCxx / FDxx (recognised by IETF)
  - routable inside LAN
  - not routable to internet
- multicast : FFXX::
- global unicast : 2xxx/3xxx
- Anycast:
  assign same IPv6 address to multiple non-host devices  (servers/routers/load balancers)

ifconfig
netstat -rn

Q14
8c/1111 1111 = 255
7c/0111 1111 = 127
6c/0011 1111 = 63
5c/0001 1111 = 31 
4c/0000 1111 = 15
3c/0000 0111 = 7
2c/0000 0011 = 3

3th octet
128.0/17
192.0/18
252.0/22

4th octet
1000 0000 128 /25
1100 0000 192 /26
1110 0000 224 /27
1111 0000 240 /28
1111 1000 248 /29
1111 1100 252 /30 
1111 1110 254 

/30
8n.8n.8n.6n 2c

6n
nn nn nn cc
00 00 00 01 1
00 00 00 10 2

8n.8n.8n.5n 3c
192.168.1.1

A 1.x.x.x - 126.x.x.x (10.x.x.x:private ip) 
B 128.x.x.x - 191.x.x.x (172.16.x.x-172.31.x.x:private ip)
C 192.x.x.x - 223.x.x.x (192.168.x.x:private)
D 224.x.x.x-239.x.x.x multicast

nnnn cccc
1000 1111

15+128 = 143

Controller-Based Networking
- centralized configuraiton, monitoring, management
- leverage controllers to handle network management and configurations
- automation of devices (networks) and services
- like Cisco DNA Center


WIFI
5GHz many non-overlapping / many devices
2.4GHz 3 non-overlapping 
- channel : 1, 6, 11

802.11AC

TCP
- reliable, statefull, connection-oriented (three way handshake)
- use sequential, acknowledge
- has control bits 
- can use checksum
- ftp, smtp, ssh, www, mysql , postgresql, ms sql, pop3, dns

UDP
- unreliable, stateless, connection-less
- can use checksum
- fast, less overhead
- snmp, tftp, voice, audio, dns, NTP, DHCP

Single mode 
- long distance
- single application
- use/implement at backbone
- core very small (9 um)
vs Multi mode
- short distance
- multiple application (data+audio+video)
- within on-prem DC

Collapsed-Core (two-tier)
- combined distribution and core layer devices into one
- reduce cost and complexity design
- used by small to medium size companies


00:00:a2:ff:fe:dc:22:33
fe80::20:00:a2:ff:fe:dc:22:33/10

0000 0010 0000 0000

2^c-2 = number of clients/users
2^c-2 = 22
2^c = 24
c = 5
n = 27
/27 = 255.255.255.224

nnn ccccc
001 10000
001 00000 

Q37
8*40 = 320
2^c-2 = 320
c=9
32-9=23
23n 
8n.8n.7n 1c.8c

1000 0000 128 1n
1100 0000 192 2n
1110 0000 224 3n
1111 0000 240 4n
1111 1000 248 5n
1111 1100 252 6n 
1111 1110 254 7n


WPA
- TKIP/MIC encryption

WPA-2
- only 8-63 ASCII characters or 64 HEXADECIMAL characters
- 128 bits
- use pre-shared key

WPA-3
- AES : for encryption 
- SAE : Simultaneous Authentication of Equals
  - is resistant to dictionary and brute force attacks
- relies on Perfect Forward Secrecy 

Q49
DHCP
- DORA Discover Offer Request and Acknowledge
  discover from client broadcast to whole network, look for DHCP server
  DHCP server respond with Offer back to client
  Based on offer, Client request direct from the DHCP server
  Finally Server acknowledge the request by client
- when conflict - ip is removed
- Relay Agent 
  To see relay agent / helper address # show ip interface
- Lease : list of ip assigned to clients
  # show ip dhcp bindings
- Pool :  list of ip available 
  # show ip dhcp pool
- If router want to obtain IP on its interface
  # ip address dhcp
  
Q51 
MAC 
- not routable to another network (internet)
- NIC automatically assign with MAC (physical)
- first 24bits OUI : last 24 client bits 
vs IP
- routable
- assign / DHCP / static
- network portion + client portion

Hot Standby Redundancy Protocol
- HSRP
- VRRP
- GLBP



ip route <network-ID> <netmsak> <next hop> [metric]


ip route  0.0.0.0 0.0.0.0 192.168.2.3
- default route / last resort
- 

Q60 
A-10
B-11
C-12
D-13
F    | D 
1111   1101

IPv4
- Private IPv4 address (RFC 1918)
  : conserve public address ,secured
  : always private, cannot route to internet
  : unless configured with NAT to be translate into public
  : implement within LAN

Software Defined Networking (SDN)
1. Management plane
    - business criteria / conditions
    - human/administrator/manager
2. Control plane
    - Routing protocol / configuration / decision
    - NAT configuration
    - ACL configuration
    - VLAN configuration
3. Data plane
    - switching using MAC address table
    - forward traffic according to routing from control plane
    - Vlan tagging / trunking
    - encrypt (VPN) / confidentiality configuration
    - drop frame (if denied by ACL)
    - Change source IP (when configured with NAT)

lunch + ur self prep 
- continue at 2pm
- 

2001:0db8::700:3:400F:572B


URL https://pc1.trainocate.com/aseee

c60142 fffe 0f0007

DNS
- resolve FQDN into IP
- 

Q109
R7 fa1/0
10.88.31.64/26n 6c
8n.8n.8n.2n 6c
nn cccccc
01 111111 63
64+63 = 10.88.31.126 255.255.255.192


R8 fa0/0
10.19.63.80/28n (4c = 15)
10.19.63.94 255.255.255.240


SSIDs
- max 32 alphanumeric case-sensitive characters
- can optionally hidden (non-broadcast)

  
Q129
2^8 = 254
2^9c = 512

9c = 23n
255.255.254.0
10.7.54.0

2^c-2 = 30
2^5-2 = 30

3n = 255.255.255.224

97
nnn ccccc
011 11110
000 11111

2^8c = 225
2^10c = 923


R7 fa1/0  22n 255.255.252.0
R8 fa0/0  24n 255.255.255.0

Q163
25n
8n.8n.8n.1n 7c
cccc cccc
1000 0000
128


2^n = 31
5n
ad-hoc / infra

blocking -> listening -> learning - > forwarding
blocking -> forwarding

QOS
- Low-Latency Queue (LLQ) : suited for voice and video
- Weighted Random Early Detection (WRED)
  : when queue is full then start dropping low priority packet
- Policing : implement by ISP 
  : limit both incoming and outgoing flow
  : Discards or re-marks packets
- Traffic Shaping 
	: limit bandwitdh that an outgoing flow can use
     : reschedules packets by delaying or queueing when traffic exceed limits
- Precision Queue (PQ) : congestion management : suited for voice 
- Class-Based Weighted Fair Queueing (CBWFQ) : congestion management
- 
Spanning Tree (PVST+ or Rapid PVST+)
- one spanning tree instance for each VLAN
- Elect Root bridge
  1. Lowest priority number (0 - 61440)
  2. Lowest MAC address 

CDP
- can used to discover only cisco neigbor devices
- enabled globally
- question says enable on particular interface

en
conf t
no cdp run
int g0/1
   cdp enable
vs
LLDP
- can used to discover multi-vendor neighbor devices
- not enabled globally
- question says enable on particular interface
en
conf t
int g0/1
   lldp receive/transmit

  
#175 find out 

Q183 answer is A

Wireless controller
- service port : administration/ management
- virtual port : support mobility management
- dynamic port : for wireless client communication
- control/manage all AP

access point (AP)
- user's devices will connect

EtherChannel / LACP /PAGP
1. LACP (universal)
   mode : active/passive
2. PAGP (cisco)
   mode : auto/desirable
3. Static
   mode : on
5.

