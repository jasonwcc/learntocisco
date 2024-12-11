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

Enable/Disable CDP/LLDP





*** Network Topology configuration ***
PC1 - 10.0.0.1
PC2 - 10.0.0.2
PC3 - 20.0.0.3
PC4 - 20.0.0.4
PC5 - 30.0.0.5
SW1 - 10.0.0.253
SW2 - 20.0.0.253
SW3 - 30.0.0.253
RO1 g0/0 10.0.0.201
RO1 g0/1 20.0.0.201
RO2 g0/0 10.0.0.202
RO2 g0/1 30.0.0.202

!ro1
en 
conf t
int g0/0
ip add 10.0.0.201 255.0.0.0
int g0/1
ip add 20.0.0.201 255.0.0.0
end
!ro2
en 
conf t
int g0/0
ip add 10.0.0.202 255.0.0.0
int g0/1
ip add 30.0.0.202 255.0.0.0
end
!ro3
en 
conf t
int g0/0
ip add 30.0.0.203 255.0.0.0
end

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
end
copy run start

!on all switch, reconfigure default-gateway



























...
