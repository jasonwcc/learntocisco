Technique to answer question
1. understand IP calculation
2. POE (Power of elimintation)
3. Look keywords in Answer --> Question

   Go thru each question, look at the answer - use above technique and repeat the question


CAPWAP
- local mode: AP create two CAPWAP tunnels to WLC
  -- management tunnel
  -- data tunnel 

- Flex connect 
: 


IPv6
- 48 bits MAC --> 128 bits IPv6
- Link-local SLAAC (FE80::EUI-64)
- EUI-64
  -- bit 7th toggle
  -- 0000 0010 --> 02
  -- FFFE

1. Globally
  cdp run
  no lldp run

2. Per-Interface
int fa0/X
  no cdp enable

#288
R5
en
conf t
  no cdp run
  int g0/2
     cdp enable
sh cdp nei detail


EtherChannel Protocol
- LACP mode: active (must negotiate) / passive (only, without nego)
- PAGP mode: desirable / auto
- static : on <--> on (both side without nego)

EtherChannel 
en
conf t
int range fa0/1-4
  channel-group 1 mode active 

int port-channel 1
  switchport mode trunk
  switchport trunk native
  switchport trunk allowed vlan 

DTP: 
- cisco model disabled DTP 
- automatically negotiate trunking
- switchport mode { dynamic desirable / dynamic auto / trunk / access }
- why trunk? allow multiple vlan

VTP (VLAN trunking protocol)
- synchronize vlan information among switches
- Configure 
  1. VTP mode : server | client (cannot manage vlan) | transparent (can manage vlan)
  2. domain name: must be same
  3. version: must be same
  4. password: must be same

- revision number



Test switch
- write erase
- reload
- delete flash:vlan.dat


sh vtp status

sw2
en
conf t
  vlan 202
    name MARKETING

Redundancy Routers / FHRP
HSRP
: cisco proprietary
: Active-Standby
: preempt so that previously master become active again
VRRP
: vendor neutral
: Master-Backup
: learn in CCNP
GLBP (Gateway Load Balancing Protocol)
: cisco proprietary
: learn in CCNP
: Active-active


Spanning Tree Protocol
- avoid broadcast storm
- one STP for all VLANs 
- priority 0 - 65535 (16 bits)
- To configure priority
  en
  conf t
     spanning-tree vlan 1-300,400 priority 0,4096,8192
     spanning-tree vlan 1-300,400 root primary (24576)
     spanning-tree vlan 1-300,400 root secondary (28672)

Root Guard
- should enabled on ports facing PC/laptop/server/router
- BPDU - election

BPDU Guard
- should enabled on ports facing PC/laptop/server/router



Per VLAN ST+
- each VLAN will have a STP
- VLAN ID: 12 bits (0-4095)
- 4 bits for priority (


Election use BPDU
- Lowest Priority
- Lowest MAC Address


Port Role
- Root Port 
- Designated Port (FWD)
- Block/Alternate

Status
- Blocking -> Listening -> Learning -> Forwarding

Portfast
- Blocking -> Forwarding
- enabled on specific interface/port
- enabled globally

Confirm answer:
Q212: BE
Q213: C
Q216: AE
Q228: A








1. Globally
  cdp run
  no lldp run

2. Per-Interface
int fa0/X
  no cdp enable

#288
R5
en
conf t
  no cdp run
  int g0/2
     cdp enable
sh cdp nei detail


EtherChannel Protocol
- LACP mode: active (must negotiate) / passive (only, without nego)
- PAGP mode: desirable / auto
- static : on <--> on (both side without nego)

EtherChannel 
en
conf t
int range fa0/1-4
  channel-group 1 mode active 

int port-channel 1
  switchport mode trunk
  switchport trunk native
  switchport trunk allowed vlan 

DTP: 
- cisco model disabled DTP 
- automatically negotiate trunking
- switchport mode { dynamic desirable / dynamic auto / trunk / access }
- why trunk? allow multiple vlan

VTP (VLAN trunking protocol)
- synchronize vlan information among switches
- Configure 
  1. VTP mode : server | client (cannot manage vlan) | transparent (can manage vlan)
  2. domain name: must be same
  3. version: must be same
  4. password: must be same

- revision number


MAC-address-table  = CAM 
Test switch
- write erase
- reload
- delete flash:vlan.dat

Port security

sh vtp status

sw2
en
conf t
  vlan 202
    name MARKETING

Redundancy Routers / FHRP
HSRP
: cisco proprietary
: Active-Standby
: preempt so that previously master become active again
VRRP
: vendor neutral
: Master-Backup
: learn in CCNP
GLBP (Gateway Load Balancing Protocol)
: cisco proprietary
: learn in CCNP
: Active-active


Spanning Tree Protocol
- avoid broadcast storm
- one STP for all VLANs 
- priority 0 - 65535 (16 bits)
- To configure priority
  en
  conf t
     spanning-tree vlan 1-300,400 priority 0,4096,8192
     spanning-tree vlan 1-300,400 root primary (24576)
     spanning-tree vlan 1-300,400 root secondary (28672)

Root Guard
- should enabled on ports facing PC/laptop/server/router
- BPDU - election

BPDU Guard
- should enabled on ports facing PC/laptop/server/router



Per VLAN ST+
- each VLAN will have a STP
- VLAN ID: 12 bits (0-4095)
- 4 bits for priority (


Election use BPDU
- Lowest Priority
- Lowest MAC Address


Port Role
- Root Port 
- Designated Port (FWD)
- Block/Alternate

Status
- Blocking -> Listening -> Learning -> Forwarding

Portfast
- Blocking -> Forwarding
- enabled on specific interface/port
- enabled globally


Router
- choose best route for routing table
  1. same subnet ID > longest prefix (/X)
  2. same subnet ID > lowest administrative distance value
  3. same subnet ID > lowest metric
 
AD - trusted routing protocol
- EBGP: 20
- EIGRP : 90
- OSPF : 110
- IS-IS: 115
- RIP : 120
- IBGP : 200


128-255/25n 7c : 127
192-199/29n 3c : 7

1.0-15/28n 4c: 
1.0-31 /26n 6c: 63 

Confirm answer:
Q212: BE
Q213: C
Q216: AE
Q228: A
Q432: A

10.10.13.0/25n
8n.8n.8n.1n 7c
255.255.255.128

10.10.13.144/28
8n.8n.8n.4n 4c
255.255.255.240


10.10.13.160/29
8n.8n.8n.5n 3c
255.255.255.248

209.165.202.128/27
8n.8n.8n.5n 3c
255.255.255.224

host A: 10.10.13.214

10.10.13.208/29n 3c=7+208=215


EUI-64
1. convert MAC into hex
2. Toggle / invert 7th bit
3. Insert FFFE


11 --> 0001 0001 
12.0/27n 5c 0-31
12.0/28n 4c 0-15

10.0/27n 5c 0-31

IaC - automate/orchestrate
- JSON
vs
- YAML
vs
- XML

JSON
define/declare data structure
- representational data
- object / array
- key: string / Boolean, integer

Cloud
IaaS
- pay what you allocated
- control / customized/ OEM / third-party
PaaS
- pay what you consumed/utilized
- developer / programmer
- java/python code
- fully automated / fully managed
- Cloud Function
SaaS
- pay what you consumed/utilized
- fully automated / fully managed


VM - windows
- cpu 10 utilize 0% cpu
- boot up and run for 1hour 


IaC
ansible
Puppet
Chef
Terraform

Java
Java script
Java script object notation JSON





