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





