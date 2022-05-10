```
Material Access
URL : https://learningspace.cisco.com/
Sign up : personal email
Redeem : xxxxxxxxxxxxxx (email dari cisco / trainocate)
Offline read: Download and install Cisco eReader

Lab Access
Access to Cisco Learning Labs is via the Cisco Learning Labs Portal:
URL: https://cll-ng.cisco.com/users/pblogin
(60H 90D) Pods.

Course Start and End Dates: 2022-05-09 - 2022-05-13

Access to Cisco Learning Labs is via the Cisco Learning Labs Portal at the following URL:
https://cll-ng.cisco.com/users/pblogin


Students Credentials

Student:  SHAFIQ 
Username: 2022051620072
Password: YUeUhb2Q

Student: AL-AFSYIN 
Username: 2022051620073
Password: qntmY3US

Student: AHMAD SYUKRI 
Username: 2022051620074
Password: 9VgM37f5

Student: ISMAH ZAKIRAH
Username: 2022051620075
Password: uM2RQ326

Student: DAYANG JASMINA 
Username: 2022051620076
Password: bT4Tp7Cy

Student: HAIREE IZZAM 
Username: 2022051620077
Password: CMLnRkv2

Student: AMIR 
Username: 2022051620078
Password: joPN3Rpi

Student: MOHAMMAD FAHMI  
Username: 2022051620079
Password: jWJ75gvk

Student: ABDUL HAKAM 
Username: 2022051620080
Password: 8aHLu7bi

Student: MOHAMAD AZREEN 
Username: 2022051620081
Password: Jg8Tm3xy

Student: MUHAMMAD NAQIUDDIN 
Username: 2022051620082
Password: vN2yEP9W

Student: MUHAMMAD SHAFIK 
Username: 2022051620083
Password: 4MF7tfSw

Student: RAZIF 
Username: 2022051620084
Password: u4AMwD6u

Student: YADIY RAHIMI 
Username: 2022051620085
Password: rTi39ABT

Token: angio


6 months
- 2 exam vouchers
- 3rd exam - MYR 1000+
- examtopics.com (leak questions)
- Q1 --> Q2 --> Q10

Serial - ISP
- Frame Relay
- ATM
- ISDN


Spoke and Hub

VLAN
1 A 
2 B & C
3 Server
4
5
6
-4095

Classless Inter Domain Routing


Interior Gateway Protocl 
- OSPF, EIGRP, RIP
Exterior Gateway Protocl
- BGP

L1 - Hub / Repeater 
L2 
- MAC Address used by switches / bridges / AP
- VLAN, STP, RSTP, MSTP, VTP, EtherChannel / LACP
L3 
- IP Address used by Routers /  PCs / Firewall ...
- ICMP, IGMP, DHCP, OSPF, EIGRP, RIPv1 RIPv2
L4
- TCP / UDP 
- discuss in Module 8

L7 telnet, ssh, smtp, snmp, rlogin, rsh, db, email, http

Media Access Control Address / Hardware addressing
- hardcoded to LANIC
- created by IEEE 
- 00-50-56-C0-00-01
- 00:50:56:C0:00:01
- hexadecimal value
- 6 octets x 8bits = 48 bits
vs
IP Address / software address / logical addressing
- can change from subnet to subnet
windows c:> ipconfig /all
linux # ifconfig
- decimal value (0-255)
- IPv4: 4 octets = 32 bits
- IPv6: 8 octets = 128 bits
- 192.168.219.1

Why IP + MAC ?
Why CAR number plate(IP Address) + Engine chassis number (MAC address)?
- JPJ

w
who
last
uptime

ASCII - Text
- MACintosh 

EBCDIC - Text
- Mainframe --> PC 

Binary --> Text

Please Do Not Trust Sales Person Advice
Pak Dah Naik Tek Si Pergi AlorSetar


Standard Frame 
- Max Transmission Unit 1500 bytes -- > 1494

Jumbo Frame (FCoE) -- > SAN
- MTU : 9000 bytes

LAN
- org. admin responsible
- close distance
WAN
- subscribe to SP / telco
- geographic region

PAN

MAN

SAN
- block storage
- FC / iSCSI(ethernet) / FCoE / NVMeOF

NAS
- NFS / CIFS

Hub
- L1
- Half Duplex
- Flooding send out frame to all ports except original port
Bridge
- L2 
- understand
- less developed
Switch
- L2
- Half / Full Duplex 
- understand
- vendor R&D

TPLink
- managed switch
- 240 

Collision Domain

Broadcast Domain

Switch 
- by default it operate as switch at L2
- without configuration
- Optional, configure IP on switch vlan 1 interface
  - default gateway
  - remote management

1GBe
10GBe
25GBe
40GBe
-> 
100 GBe
600 GBe

flooding vs broadcast
IPv4
- unicast
- multicast
- broadcast (Netbios, DHCP, arp, virus)
  ---> break into VLAN / segment

ARP
- address resolution protocol
- resolved IP into MAC
- ping IP / telnet IP 

RARP 
- Reverse ARP
- resolved MAC into IP
- Installation / Boot Server 
- RedHat KickStart / Solaris Jumpstart
  - PXE-boot NIC

IPv6
- unicast
- multicast
- anycast


Cross
- Same type of device
- exception1 PC <--> Router
- exception2 Switch <--> Hub

- MDI -- MDI-X

Netbios
- File & Print
- Streaming
- advertise

0    0 <-- hexa
0000 0000  --> WAN
0    2

0000 0010  --> LANIC

Physical, Logical (configuration)
UP, UP ==> Superb Good
DOWN, DOWN ==> Physical connection / cable
UP, DOWN (secured-err) ==> Configuration is bad
ADMIN DOWN, DOWN ==> manually disabled by admin

Metrics can used by routing protocol 
- control routing process
- DLY = DELAY

OSPF
- BW
EIGRP
- BW + DELAY
RIP
- hop count

show run
- latest config (ram - MB)
show start 
- last saved configuration (nvram - kb)

copy run start 
== wr

copy start run

flash (MB)
- IOS

line vty 0 5
   password cisco
   
   login 

crypto
ip ssh
ip domain

Discovery lab 1 - 3
Fastlab 1: Implement the Initial Switch Configuration

ipv4
32 bits
2^32 = 4 billion
IP range 0.0.0.0 -> 255.255.255.255
IP Address : 192.168.0.1
Netmask    : 255.255.0.0

Classfull design
A 255.0.0.0     0.0.0.0 - 127.255.255.255
B 255.255.0.0   128.x.x.x - 191.x.x.x
C 255.255.255.0 192.0.0.0 - 223.255.255.255
D               224.0.0.0 - 239.255.255.255
E reserved for future use 240.x.x.x - 255.255.255.255

2.7 billion usable over Public WAN

Classless design
255.128.0.0
255.255.255.252

Calculate Network ID / Broadcast IP
Binary <--convert-->Decimal
AND
x = 0101
y = 0011
AND=0001 --> 

Decimal     base 10 (0-9)
Binary      base 2 (0,1)
Octal       base 8 (0-7)
Hexadecimal base 16 (0-9,a-f)

Decimal <--> Binary
255       --> 1111 1111

Decimal <-- Binary <-- Hexadecimal (IPv6)
	   1111 1111	ff
           
0-9
10 = a
11 = b
12 = c
13 = d
14 = e
15 = f

RFC1918
- these private range can never routed in the internet
10.x.x.x - Private
192.168.x.y - Private
172.16.x.y - Private
- 172.31.x.y - 

NAT - network translation table
172.15.6.1

VLSM 
- differnt subnet mask
- what formula? 
3 rules
- minimize IP wastage
- No overlapping
- Start from direction 
  - small / big

HQ - 172.16.x.x/16
JB - 10 clients
PN - 20 clients
PJ - 3 clients
answer: refer to excel file

```
TCP Connection-Oriented
PcA --> Frame1 (100b)  ---> PcB
TCP : Seq number : 100 --> 
     <-- Ack number : 101
PcA --> Frame1 (90b)  ---> PcB
TCP : Seq number : 190 --> 
     <-- Ack number : 191
.... 421.......

applications / services
0 - 65535 (16 bits)
0 - 1023 well known port
80
22
23
25
69
443
110
111 rpc
1024 - 49151 registered port (vendor / OS specific)
49152 - 65535 arbitrary / random port

DHCP 
-  release IP
- 
DNS
- resolve FQDN into IP
- Fully qualified domain name
- mail.yahoo.com --> 22.22.22.11

Discovery 4 Lab

Directly Connected Route

show ip route
netstat -rn


RAM (bootup)
- Cisco IOS + 
- Running configuration
Flash (mb)
- Cisco IOS (permanent)
NVRAM (kb)
- startup configuration

Router
if received several routing information from 
different routing protocol (OSPF, EIGRP, RIP)
then decide best route from AD
if received several routing information from 
same routing protocol
then decide best route from metric


EIGRP
= Bandwitdh + Delay
= propietory
OSPF
= Bandwitdh
RIP
= Hop Count

HDLC
PPP
FRAME-RELAY
ATM


192.168.1.0/24
- via 10.10.10.1
192.168.2.0/28
- via 10.10.10.2
192.168.1.0/20
- via 10.10.10.3

sh cdp entry SwitchA
- ip


cdp
lldp

Until
- Discovery Lab 6
- FASTLab 2






 



































```
