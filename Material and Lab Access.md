## Material Access
```
URL : https://learningspace.cisco.com/
Sign up : personal email
Redeem : xxxxxxxxxxxxxx
Offline read: Download and install Cisco eReader
```

## Lab Access
Access to Cisco Learning Labs is via the Cisco Learning Labs Portal:
```
URL: https://cll-ng.cisco.com/users/pblogin

```


Credentials
```
Student: Darma
Username: 2021111340928
Password: Wgn6Tfm7

Student: Muhammad Azri
Username: 2021111340923
Password: YMx5hZ2L

Student:  Edfairzal
Username: 2021111340924
Password: HxsPrXvM

Student: Emilia
Username: 2021111340925
Password: 69y9Qxgx

Student: Wan Ahmad
Username: 2021111340926
Password: Ld6J5ffd

Student: Ahmad Afiq
Username: 2021111340927
Password: 7wG8FBKV

Student: Asnawi
Username: 2021111340929
Password: eHmrUkbB

Student: Thace
Username: 2021111340930
Password: C7CQKJLs

Student: Lim
Username: 2021111340931
Password: m3RADHRm

Student: Haikal
Username: 2021111340932
Password: Etat36sY

Student: Afiq Adha
Username: 2021111340933
Password: uJj7W6jp

Student: Oong
Username: 2021111340934
Password: 7jzeLunu

```

Equipment Passwords
```
Please do not change any of these passwords. 
Doing so will cause delays in providing support for your class should support be required. 
Any equipment password not indicated in the lab guide will be attached in the errata.
```

Notes day 1 to 5
```
3    | 0 --> 
0011 | 0010 -->
3 2
loopback interface
- ip address : OSPF DR election

trunk 
- allow multiple vlans
- switch / bridge
- interVlan (router)

vs
access 
- allow single vlans
- PC, server, router

dtp
dynamic trunking protocol -> configure trunk or not
- dynamic auto
- dynamic desireable

Sw1<->Sw2
DA 	  DA   = access
DA    access = access
DA    trunk  = trunk
DA    DD  = trunk
DD    access = access
DD    DD = trunk
DD    trunk = trunk

untagged

vlan 1 : native : 192.168.0.0/24
vlan 2 : hr     : 192.168.1.0/27

IEEE 802.1Q

DV
- RIPv1(classfull) & RIPv2 (classless) & RIPng
- IGRP
- Hop count
- Care about one thing - Routing Table (best route)
Link State
- OSPF & EIGRP & IS-IS
- MTU, BW, Delay, Txload/Rxload, reliability (255/255)
- Neightbor/adjancency table , Topology table (all routes), 
Routing table (best route)
- memory consumption
- cpu memory

Reference BW(100)
-------------    = 10
    BW (500)
	
	
en
conf t
  int g0/0
     bandwitdh 500
	 
STP - single STP for all VLANs
PVST+ - per VLAN STP
RSTP - rapid but single STP for all VLANs
PVRST+ - rapid per VLAN STP
MSTP - universal 

STP
- 16 bits priority
- 0 - 65535
PVST + VLAN
- 4 bits priority
  16 possible values
  0, 4096, 8192, 12xxx
- 12 bits VLANs

RAPID
1. Decide who is P/S root bridge
- Primary Root Bridge
vlan:  1-100 Switch3
vlan:  101-200 Switch0

- Secondary Root Bridge
vlan:  1-100 Switch0
vlan:  101-200 Switch3
  
2. Configure Port fast
- ports that is access mode (PC, Server, Router )

!switch3
en
conf t
  spanning-tree mode rapid-pvst
  spanning-tree vlan 1-100 root primary
  spanning-tree vlan 101-200 root secondary

  int range fa0/1-5
     switchport mode trunk
  int range fa0/6-24
     switchport mode access
	 spanning-tree portfast
	 end
wr
	 
!switch0
en
conf t
  spanning-tree mode rapid-pvst
  spanning-tree vlan 1-100 root secondary
  spanning-tree vlan 101-200 root primary
    
  int range fa0/1-5
     switchport mode trunk
  int range fa0/6-24
     switchport mode access
	 spanning-tree portfast
	 end
wr

!switch6
en
conf t
  spanning-tree mode rapid-pvst
  
  int range fa0/1-5
     switchport mode trunk
  int range fa0/6-24
     switchport mode access
	 spanning-tree portfast
	 end
wr


HSRP
- cisco
- active-passive

VRRP
- universal
- active-passive

Gateway Load Balance Protocol
- cico
- active-active

IP Adddres	: 192.168.5.193 - 222
CIDR/Netmask: /27n --> 255.255.255.224
usable first ip
usable last ip
? Wildcard    :          0.  0.  0. 31
? Network ID  : 192.168.5.192

192.168.5 .200
8n .8n .8n.3n 5c
192.168.5 .nnn ccccc
           110 11111  ==> 192.168.5.192 


Why wildcard, just use netmask?

Given 192.168.0.0/24, deny from 192.168.0.4  to 192.168.0.7. Configure the ACL
We need to determine networkID and wildcard mask

192.168.0.4	--> 0000 0100
..
..
192.168.0.7 --> 0000 0111
			--> nnnn nncc
NetworkID   --> 192.168.0.4
Wildcard    -->     0.0.0.3

access-list 1 deny 192.168.0.4 0.0.0.3 

Given 192.168.0.0/24, deny from 192.168.0.190 to 192.168.0.210  Configure the ACL
We need to determine networkID and wildcard mask

190 --> 1000 0000
207 --> 1100 1111
        nnnn cccc
		1100 0000 --> 192.168.0.192
		0000 1111 --> 0.0.0.

190
191
192 --> 192.168.0.192
...

access-list 1 deny host  192.168.0.190
access-list 1 deny host  192.168.0.191
access-list 1 deny 192.168.0.192 0.0.0.15
access-list 1 deny host  192.168.0.208
access-list 1 deny host  192.168.0.209
access-list 1 deny host  192.168.0.210


Deny following ips 
172.16.100.16, 
172.16.100.17, 
172.16.100.18, 
172.16.100.19, 
172.16.100.25,
172.16.100.26
.
172.16.100.30  

Configure the ACL
We need to determine networkID and wildcard mask

16 --> 0001 0000
30 --> 0001 1110
       nnnn cccc
	   16		 -> 172.16.100.16
            1111 ->  0.0.0.15

access-list 1 permit 172.16.100.20 0.0.0.0
access-list 1 permit 172.16.100.21 0.0.0.0
access-list 1 permit host 172.16.100.22
access-list 1 permit host 172.16.100.23
access-list 1 permit host 172.16.100.24
access-list 1 permit host 172.16.100.25
access-list 1 permit host 172.16.100.31
access-list 1 deny 172.16.100.16 0.0.0.15




172.16.100.0 0.0.15.255

0000 0000
0000 1111.1111 1111

172.16.96.0 --> 172.16.111.255


Given following ip addresses, configure acl to deny them

192.168.100.80
192.168.100.81
192.168.100.82
192.168.100.83
192.168.100.84
192.168.100.85
192.168.100.86
192.168.100.87

1. convert first and last ip into binary
0101 0000
0101 0111
2. Anding, find matching bit (left to right)
    01010 000
    01010 111
    ------ ---
	nnnnn ccc
3. Matched bits --> Network ID (all client bits turn to 0's)
	nnnnn ccc
	01010 000 --> 80
	
4. Unmatched bits --> Wild card mask 
   (all network bits turn to 0's, all client bits turn to 1's)
	nnnnn ccc
	00000 111 --> 0.0.0.7
	
Network ID: 192.168.100.80
Wildcard  : 0.0.0.7

```