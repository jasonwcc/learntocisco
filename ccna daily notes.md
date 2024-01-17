Text
- ASCII (windows/unix/linux)
- EBCDIC (mainframe)

Transport 
- UDP / TCP

Network
- IP (logical address)
  -- can change
  -- car number plate
  -- routable
- Layer 3

Data Link
- MAC (physical address)
  -- cannot change
  -- engine chassis number
  -- not routable
- Layer 2

DNS
- facebook.com --> 102.1.11.2


Pls
Do
Not
Trust
Sales
Person
Advice

Ethernet frame


90 day
login without starting lab

start lab - 60 hours


switch (L2)
SWX > enable
SWX # di
SWX # conf t
SWX (config) # hostname jasonwong
SWX (config) #

router (L3)
RX > enable
RX # conf t
SX (config) # interface fa0/1
RX (config-if) # ip address 1.1.1.1 255.255.255.0
enable
exit



github.com/jasonwcc/learntocisco


LAN 
- network infra managed/control by org admin
vs 
WAN
- subscribe to telco / SP
- geo-location


switches
- L1&L2
- understand VLAN, STP, VTP, MAC
- first packet - flooding
vs
bridges
- L1&L2
- no longer R&D
vs
hub
- L1
- half duplex


straight-thru (different type)
PC -- SW
PC -- Hub

cross-over (same type)
PC -- PC
SW -- SW
RO -- RO
Hub -- SW
RO -- PC (OS)

roll-over (console)


Standard frame - mtu : 1500 bytes
Jumbo frame - mtu : 9000 bytes

IPv4
- unicast,  multicast, broadcast (separate by VLAN)
- 32 bits (0.0.0.0 -- 255.255.255.255)
- 4 billion

IPv6
- unicast,  multicast, anycast (service based on nearest device)
- 128 bits 3.4 (36 0's)

EUI-64

IETF

192.168.0.1 = 32 bits
255 --> 1111 1111

Switch
MAC table
- MAC ==> Port

PC
- ethernet frame (IP-SA, IP-DA, MAC-SA, MAC-DA
- ARP

flooding (MAC) vs broadcasting (IPv4)





Decimal ( base 10)
0 - 9
10 -100
101 - 1000

Binary ( base 2)
0,1

Octal ( base 8 )
0 - 7
syslog 

Hexadecimal ( base 16 )
0 - 9, a - f


9 - 1001


binary <--> decimal
hexa <--> decimal/binary

125 
decimal --> binary --> hexadecimal

9 A --> 1001 1010
128+16+10 = 

0.0.0.0 - 0.255.255.255 --16 777 xxx
Class A  1.0.0.1 - 126.255.255.254/8 (255.0.0.0)
127.x.x.x - loopback (testing, demo, poc)
class B
128.x.x.x - 191.255.255.254/16 (255.255.0.0)
Class C
192.x.x.x - 223.255.255.254/24 (255.255.255.0)
class D
224 - 239
Class E
240 - 255


netmask /21 = 255.255.248.0

network address translation (NAT)
ifconfig
ip add
nmcli

netstat -r -n -

Administrative distance
- trust value (OSPF, RIP, EIGRP, BGP)

Metrics
- decide best route

dynamic route
- use routing protocol (OSPF, RIP, EIGRP, BGP) - automatically

static route
- admin add route manually


Metrics
- BW (OSPF/EIGRP)
- reliability
- MTU
- load
- latency (EIGRP)

RIP
- hop count


conf t
int e0/1
  no ip add 172.16.0.1 255.255.0.0
int e0/0
  ip add 172.16.100.2 255.255.240.0
error: overlap

CDP

LLDP

show cdp entry SwitchA

Router A
en
conf t
  no cdp run
  int fa0/0
    cdp enable





ARP 
- ARP request dari sender ke receiver
- ARP reply dari receiver back to sender
  - ip:mac

Switch (show mac address)
- based on ARP reply from printer
- cache port:mac address

Router (show ip arp/ show ipv6 nei) / PC (arp -a)
- ARP
  - ip:mac



Q1 PC1 send UDP PC2, what is the source MAC address of the frame exiting R1?
A. Mac E0/0 of PC1
B. Mac E0/2 of R1
C. Mac E0/2 of R2
D. Mac E0/1 of R3

Q2 PC1 send UDP PC2, what is the source MAC address of the frame entering R1?
A. Mac E0/0 of PC1
B. Mac E0/2 of R1
C. Mac E0/0 of R1
D. Mac E0/1 of R3

Q3 PC1 send UDP PC2, what is the source IP address of the frame exiting R1?
A. 10.10.1.10
B. 10.10.1.1
C. 10.10.1.4
D. 10.1.1.10
E. 10.10.2.20

Q4 PC1 send UDP PC2, what is the destination IP address of the frame exiting R1?
A. 10.10.1.10
B. 10.10.1.1
C. 10.10.1.4
D. 10.10.1.10
E. 10.10.2.20



Q4 PC1 send TCP PC2, what is the source IP address of the returning frame exiting R1?


..!!!
!!!!!
arp 
.!.!.!
!.!.!.

ECMP
- EIGRP
- OSPF
- static


local


Internet
IPv4
- 32 bits
- 4 billions
- a.b.c.d
> 
IPv6
- 128 bits
- 3.4 36 0's
- hexadecimal

1.x.x.x - 223.x.x.x
224.x.x.x multicast
- 239.x.x.x
240 - 255.x.x.x reserved for future

- 10.x.x.x
- 172.16.x.x - 172.31.x.x
- 192.168.x.x



NAT
- translate private ip into public
- 192.168.0.100 ==> 111.1.11.1:11111
- 192.168.0.101 ==> 111.1.11.1:11112



en
conf t
int fa0/1
   ipv6 address 2002::0 eui-64
   ipv6 address 2001::1/64
   ip add 10.0.0.1 255.255.255.0
   ip add 20.0.0.1 255.255.255.0

G

show ipv6 int brief


DB1 1001::1
DB2 1001::1
DB3 1001::1


Load Balancing




















  










nssa
- ospf
- not so stubby area


Admin add 2 vlans, how many broadcast domains?
A. 2
B. 3
C. 1
D. 4


vlan 1 -- 192.168.1.0/24
vlan 2 -- 192.168.2.0/24
vlan 20 -- 192.168.20.0/24



4095
- VM
- container

VXLAN
- million

dynamic trunking protocol (dtp)
- negotiate : 
- configure : trunk vs access

int g0/0

int g0/0.10
  ip add
  no shut































