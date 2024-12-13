```

https://trainocate.com/manage-attendance?ClassId=6685

Download materials -
https://github.com/jasonwcc/learntocisco
(https://trainocate.com/manage-attendance?ClassId=6685

Download materials -
- https://github.com/jasonwcc/learntocisco
- https://tinyurl.com/jtodshareddocs

Download Cisco packet tracer
- network academy 
- https://tinyurl.com/cisconetacad2024

4. indra.silavurajoo@tm.com.my
8. replace - Muhammad Azim Mirza azim.farid@tm.com.my
 
Cisco Router/Switch
- BIOS  = ROMMON
- windows = IOS (customizeable/upgradeable)


Router > en
# config ter
# hostname JasonRo
JasonRo #
Switch >


user		: geomancer1o1@gmail.com
password	: C@ngetin43

user  		: jasonwcc.cisco@gmail.com
password	: A@bc1234

coaxial

Straight-thru (copper)
- different device type
- PC to Switch

Cross-over (copper)
- same device type
- router to router
- switch to switch
- pc to pc
- server to server
- PC to server (NOS)
- Switch to HUB


Roll-over (console)


8 pins
4 pins 
- Transmit +
- Transmit -
- Rec + 
- Rec -

Cat 8
SFTP 40m / 40G / 2GHz


LAN
- local
vs
WAN
- wide / jauh
MAN
PAN
SAN
- FC
- FCoE
- iSCSI
- NVMeoFC/TCP
NAS
- NFS
- CIFs

NIC
HBA (FC)
CNA (FCoE)


App --> IP in Payload
IP address
- logical address
- IPv4 (32 bits) and IPv6 (128bits)
  9.168.0.255 /23n (9c)
- Just like number plate
- routable
vs
MAC address (48 bits)
- hardware / physical address
- cannot change
- given IEEE (24 bits OUI) + 24 client
- Just like engine chassis number
- no routable

Standard ethernet frame
IEEE 802.3 MTU : 1500 byte
Jumbo Ethernet frame 
IEEE xxx MTU : 9000 byte


IPv6
- unicast, multi, anycast


ARP --> NDP

NetBIOS
- file / print
- AD

copy run(DRAM) start(NVRAM)
copy start run

!Config on ro1
en
conf t
  int g0/0
   !inter connect to sw1
    ip address 10.0.0.254 255.0.0.0
    no shut
  int g0/1
    ip address 20.0.0.254 255.0.0.0
    no shut

  int g0/2
    no ip address 30.0.0.254 255.0.0.0
    end
copy run start

!PC1 ping 10.0.0.254 

!Config on sw1
en
conf t
  int vlan 1
    ip add 10.0.0.253 255.0.0.0
    no shut
    ip default-gateway 10.0.0.254
    end
copy run start

!Config on sw2
en
conf t
  int vlan 1
    ip add 20.0.0.253 255.0.0.0
    ip default-gateway 20.0.0.254
    no shut
    end
copy run start

Verify
Sw1 ping 10.0.0.1, 10.0.0.2, 10.0.0.253, 20.0.0.254/253



  



















)
...
](https://trainocate.com/manage-attendance?ClassId=6685

Download materials -
- https://github.com/jasonwcc/learntocisco
- https://tinyurl.com/jtodshareddocs

Download Cisco packet tracer
- network academy 
- https://tinyurl.com/cisconetacad2024

4. indra.silavurajoo@tm.com.my
8. replace - Muhammad Azim Mirza azim.farid@tm.com.my
 
Cisco Router/Switch
- BIOS  = ROMMON
- windows = IOS (customizeable/upgradeable)


Router > en
# config ter
# hostname JasonRo
JasonRo #
Switch >


user		: geomancer1o1@gmail.com
password	: C@ngetin43

user  		: jasonwcc.cisco@gmail.com
password	: A@bc1234

coaxial

Straight-thru (copper)
- different device type
- PC to Switch

Cross-over (copper)
- same device type
- router to router
- switch to switch
- pc to pc
- server to server
- PC to server (NOS)
- Switch to HUB


Roll-over (console)


8 pins
4 pins 
- Transmit +
- Transmit -
- Rec + 
- Rec -

Cat 8
SFTP 40m / 40G / 2GHz


LAN
- local
vs
WAN
- wide / jauh
MAN
PAN
SAN
- FC
- FCoE
- iSCSI
- NVMeoFC/TCP
NAS
- NFS
- CIFs

NIC
HBA (FC)
CNA (FCoE)


App --> IP in Payload
IP address
- logical address
- IPv4 (32 bits) and IPv6 (128bits)
  9.168.0.255 /23n (9c)
- Just like number plate
- routable
vs
MAC address (48 bits)
- hardware / physical address
- cannot change
- given IEEE (24 bits OUI) + 24 client
- Just like engine chassis number
- no routable

Standard ethernet frame
IEEE 802.3 MTU : 1500 byte
Jumbo Ethernet frame 
IEEE xxx MTU : 9000 byte


IPv6
- unicast, multi, anycast


ARP --> NDP

NetBIOS
- file / print
- AD

copy run(DRAM) start(NVRAM)
copy start run

!Config on ro1
en
conf t
  int g0/0
   !inter connect to sw1
    ip address 10.0.0.254 255.0.0.0
    no shut
  int g0/1
    ip address 20.0.0.254 255.0.0.0
    no shut

  int g0/2
    no ip address 30.0.0.254 255.0.0.0
    end
copy run start

!PC1 ping 10.0.0.254 

!Config on sw1
en
conf t
  int vlan 1
    ip add 10.0.0.253 255.0.0.0
    no shut
    ip default-gateway 10.0.0.254
    end
copy run start

!Config on sw2
en
conf t
  int vlan 1
    ip add 20.0.0.253 255.0.0.0
    no shut
    ip default-gateway 20.0.0.254
    end
copy run start

Verify
Sw1 ping 10.0.0.1, 10.0.0.2, 10.0.0.253, 20.0.0.254/253

!Config on ro2
en
conf t
  int g0/0
    ip address 10.0.0.252 255.0.0.0
    no shut
  int g0/1
    ip address 30.0.0.252 255.0.0.0
    no shut
   end
copy run start

!Config on sw3
en
conf t
  int vlan 1
    ip add 30.0.0.253 255.0.0.0
    no shut
    ip default-gateway 30.0.0.252
    end
copy run start

  
sw3 should be able to ping 30.0.0.252, 10.0.0.252

Subnets
10.0.0.0/8
20.0.0.0/8
30.0.0.0/8

!ro1 configure static route towards missing route
en 
 conf t
  ip route 30.0.0.0 255.0.0.0 10.0.0.252
  end
copy run start
show ip route

!ro2 configure default route towards missing route
en 
 conf t
  ip route 0.0.0.0    0.0.0.0 10.0.0.254
  end
copy run start
show ip route


dynamic route - OSPF/RIP/EIGRP

ro2 g0/0 10.0.0.252
ro2 g0/1 30.0.0.252
ro2 g0/2 20.0.0.252
dns 10.0.0.200

NetBIOS
SMBv1

IPv4  / IPv6
- Subnet/Network ID | Host ID
- netmask

A 0.0.0.0 - 127.255.255.255
B 128.0.0.0 - 191.255.255.255
C 192.0.0.0 - 223.255.255.255
D Multicast 224.0.0.0 - 239.255.255.255
E Reserved for future - 240.0.0.0 - 255.255.255.255

Private IP (IETF RFC 1918)
A 10.x.x.x
B 172.16.x.x - 172.31.x.x
C 192.168.x.x/24 
vs
Public IP
A 1.0.0.1 - 9.255.255.255, 11.0.0.1 - 126.255.255.255
B 128.x.x.x - 172.15.255.255, 172.32.x.x - 191.255.255.255
C 192.x.x.x - 192.167.x.x , 192.169.x.x - 223.255.255.255

show ip route
netstat -rn = route print


Decimal  0-10
- base 10
Binary 0,1
- base 2
Octal 0-7
- base 8
Hexadecimal 0-9,a-f
- base 16


100 ==> 



!ro1
en
conf t
  int g0/1
    ip add 192.168.1.17 255.255.255.240
    ipv6 add 2001:db8:aaaa::1/64
   end
copy run start

!ro2
en
conf t
  int g0/1
    ip add 192.168.1.30 255.255.255.240
    ipv6 add 2001:db8:aaaa::2/64
   end
copy run start

!ro1 configured as DHCP server
en
conf t
ip dhcp excluded-address 10.0.0.200 10.0.0.254
ip dhcp pool Sales_10
  network 10.0.0.0 255.0.0.0
  default-router 10.0.0.252 
  dns-server 10.0.0.200
  domain-name cisco.com

ip dhcp excluded-address 20.0.0.200 20.0.0.254
ip dhcp pool HR_20
  network 20.0.0.0 255.0.0.0
  default-router 20.0.0.254
  dns-server 10.0.0.200
  domain-name cisco.com

ip dhcp excluded-address 30.0.0.200 30.0.0.254
ip dhcp pool Operation_30
  network 30.0.0.0 255.0.0.0
  default-router 30.0.0.252
  dns-server 10.0.0.200
  domain-name cisco.com

!ro2 configured as Relay Agent for subnet 30.x.x.x/8
en
conf t
int g0/1
  ip helper-address 10.0.0.254	
  end
copy run start

















)
](https://trainocate.com/manage-attendance?ClassId=6685

Download materials -
- https://github.com/jasonwcc/learntocisco
- https://tinyurl.com/jtodshareddocs

Download Cisco packet tracer
- network academy 
- https://tinyurl.com/cisconetacad2024

4. indra.silavurajoo@tm.com.my
8. replace - Muhammad Azim Mirza azim.farid@tm.com.my
 
Cisco Router/Switch
- BIOS  = ROMMON
- windows = IOS (customizeable/upgradeable)


Router > en
# config ter
# hostname JasonRo
JasonRo #
Switch >


user		: geomancer1o1@gmail.com
password	: C@ngetin43

user  		: jasonwcc.cisco@gmail.com
password	: A@bc1234

coaxial

Straight-thru (copper)
- different device type
- PC to Switch

Cross-over (copper)
- same device type
- router to router
- switch to switch
- pc to pc
- server to server
- PC to server (NOS)
- Switch to HUB


Roll-over (console)


8 pins
4 pins 
- Transmit +
- Transmit -
- Rec + 
- Rec -

Cat 8
SFTP 40m / 40G / 2GHz


LAN
- local
vs
WAN
- wide / jauh
MAN
PAN
SAN
- FC
- FCoE
- iSCSI
- NVMeoFC/TCP
NAS
- NFS
- CIFs

NIC
HBA (FC)
CNA (FCoE)


App --> IP in Payload
IP address
- logical address
- IPv4 (32 bits) and IPv6 (128bits)
  9.168.0.255 /23n (9c)
- Just like number plate
- routable
vs
MAC address (48 bits)
- hardware / physical address
- cannot change
- given IEEE (24 bits OUI) + 24 client
- Just like engine chassis number
- no routable

Standard ethernet frame
IEEE 802.3 MTU : 1500 byte
Jumbo Ethernet frame 
IEEE xxx MTU : 9000 byte


IPv6
- unicast, multi, anycast


ARP --> NDP

NetBIOS
- file / print
- AD

copy run(DRAM) start(NVRAM)
copy start run

!Config on ro1
en
conf t
  int g0/0
   !inter connect to sw1
    ip address 10.0.0.254 255.0.0.0
    no shut
  int g0/1
    ip address 20.0.0.254 255.0.0.0
    no shut

  int g0/2
    no ip address 30.0.0.254 255.0.0.0
    end
copy run start

!PC1 ping 10.0.0.254 

!Config on sw1
en
conf t
  int vlan 1
    ip add 10.0.0.253 255.0.0.0
    no shut
    ip default-gateway 10.0.0.254
    end
copy run start

!Config on sw2
en
conf t
  int vlan 1
    ip add 20.0.0.253 255.0.0.0
    no shut
    ip default-gateway 20.0.0.254
    end
copy run start

Verify
Sw1 ping 10.0.0.1, 10.0.0.2, 10.0.0.253, 20.0.0.254/253

!Config on ro2
en
conf t
  int g0/0
    ip address 10.0.0.252 255.0.0.0
    no shut
  int g0/1
    ip address 30.0.0.252 255.0.0.0
    no shut
   end
copy run start

!Config on sw3
en
conf t
  int vlan 1
    ip add 30.0.0.253 255.0.0.0
    no shut
    ip default-gateway 30.0.0.252
    end
copy run start

  
sw3 should be able to ping 30.0.0.252, 10.0.0.252

Subnets
10.0.0.0/8
20.0.0.0/8
30.0.0.0/8

!ro1 configure static route towards missing route
en 
 conf t
  ip route 30.0.0.0 255.0.0.0 10.0.0.252
  end
copy run start
show ip route

!ro2 configure default route towards missing route
en 
 conf t
  ip route 0.0.0.0    0.0.0.0 10.0.0.254
  end
copy run start
show ip route


dynamic route - OSPF/RIP/EIGRP

ro2 g0/0 10.0.0.252
ro2 g0/1 30.0.0.252
ro2 g0/2 20.0.0.252
dns 10.0.0.200

NetBIOS
SMBv1

IPv4  / IPv6
- Subnet/Network ID | Host ID
- netmask

A 0.0.0.0 - 127.255.255.255
B 128.0.0.0 - 191.255.255.255
C 192.0.0.0 - 223.255.255.255
D Multicast 224.0.0.0 - 239.255.255.255
E Reserved for future - 240.0.0.0 - 255.255.255.255

Private IP (IETF RFC 1918)
A 10.x.x.x
B 172.16.x.x - 172.31.x.x
C 192.168.x.x/24 
vs
Public IP
A 1.0.0.1 - 9.255.255.255, 11.0.0.1 - 126.255.255.255
B 128.x.x.x - 172.15.255.255, 172.32.x.x - 191.255.255.255
C 192.x.x.x - 192.167.x.x , 192.169.x.x - 223.255.255.255

show ip route
netstat -rn = route print


Decimal  0-10
- base 10
Binary 0,1
- base 2
Octal 0-7
- base 8
Hexadecimal 0-9,a-f
- base 16


100 ==> 



!ro1
en
conf t
  int g0/1
    ip add 192.168.1.17 255.255.255.240
    ipv6 add 2001:db8:aaaa::1/64
   end
copy run start

!ro2
en
conf t
  int g0/1
    ip add 192.168.1.30 255.255.255.240
    ipv6 add 2001:db8:aaaa::2/64
   end
copy run start

!ro1 configured as DHCP server
en
conf t
ip dhcp excluded-address 10.0.0.200 10.0.0.254
ip dhcp pool Sales_10
  network 10.0.0.0 255.0.0.0
  default-router 10.0.0.252 
  dns-server 10.0.0.200
  domain-name cisco.com

ip dhcp excluded-address 20.0.0.200 20.0.0.254
ip dhcp pool HR_20
  network 20.0.0.0 255.0.0.0
  default-router 20.0.0.254
  dns-server 10.0.0.200
  domain-name cisco.com

ip dhcp excluded-address 30.0.0.200 30.0.0.254
ip dhcp pool Operation_30
  network 30.0.0.0 255.0.0.0
  default-router 30.0.0.252
  dns-server 10.0.0.200
  domain-name cisco.com

!ro2 configured as Relay Agent for subnet 30.x.x.x/8
en
conf t
int g0/1
  ip helper-address 10.0.0.254	
  end
copy run start

!Administrative Distance (AD)
0 - directly connected 
1 - static/default route
90 - EIGRP 
110 - OSPF
120 - RIP

Metrics
EIGRP - BW + Delay
OSPF  - BW
RIP   - Hop count


Router - route selection
1. AD (lower) if use different routing protocol
2. Metric (lower) if use same routing protocol
3. route with matching longest prefix


show run
show ip int brief
show ip route
show ip arp
show mac-address-table



Add another Ro3
- static route
- redundant routes

!common/base configuration
en
conf t
  line console 0
      exec-timeout 0 0
      logging sync
 end
copy run start



!ro1
en 
conf t
int g0/0
ipv6 add aaaa:1010::201/64
int g0/1
ip add 20.0.0.201 255.0.0.0
ipv6 add bbbb:2020::201/64
end

!ro2
en 
conf t
int g0/0
ip add 10.0.0.202 255.0.0.0
ipv6 add aaaa:1010::202/64
int g0/1
ip add 30.0.0.202 255.0.0.0
ipv6 add cccc:3030::202/64
end
copy run start

!ro3
en 
conf t
int g0/0
no ip add 30.0.0.203 255.0.0.0
ipv6 add cccc:3030::203/64
end
copy run start

!ro1 reconfigure static route
en
show ip route
show run | include ip route
conf t
no ip route 30.0.0.0 255.0.0.0 10.0.0.252
ip route 30.0.0.0 255.0.0.0 10.0.0.202
end
copy run start

!ro2 reconfigure default route
en
show run | include ip route
conf t
no ip route 0.0.0.0 0.0.0.0 10.0.0.254
ip route 0.0.0.0 0.0.0.0 10.0.0.201
ip route 192.168.30.0 255.255.255.0 30.0.0.203
end
copy run start

!on all switch, reconfigure default-gateway

!ro3 configure default route via ro2
en
conf t
ip route 0.0.0.0 0.0.0.0 30.0.0.202

end
wr

!ro1 create dummy network using loopback interface
en
conf t
int loopback 222
   ip add 172.16.10.201 255.255.0.0
end
copy run start

!ro2 create dummy network using loopback interface
en
conf t
int loopback 222
   ip add 172.17.10.202 255.255.0.0
end
copy run start

!ro1 reconfigure static into default route
en
conf t
  ip route 30.0.0.0 255.0.0.0 10.0.0.202
  ip route 0.0.0.0   0.0.0.0 10.0.0.202
  end
copy run start

!ro3 create dummy network using loopback interface
en
conf t
int loopback 555
   ip add 192.168.30.203 255.255.255.0
end
copy run start

!ro2 configure g0/2
en
conf t
   int g0/2
      ip add 20.0.0.202 255.0.0.0
      no shut
      end
copy run start

!ro2 configure redundant static/default route via ro1
en
show run | include ip route
conf t
no ip route 0.0.0.0 0.0.0.0 10.0.0.254
ip route 172.16.0.0 255.255.0.0 10.0.0.201 1
ip route 172.16.0.0 255.255.0.0 20.0.0.201 10
ip route 192.168.30.0 255.255.255.0 30.0.0.203
end
copy run start


Enable/Disable CDP/LLDP
1. On ro2, Disable CDP globally (all interfaces incoming/outgoing)
2. But enable CDP on g0/0 only
!ro2
en
conf t
   no cdp run
   int g0/0
     cdp enable
end
copy run start


Q. Disable CDP completely, but enable LLDP on g0/0 and g0/2
!ro2
en
conf t
  no cdp run
  lldp run
int g0/0
   lldp transmit
   lldp receive
end
wr

IEEE 802.1Q
- VLAN
- supports 0-4095 (12 bits)
- vlan 1 (native/management/default)
- each vlan has its own subnet
- create vlan 2, 3, 4


switchport mode access
- allow one vlan to go thru
- connect to PC/Server/Router

switchport mode trunk
- allow multiple vlan
- connect to switch/InterVLAN router/ESX/Hyper-V/IBM PowerVM/Proxmox/OpenStack 

Dynamic Auto (default)
Dynamic Desirable
Trunk
Access

!sw3
en
conf t
  vlan 2
    name HR
  vlan 3
    name Sales
  vlan 4
    name Operation
  vlan 15
    name Engineering
  int range fa0/10-11
     switchport mode trunk
  int fa0/1
     switchport mode access
     switchport access vlan 2
  int fa0/5
     switchport mode access
     switchport access vlan 4
end
copy run start

!sw4
en
conf t
  vlan 2
    name HR
  vlan 3
    name Sales
  vlan 4
    name Operation
  vlan 15
    name Engineering
  hostname sw4
  int range fa0/10-12
     switchport mode trunk
  int fa0/2
     switchport mode access
     switchport access vlan 2
  int fa0/3
     switchport mode access
     switchport access vlan 3
end
copy run start

!sw5
en
conf t
  hostname sw5
  vlan 2
    name HR
  vlan 3
    name Sales
  vlan 4
    name Operation
  vlan 15
    name Engineering
  int range fa0/10-12
     switchport mode trunk
  int fa0/4
     switchport mode access
     switchport access vlan 3
end
copy run start

*** Network Topology configuration ***
PC1 (sw3 fa0/1) - vlan 2 - 30.0.2.1
PC2 (sw4 fa0/2) - vlan 2 - 30.0.2.2
PC3 (sw4 fa0/3) - vlan 3 - 30.0.3.3
PC4 (sw5 fa0/4) - vlan 3 - 30.0.3.4
PC5 (sw3 fa0/5) - vlan 4 - 30.0.4.5
DNS (sw1 fa0/10) - vlan 1 - 10.0.0.101 (gw:10.0.0.100)
SW1 - 10.0.0.253 
SW2 - 20.0.0.253
SW3 - 30.0.0.253
RO1 g0/0 10.0.0.201 / aaaa:1010::201/64
RO1 g0/1 20.0.0.201 / bbbb:2020::201/64
RO2 g0/0 10.0.0.202 / aaaa:1010::202/64
RO2 g0/1 30.0.0.202 / cccc:3030::202/64
PC1 (sw3 fa0/1) - vlan 2 - 30.0.2.1
PC2 (sw4 fa0/2) - vlan 2 - 30.0.2.2
PC3 (sw4 fa0/3) - vlan 3 - 30.0.3.3
PC4 (sw5 fa0/4) - vlan 3 - 30.0.3.4
PC5 (sw3 fa0/5) - vlan 4 - 30.0.4.5

Vlan
1 30.0.0.0/24
2 30.0.2.0/24
3 30.0.3.0/24
4 30.0.4.0/24

Test
Pc1 should be able ping pc2
Pc3 should be able ping pc4

!ro2 configured as InterVLAN router
en
conf t
  int g0/1
    ip add 30.0.0.202 255.255.255.0
  int g0/1.2
    encap dot1q 2
    ip add 30.0.2.202 255.255.255.0
  int g0/1.3
    encap dot1q 3
    ip add 30.0.3.202 255.255.255.0
  int g0/1.4
    encap dot1q 4
    ip add 30.0.4.202 255.255.255.0
end
copy run start

!sw3 g0/1 configured as trunk
en
conf t
  int g0/1
    switchport mode trunk
end
copy run start

Test
every PC can every PC in the multi vlans environment

!ro2
show ip int brief
show ip route
show run

IGP
- RIP1/2 (DV),OSPF(LS),IGRP(DV),IS-IS(S), EIGRP(DV+LS)
EGP
- BGP

Distance Vector
- care hop count as best path
- care about one table (routing table)
Link State
- care bw/delay/mtu/reliability/txload/rxload
- hello timer to directly connected neighbor each 10 sec
- dead timer 40 seconds 
- care 3 tables:
  1. Neighbor/Adjacency table
  2. Topology table (all routes)
  3. Routing table (best route)

!ro1
en
conf t
  router ospf 1
    network 10.0.0.0  0.255.255.255 area 0
    network 20.0.0.0  0.255.255.255 area 0 
    network 172.0.0.0 0.255.255.255 area 1
end
copy run start

!ro2
en
conf t
  router ospf 1
    network 0.0.0.0  31.255.255.255 area 0
    network 172.0.0.0 0.255.255.255 area 1
end
copy run start

!ro3
en
conf t
  router ospf 2
    passive-interface g0/0
  exit
  int g0/0
     ip ospf 2 area 0
  int loop 555
     ip ospf 2 area 1

end
copy run star

Netmask
- determine networkID/hostIP
- determine first/last usable
vs
Wildcard mask
- OSPF and ACL
- determine which range of ips


!on all router, remove static/default routes
en
sh run | inc ip route
add no in front every command
and paste into the ro configuration
copy run start

Election for Designated Router (DR)
1. Priority (1-255) (higher number wins)
2. Highest IP from router-id
3. Highest IP from loopback interfaces
4. Highest IP from physical interfaces

Election for Root Bridge (RB)
1. Priority (0-65535) (lower number winner)
2. Lowest MAC address
Determine port role
1. Root port
2. Designated port
   - on all ports on RB
3. alternate port
Determine port status
1. Forwarding (root/designated)
2. Blocking (alternate)

Per VLAN ST+
original election
- BLK --> LIS --> LRN --> FWD

Portfast
- access port (PC/Server/Router)
- BLK --> FWD


!sw2
en
conf t
  int range fa0/10-13
    channel-group 1 mode active
  int port-channel 1
     switchport mode trunk
end
wr

!sw6
en
conf t
  int range fa0/10-13
    channel-group 1 mode passive
  int port-channel 1
     switchport mode trunk
end
wr

sh ip int brief
sh etherchannel
sh etherchannel summary

1. HSRP
- cisco propietory
- redundancy only
2. VRRP
- generic protocol
- redundancy only
3. GLBP
- cisco propietory
- redundancy + load balancce


!ro1 configured as HSRP group active partner
en
conf t
  int g0/0
     standby version 2
     standby 1 ip 10.0.0.100
     standby 1 priority 250
     standby 1 preempt 
  int g0/1
     standby version 2
     standby 2 ip 20.0.0.100
     standby 2 priority 250
     standby 2 preempt 
end
copy run start

!ro2 configured as HSRP group standby partner
en
conf t
  int g0/0
    standby version 2
    standby 1 ip 10.0.0.100
    standby 1 preempt 
  int g0/1
     no standby version 2
     no standby 2 ip 20.0.0.100
     no standby 2 preempt
  int g0/2
      standby version 2
      standby 2 ip 20.0.0.100
      standby 2 preempt 
end
copy run start

Verify configuration
show standby brief

ACL
- create numbered list 
  - standard list vs extended list
  - sequence fixed to 10 > 20 > 30 > 40 
vs create named list
  - modify sequence
  - add rule before/after existing
  - delete specific rule
- permit / deny 
- apply list to interface
  - in vs out
- remember protocol/port number telnet(tcp/23), ssh(tcp/22), web(tcp/80,tcp/443) , smtp (tcp/25) , ftp (tcp/20,21) , tftp (udp/69)

Cisco Best Practices for ACL
- Standard (1-99) List : router closest to destination
- Extended (100-199) list : router closest to source

host - specific
any - 0.0.0.0 255.255.255.255

permit 0.0.0.0 255.255.255.255 / permit any
permit 10.0.0.6 0.0.0.0 / permit host 10.0.0.6
permit host 20.0.0.1
permit 192.168.100.0 0.0.63.255
deny any 
1  0000 0001
3  0000 0011
7  0000 0111
15  
31 0001 1111
63 
127 
255


192.168.96.0-255
192.168.97.0-255
..
..
192.168.127.0-255

Formula
1. convert first subnet to binary
192.168.96.0 --> 0110 0000

2. convert last subnet to binary
192.168.127.255> 0111 1111

3. Find matching bits from left
x               > nnnc cccc
192.168.96.0    > 0110 0000
0.0.31.255      > 0001 1111

permit 192.168.96.0 0.0.31.255


en
conf t
 ip access-list standard jacl1
    5 permit host 10.0.0.1
    20 permit host 10.0.0.2
    40 permit host 10.0.0.4
    88 permit host 10.0.0.199
    25 deny 10.0.0.0 0.0.0.255
end
wr

Connection
ro3 g0/1 --> sw7 g0/1
sw7 fa0/10 --> facebook.com fa0
sw7 fa0/11 --> yahoo.com fa0

!ro2 configure default route via ro3
en
conf t
  ip route 0.0.0.0 0.0.0.0 30.0.0.203
end

!ro3 configure g0/1
en
conf t
  int g0/1
     ip add 200.0.0.203 255.255.255.0
     no shut
  ip route 0.0.0.0 0.0.0.0 30.0.0.202
end
wr

facebook.com
- IP 200.0.0.101 /24
- GW 200.0.0.203
yahoo.com
-IP 200.0.0.102/24
- GW 200.0.0.203
DNS
- connect sw1 fa0/10
- IP 10.0.0.101/8
- GW 10.0.0.100

!ro2 inject default route into OSPF environment
en
conf t
   router ospf 1
      default-information originate
   end
wr


!Policy 1
- deny PC6 from entering internet
- permit everything else

!ro3 Implement the Policy using standard ACL
en
conf t
  access-list 5 deny host 10.0.0.6
  access-list 5 permit any
  int g0/1
     ip access-group 5 out
end
copy run start

!Policy 2
- deny subnet 20.0.0.0/8 from surfing internet
- permit everything else



!ro2 Implement the Policy using standard ACL
en
conf t
    access-list 110 deny tcp 20.0.0.0 0.255.255.255 200.0.0.0 0.0.0.255 eq 80
    access-list 110  deny tcp 20.0.0.0 0.255.255.255 200.0.0.0 0.0.0.255 eq 443
    access-list 110  permit ip any any
   int g0/1
     ip access-group 110 out
end
wr

NAT
- translate private ip into public ip
- RFC 1918 10.x.x.x, 172.16-172.31.x.x, 192.168.x.x

1. Static NAT
- every private must have one public
- Port Forwarding
2. Dynamic NAT
- every private must have one public (keep changing)
- PC1 10.0.0.1 translate 200.0.0.2
- PC2 10.0.0.2 translate 200.0.0.1

3. Dynamic NAt with Overloading / PAT

!ro3 configured as Static NAT
en
conf t
  int g0/0
    ip nat inside
  int g0/1
    ip nat outside
  ip nat inside source static 30.0.2.1 200.0.0.141
  ip nat inside source static 30.0.2.2 200.0.0.142
   end
copy run start

Test nat
PC1 ping 200.0.0.101
PC2 ping 200.0.0.102

!ro3 show ip nat translation


!ro3 configured as Dynamic NAT
en
conf t
  int g0/0
    ip nat inside
  int g0/1
    ip nat outside
  no ip nat inside source static 30.0.2.1 200.0.0.141
  no ip nat inside source static 30.0.2.2 200.0.0.142
  access-list 10 permit 30.0.2.0 0.0.0.255
  ip nat pool TMpool1 200.0.0.171 200.0.0.175 netmask 255.255.255.0
  ip nat inside source list 10  pool TMpool1 
   end
copy run start

Test nat
PC1 ping 200.0.0.101
PC2 ping 200.0.0.102


SSH
ACL - in router




















...







