```
[
https://trainocate.com/manage-attendance?ClassId=6685

Download materials -
https://github.com/jasonwcc/learntocisco
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
    ip default-gateway 20.0.0.254
    no shut
    end
copy run start

Verify
Sw1 ping 10.0.0.1, 10.0.0.2, 10.0.0.253, 20.0.0.254/253



  



















)
...
