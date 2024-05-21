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






