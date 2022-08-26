```
Implementing and Administering Cisco Solutions

Course Start and End Dates: 2022-08-22 to 2022-08-26

Access training material via Cisco Learning Network Space . No expiration
https://learningspace.cisco.com/

Access to Cisco Learning Labs is via following URL:
https://cll-ng.cisco.com/users/pblogin
v1.0.34
Active Learning (60H 90D) Pods. Students Credentials
Student: Ahmad Harith
Username: 2022081794129
Password: 2UvPvJNe

Student: Izzati Alwani
Username: 2022081794130
Password: TWeEZQ2e

Student: Khairul Afiq
Username: 2022081794131
Password: SZ2hbs8L

Student: Naquiddin
Username: 2022081794132
Password: kfoD3Scf

Student: Muhaimin
Username: 2022081794133
Password: qFrJpDN5

Student: Amir Hazim
Username: 2022081794134
Password: 4mEpP6Wu

Student: Amirul Faris
Username: 2022081794135
Password: rws52hrZ

Student: Fadhilah
Username: 2022081794136
Password: Z86o9xTx

Instructor Credentials
Username: 2022081794137
Password: SLxHx5Dd



CSMA/CD
Carrier Sense Multiple Access / Collission Detection
- BackOff Algorithm
  2^n

Please Do Not Trust Sales Person Advice
Switch  =  Bridge
- L2 
- MAC Addres

PC / Router / Server
- ARP : resolve IP into MAC
- Broadcast
 
Switch
- Learn MAC 
  - filter / forward
- cache into MAC Address table
   MAC map to Port
- Flooding (L2)

Fiber optics
Fiber channel (SAN protocol) / FC

show running-config (in memory) - non-persistent
show startup-config (in nvram) - persistent

Why configure IP on Switch?
- remote management/administration.
Nxt, configure ssh / telnet

RFC 1918
- private IP can not be routed in internet
- must be translate by NAT
- translate private IP to public IP
- Port Address Translate

192.168.100.100/27
NVRAM - non volatile RAM (persistent)
RAM - volatile
R IP
- hop count
O SPF
- BW
D - EIGRP
- BW + Delay
BGP
- MED
Static route
- hop count
S* Default route
- last resort route
administrative distance

R1 
- 172.16.100.0/24

R2
- 172.16.100.0/27

R3
- 172.16.100.0/22

By default, 
- CDP is enabled
- LLDP is disabled
Q. UDP traffic from Host B to Host A, what is the frame's 
destination  MAC address entering Router?
A. 0800:0222:2222
B. 0800:0333:2222
C. 0800:0333:1111
D. 0800:0222:1111




Exterior GW Protocol
- BGP

Interior GW Protocol
- OSPF 
  : Link State
- RIP
  : Distance Vector
  : v1 classful   : v2 classless
  10.1.1.0/29 --> 10.0.0.0/8
  128.x.x.x-191.x.x.x/16
- IGRP --> EIGRP (Cisco Propietory)
  :  DV + Link State
- IS-IS
  : Link State

1. Administrative Distance (same route from different routing
protocol)
- RIP : 120
- OSPF: 110
- EIGRP : 90
- Directly Connected Route : 0
- Static : 1
2. Metric (different routes from same routing protocol)
  - RIP : Hop count 
  - OSPF: Bandwitdh (10M/100M/1G/10G/25G)
  - EIGRP : Bandwitdh + Delay (show interface fa0/1)
  - BGP : MED (Multiple exit Discriminator = Priority)
HW1: RM10 / 2 Tolls / 2 Lanes
HW2: RM1 / 10 Tolls / 10 Lanes
3. Longest Prefix (same network destination but different 
CIDR)
192.168.100.0/27 via R1
192.168.100.0/24 via R2
192.168.100.0/30 via R3

Distance Vector 
- Select best path from hop count
- Keep routing table (best route)
- less overheads
vs Link-state
- Select best path from bw/delay/mtu/reliability/txload/rxload
- Keep
   1. Neighboring Table (adjacent)
       - Router interface speed / characteristic / model 
       - Hello: 10 sec /  Dead Timer: 40 sec
   2. Topology Table
      - All routes
   3. Routing Table
      - Best route (recalculate)
- Consume lots of memory + cpu utilization 
   - OSPF use disjktra algoritm


Election
- Designated Router (Area leader)
- BDR

OSPF uses following multicast ip:
- 224.0.0.5
- 224.0.0.6
- ff02::5
- ff02::6
ECMP: Equal cost multipath
- 4x (configurable upto 16x)

show ip ospf nei
Formula
Cost = Reference BW / Actual Link BW
100 MB / 100 MB = 1
100 MB / 10 MB = 10


STP
- IEEE 802.1D
- single STP for all VLANs (0-4095)
Rapid STP
- IEEE 802.1W
- rapid / fast convergency
PVST+
- Per VLAN STP
- overhead
- Cisco propietory
rapid PVST+
- rapid / fast convergency
MSTP
- Multiple STP
- universal
- IEEE 802.1s

1. Elect a Root Bridge
    a. Priority (lower)
    b. MAC (lower)
2. Root port / Designated Port
     a. RP going towards the Root Bridge
     b. DP come to me to the Root

1000 VLAN
1-500 STP1
501-700 STP2
700-1000 STP3

> en
# conf t
(conf) # vlan 100
(conf-vlan) # name 
(conf) # no spanning-tree vlan 100

Listening
- exchange BPDU (bridge PDU)
- elect Root Bridge
Learning
- Root port / Designated port / Disabled / Alternate
- Forwarding / Blocking
PBq
- performance-based question

EtherChannel Mode
LACP  (active/passive)
- universal protocol
PAGP (desireable/auto)
- cisco propietory
Static (on)
- don't use protocol
- universal

Sw1			Sw2
A			P	= LACP
A			A	= LACP
P			P 	= no LACP

FHRP
1. HSRP (HA)
- cisco propieotry
- active / passive
- failover
2. VRRP (HA)
- Universal 
- active / passive
- failover
3. Gateway Load Balance Protocol (round robin)
- cisco propietory
- active / active
- failover + load balance

netmask
ACL - wildcard mask
0 - i care
1 - i don't care / anything
/24 --> 255.255.255.0
        --> 0.0.0.255
Vlan1 --> VLan99
- tagged 
- native/default
- management traffic (DHCP,DNS, NTP, SNMP, monitoring, 
SSH)

HSRP vs VRRP vs GLBP
- flapping
- tracking + preemptive

Given 192.168.100.123/18, what is the networkID?
--> answer: 192.168.64.0
```

# ACL
```
Numbered Standard ACL 
- 1 to 99,
- Look at source address
Numbered Extended ACL
- 100 to 199
- Look at source/destination address, src/destination port number
protocol.
Numbered when delete, entire list will deleted

Named Standard / Extended ACL 
- IOS v15 onward
- change / speciy rule number
- Delete specific rule
Last rule : Deny any 
```

## Lets look at some example finding out the networkID and wildcard mask, then follow by example acl command
```
- Criteria 1: Deny 172.16.200.55/20
access-list 1 deny networkID wildcard
access-list 1 deny 172.16.192.0 0.0.15.255

- Criteria 2: Deny these subnets range 
172.16.160.0/27
172.16.161.0/26
172.16.164.224/28
172.16.165.192/26
172.16.160.160/27
172.16.163.96/28
172.16.167.128/29
172.16.162.96/24

1. Find the first subnet and last subnet
172.16.160.0/27 --> 
172.16.167.128/29 -->
2.  Convert above non matching octet to bin. 
160.0     -->  1010 0 000.0000 0000
167.128 -->  1010 0 111.1000 0000
3. Find matching bit
1010 0xxx.xxxx xxxx
4. Calculate networkID and WC.
NID : 172.16.160.0
WC :         0.0.7.255
5. Execute the cmd
access-list 2 deny 172.16.160.0 0.0.7.255
access-list 2 permit any

- Criteria 4: Permit  these subnets range 
172.16.200.0/27
172.16.192.0/26
172.16.194.224/28
172.16.207.192/26
172.16.200.160/27
172.16.198.96/28
172.16.199.128/29
172.16.200.96/24

1. Find the first subnet and last subnet
172.16.192.0/26
172.16.207.192/26
2.  Convert above non matching octet to bin. 
192 -->  1100 0000
207 -->  1100 1111
3. Find matching bit
1100 xxxx
0000 1111
4. Calculate networkID and WC.
NID : 172.16.192.0 
WC :          0.0.15.255 
5. Execute the cmd
access-list 2 permit 172.16.192.0 0.0.15.255

- Criteria 5: Permit  these subnets range 
192.100.40.0/27
192.100.54.0/28
192.100.32.0/26
192.100.63.96/27
192.100.48.160/28
192.100.44.240/29
192.100.33.96/29

```
