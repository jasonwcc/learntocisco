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



























  









































