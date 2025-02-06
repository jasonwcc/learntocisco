```
192.100.100.100/18
192.100.100.0

routing / IP

reason : VLAN
Server :  10.0.0.0/8
A :  20.0.0.0/8

MAC  (chassis engine number)
- fixed/cant change
- physical / tie to NIC
- non-routable
vs
IP (car number plate)
- change/assign by DHCP
- logical
- routable

/ipconfig/traceroute/ping/netstat
- ip application

Cisco router/switch
- use ARP to resolve IP into MAC
- use RARP to resolve MAC into IP
- mac 
- ip

write memory = copy run startup-configuration = File > Save
write erase = delete all configuration (start
copy start run
- major/corruption

wr erase
reload

copy start tftp://192.168.0.100

start = Non Volatile RAM = DISK
run = DRAM (volatile)


ccna
- MCQ (ABCD) POE
- click & drag
- simulation / performance-based 
total (55-60q)

- MCQ (ABCD) POE
- click & drag
- (q3-5) simulation / performance-based 

cisco Switch
- by default, all physical ports are up (no shutdown)
- by default, vlan 1 port/interface is down

cisco routers
- by default, all physical ports are down


fastethernet0/0
gigaethernet0/0

serial0/0/0
serial1/1/0

f1/1/0
f1/1/1
f1/1/2
f1/1/3

IPV4 Classful
unicast A 1.x.x.x - 127.x.x.x/8 (255.0.0.0)
unicast B 128.x.x.x - 191.x.x.x/16
unicast C 192.x.x.x - 223.x.x.x/24
multicast D 224.x.x.x - 239.x.x.x
E reserved for future 240.x.x.x - 255.x.x.x.

IPV6
FFxx

classless

NetBIOS

IPv6
unicast
multicast
anycast

DHCPv4
- broadcast
- router configured as DHCP relay agent

link-local
- cisco use SLAAC 
- FE80
- 

UEFI


can be used as metrics for routing protocol
- EIGRP
  - BW + DLY
- OSPF 
  - BW
- RIP
  - hop count
- IS-IS
- BGP

IP
- 4 octets
- octets 8bits
- 32 bits
- 2^32 = 4 billion
- classful --> classless

192.168.0.1/23 (8n.8n.7n 1c.8c)
MSB n> <c LSB

BASE
Decimal base 10
Binary base 2 (0,1)
Octal base 8 (0-7)
Hexadecimal base 16


F8 = 11111000 = 248


RFC


From Router 1 
To Host A 10.10.13.214


Cal 
10.10.13.208/29
8n.8n.8n.5n3c
255.255.255.248
208 --> 1101 0111
        nnnn nccc
          
208+7
192
+16

172.28.228.144/25
8n.8n.8n.1n 7c
144 -> 0000 0000
       nccc cccc
144 -> 1111 1111

nncc cccc
00
01
10
11


Google Cloud
VM - Private IP + Public IP 
- OS
- App
- Runtime
- 

TM Jalan 222
- 222.x.x.x
- ping facebook/yahoo/




cd /usr
cat /etc/passwd

AD/metric
0 directly connected
1 static. configured by user
EIGRP
- AD=90
- metric=BW+DLY
OSPF
- AD=110
- metric=BW
RIP
- AD=120
- metric=Hop Counts
- limit 15 hop counts

1. different routing protocol
- use AD
2. same routing protocol
- use metric
3. same routing protocol + same metric + same subnet/route
- with different netmask/cidr
- use longest prefix/match 

Use AD when there are multiple routing protoocls

ping 192.168.1.100

routing table
S 192.168.1.0/27 via r1
S 192.168.1.0/25 via r2

S* 
O [110/10] 192.168.2.0/28 via r1
O [110/10] 192.168.1.0/12 via r2
O [110/10] 192.168.1.0/27 via r3


Q router ping 192.168.0.1 source loopback 0

Router
- physical interface
- loopback interface
  - testing
  - dummy
  - impact/affect election (OSPF DR)
  - logical interface (always up and running)

Port connections
r1 g0/0 <--> sw1 g0/1
r1 g0/1 <--> sw2 g0/1
r1 g0/2 <--> sw3 g0/1
r2 g0/0 <--> sw2 g0/2
r2 g0/1 <--> sw4 g0/1
r2 g0/2 <--> sw5 g0/1
r3 g0/0 <--> sw4 g0/2
r3 g0/1 <--> sw5 g0/2

IP configurations
PC1 192.168.0.101
PC2 192.168.0.102
r1 g0/0 : 192.168.0.1
r1 g0/1 : 192.168.1.1
r1 g0/2 : 192.168.2.1
r1 lo1  : 10.1.1.1/24
r1 lo2  : 10.11.11.1/24
r2 g0/0 : 192.168.1.2
r2 g0/1 : 192.168.3.2
r2 g0/2 : 192.168.4.2
r2 lo1  : 10.2.2.2
r2 lo2  : 10.22.22.2/24
r3 g0/0 : 192.168.3.3
r3 g0/1 : 192.168.4.3
r3 lo1  : 10.3.3.3
r3 lo2  : 10.33.33.3

sw1 : 192.168.0.11
sw2 : 192.168.1.12
sw3 : 192.168.2.13
sw4 : 192.168.3.14
sw5 : 192.168.4.15

!r1
en
conf t
  hostname r1
  int lo1
    ip add 10.1.1.1 255.255.255.0
  int lo2
    ip add 10.11.11.1 255.255.255.0
  int g0/0
    ip add 192.168.0.1 255.255.255.0
    no shut
  int g0/1
    ip add 192.168.1.1 255.255.255.0
    no shut
  int g0/2
    ip add 192.168.2.1 255.255.255.0
    no shut
  ip route 0.0.0.0   0.0.0.0  192.168.1.2
  end 
copy run start


!r2
en
conf t
  hostname r2
  int lo1
    ip add 10.2.2.2 255.255.255.0
  int lo2
    ip add 10.22.22.2 255.255.255.0
  int g0/0
    ip add 192.168.1.2 255.255.255.0
    no shut
  int g0/1
    ip add 192.168.3.2 255.255.255.0
    no shut
  int g0/2
    ip add 192.168.4.2 255.255.255.0
    no shut
  ip route 0.0.0.0 0.0.0.0 192.168.1.1 
  ip route 10.3.3.0 255.255.255.0 192.168.3.3
  no ip route 10.3.3.0 255.255.255.0 192.168.4.3
  ip route 10.3.3.0 255.255.255.0 192.168.4.3 2

  ip route 10.33.33.0 255.255.255.0 192.168.3.3 
  no ip route 10.33.33.0 255.255.255.0 192.168.4.3
  ip route 10.33.33.0 255.255.255.0 192.168.4.3 2
  end 
copy run start

!r3
en
conf t
  hostname r3
  int lo1
    ip add 10.3.3.3 255.255.255.0
  int lo2
    ip add 10.33.33.3 255.255.255.0
  int g0/0
    ip add 192.168.3.3 255.255.255.0
    no shut
  int g0/1
    ip add 192.168.4.3 255.255.255.0
    no shut
  ip route 0.0.0.0 0.0.0.0 192.168.3.2
  no ip route 0.0.0.0 0.0.0.0 192.168.4.2
  ip route 0.0.0.0 0.0.0.0 192.168.4.2  2

  end 
copy run start


!sw1
en
conf t
   hostname sw1
   int vlan 1
      ip add 192.168.0.11 255.255.255.0
      no shut
   ip default-gateway 192.168.0.1
   end
copy run start


!sw2
en
conf t
   hostname sw2
   int vlan 1
      ip add 192.168.1.12 255.255.255.0
      no shut
   ip default-gateway 192.168.1.1
   end
copy run start


!sw3
en
conf t
   hostname sw3
   int vlan 1
      ip add 192.168.2.13 255.255.255.0
      no shut
   ip default-gateway 192.168.2.1
   end
copy run start


!sw4
en
conf t
   hostname sw4
   int vlan 1
      ip add 192.168.3.14 255.255.255.0
      no shut
   ip default-gateway 192.168.3.2
   end
copy run start


PC1/PC2
- ping 192.168.0.1 
- ping 192.168.1.1
- ping 192.168.2.1
- ping 192.168.1.12
- ping 192.168.2.13


show ip int bri
show run
show ip route
show run int lo0


CDP
- enabled by default
- cisco devices
- VMware vSphere/ESX

vs
LLDP
- disabled by default
- industry standard
  - vendor-based network appliance
- VMware vSphere/ESX
- Windows/Linux


Enable/Disable CDP - global
en
conf t
  [no] cdp run
  end
copy run start

Disable CDP - per interface
en
conf t
  cdp run
  int g0/0
    no cdp enable 
  end
copy run start


Disable LLDP - global
en
conf t
  no lldp run
  end
copy run start


Enable/Disable LLDP - per interface
en
conf t
  lldp run
  int g0/0
    lldp transmit
  int g0/1
    lldp receive
  end
copy run start


Q: u r r1, u can see sw2, but sw2 cannot see you
lldp receive
no lldp transmit


hsrp
- cisco proprietary
vrrp
- universal
glbp
- cisco proprietary
- truly nature of Load Balance or active-active


source IP	192.168.3.1 (never change)
destination IP	192.168.4.2 (never change)
source MAC
destination MAC


HostA send data to HostB which requires stateful, reliable, guaranteed, 
connection-oriented.
Q. on returning frame entering r1, what is the destination MAC?
A. 222:2222
B. 333:2222
C. 333:1111
D. 222:1111




ping facebook.com
ping 8.8.8.8
ping default gw
ping 



default route
ip route 0.0.0.0 0.0.0.0 

ping 
!.!.!
.!.!.
due HSRP/VRRP
redundancy

PCX
- ping loopbacks on r1 - ok
- ping loopbacks on r2 - not ok

r1
- ping loopbacks on r2 - not ok

switches
- ping loopbacks on r1 - ok
- ping loopbacks on r2 - not ok

r2
- ping loopbacks on r1 -  ok




Subnet
192.168.1.0 - 192.168.1.15
192.168.1.16 - 192.168.1.31



!r1
en
conf t
  int g0/1
    ip add 192.168.1.17 255.255.255.240
    ipv6 add 2001:db8:aaaa::1/64
    no shut
    end
copy run start

!r2
en
conf t
  int g0/1
    ip add 192.168.1.30 255.255.255.240
    ipv6 add 2001:db8:aaaa::2/64
    no shut
    end
copy run start

ping 

0.0.0.0 0.0.0.0
192.168.0.0 255.255.255.0
192.168.0.1 255.255.255.0



r3 to r1 192.168.1.1
!r3
en
conf t
  ip route 192.168.1.0 255.255.255.0  g0/1
or
  ip route 192.168.1.1 255.255.255.255  g0/1
  end
copy run start
 
!r2
en
conf t
  ip route 0.0.0.0 0.0.0.0  209.165.202.130  
  ipv6 route ::/0  2001:db8:abcd::2
 end
copy run start

ping - ok




2a00:aaa::1/64
ff0f:2a0::1/64
fe80::1212:
fc11
fd11
unique local
default route ::/64
::1 loopback
127.0.0.1

floating static route
- backup


r2 
- ping 10.3.3.3 & 10.33.33.3
- keep traceroute 10.3.3.3
  - it will use 192.168.3.3 and 192.168.4.3 in 
     round robin manner


untagged frame
tagged frame
\

IEEE 802.1Q

Create VLAN
Configure trunk/access
Configure InterVLAN router

VLAN
10 : HR : 172.16.10.0/24
- PC1 : 172.16.10.101
20 : Engineering : 172.16.20.0/24
- PC2 : 172.16.20.102
- PC3 : 172.16.20.103
30 : Sales : 172.16.30.0/24
- PC4 : 172.16.30.104
- PC6 : 172.16.30.105
40 : Telephony : 172.16.40.0/24
- PC5 : 172.16.40.105
100 : Servers : 172.16.100.0/24
- DHCP server : .111
- DNS Server  : .112
- TFTP Server : .113

!sw1
en
conf t
  vlan 10
    name HR
  vlan 20
    name Engineering
  vlan 30
    name Sales
  vlan 40
    name Telephony
  vlan 100
    name Native Management
  int g0/1
    switchport mode trunk
    switchport trunk allowed vlan 10-100
  int fa0/11
    description connection to PC1
    switchport mode access
    switchport access vlan 10
  int fa0/12
    description connection to PC1
    switchport mode access
    switchport access vlan 20
  end
copy run start

!r1 - configure as InterVLAN router
en
conf t
  int g0/0
    no shut
  int g0/0.10
    encapsulation dot1q 10
    ip address 172.16.10.1 255.255.255.0
  int g0/0.20
    encapsulation dot1q 20
    ip address 172.16.20.1 255.255.255.0
  int g0/0.30
    encapsulation dot1q 30
    ip address 172.16.30.1 255.255.255.0
  int g0/0.40
    encapsulation dot1q 40
    ip address 172.16.40.1 255.255.255.0
  int g0/0.100
    encapsulation dot1q 100
    ip address 172.16.100.1 255.255.255.0
  end
copy run start


	













...
