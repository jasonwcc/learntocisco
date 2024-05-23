'''
Examtopics #1061
!SW1 - solution
en
conf t
	ip dhcp snooping vlan 10
	int fa0/1
		no ip dhcp snooping information option
      end
wr

PassLeader - Simulation Q683
!R1 - pre-configured
en
conf t
	hostname R1
	int g0/0
		ip add 10.10.12.1 255.255.255.0
		no shut
	int g0/1
		ip add 10.10.13.1 255.255.255.0
		no shut
	router ospf 1
		network 10.10.12.0 0.0.0.255 area 0
		network 10.10.13.0 0.0.0.255 area 0
	end
wr

!R2 - pre-configured
en
conf t
	hostname R2
	router ospf 1
		network 10.10.12.0 0.0.0.255 area 0
		network 10.10.23.0 0.0.0.255 area 0
	!
	int g0/0
		ip add 10.10.12.2 255.255.255.0
		no shut
	int g0/2
		ip add 10.10.23.2 255.255.255.0
		no shut
	end
wr

!R3 - pre-configured
en
conf t
	hostname R3
	router ospf 1
		network 10.10.13.0 0.0.0.255 area 0
		network 10.10.23.0 0.0.0.255 area 0
	!
	int g0/1
		ip add 10.10.13.3 255.255.255.0
		no shut
	int g0/2
		ip add 10.10.23.3 255.255.255.0
		no shut
	end
wr


!R1  - solution
en
conf t
	!configure loopback
	int loopback 0
		ip add 10.10.1.1 255.255.255.255
	int loopback 1
		ip add 192.168.1.1 255.255.255.0
	router ospf 1
		router-id 10.10.12.1
		network 10.10.1.1 0.0.0.0 area 0
		network 192.168.1.1 0.0.0.0 area 0
		passive-interface g0/1
		end
copy run start


!R2  - solution
en
conf t
	!configure loopback
	int loopback 0
		ip add 10.10.2.2 255.255.255.255
	int loopback 1
		ip add 192.168.2.2 255.255.255.0
	!
	router ospf 1
		router-id 10.10.12.2
		network 10.10.2.2 0.0.0.0 area 0
		network 192.168.2.2 0.0.0.255 area 0
	!
	int g0/0
		ip ospf priority 255
	!
	int g0/2
		ip ospf priority 255
	end
copy run start
clear ip ospf process 

!R3  - solution
en
conf t
	int loopback 0
		ip add 10.10.3.3 255.255.255.255
	int loopback 1
		ip add 192.168.3.3 255.255.255.0
	!
	router ospf 1
		network 10.10.3.3 0.0.0.0 area 0
		network 192.168.3.3 0.0.0.0 area 0
		passive-interface g0/1
		end
copy run start
clear ip ospf process 

PassLeader - Simulation Q684
!pc1 - preconfigured with IP
192.168.1.101

!pc2 - preconfigured with IP
192.168.1.102

!sw1  - solution
en
conf t
   vlan 15
   exit
   int range g1/0/1-2
	channel-group 1 mode active
   int port-channel 1	
	switchport trunk encapsulation dot1q
	switchport mode trunk
	switchport trunk native vlan 15
	end
copy run start

!sw2  - solution
en
conf t
   vlan 15
   exit
   int range g1/0/1-2
	channel-group 1 mode active
   int port-channel 1	
	switchport trunk encapsulation dot1q
	switchport mode trunk
	switchport trunk native vlan 15
	end
copy run start

!sw1 - verify all physical connected ports is up and running
show ip int brief

!sw1 - verify port-channel is configured correctly with LACP
show etherchannel summary

!pc1 - test ping to pc2
ping 192.168.1.102


PassLeader - Simulation Q685
!R1 - preconfigured
en
conf t
  hostname R1
  int g0/0
      ip address 192.168.1.9 255.255.255.0
      no shut
      end
wr

!R2 - preconfigured
en
conf t
  hostname R2
  int g0/0
      ip address 192.168.1.10 255.255.255.240
      no shut
      end
wr

!R1  - solution
en
conf t
  int g0/1
    ip address 192.168.1.17 255.255.255.240
    ipv6 address 2001:db8:aaaa::1/64
    ipv6 unicast-routing
    no shut
    end
wr

!R2  - solution
en
conf t
  int g0/1
    ip address 192.168.1.30 255.255.255.240
    ipv6 address 2001:db8:aaaa::2/64
    ipv6 unicast-routing
    no shut
    end
wr

!R1 - test ping to R2
ping 192.168.1.30
ping 2001:db8:aaaa::2


PassLeader - Simulation Q686
!R1 - preconfigured
en
conf t
  hostname R1
  int g0/0
      ip add 209.165.200.225 255.255.255.252
      no shut
  int loopback 1
      ip add 192.168.1.1 255.255.255.0
  ip route 192.168.3.0 255.255.255.0 209.165.200.226
  ip route 209.165.200.228 255.255.255.252 209.165.200.226
  end
wr


!R2 - preconfigured
en
conf t
  hostname R2
  int g0/0
      ip add 209.165.200.226 255.255.255.252
      no shut
  int g0/1
      ip add 209.165.200.229 255.255.255.252
      no shut
  int g0/2
     ip add 209.165.200.229 255.255.255.252
     ipv6 add 2001:db8:abcd::1
     no shut
  int loopback 1
     ip add 192.168.1.1 255.255.255.0
  ip route 192.168.1.0 255.255.255.0 209.165.200.225
  ip route 192.168.3.0 255.255.255.0 209.165.200.230
  end
wr

!R3 - preconfigured
en
conf t
  hostname R3
  int g0/1
     ip add 209.165.200.230 255.255.255.252
     no shut
  int loopback 1
     ip add 192.168.3.1 255.255.255.0
  end
wr


!R4 - preconfigured
en
conf t
  hostname R4
  int g0/2
     ip add 209.165.200.230 255.255.255.252
     ipv6 add 2001:db8:abcd::2
     no shut
  end
wr

!R3  - solution
en
conf t
   ip route 192.168.1.0 255.255.255.0 g0/1
  end
wr

!R2  - solution
en
conf t
   ip route 0.0.0.0 0.0.0.0 209.165.202.130
   ipv6 route ::/0 2001:db8:abcd::2
  end
wr

!R3 - Verify configuration and ping test to loopback address on R1
sh ip route
ping 192.168.1.1

!R2 - Verify routing table for both ipv4 and ipv6 
sh ip route
sh ipv6 route


PassLeader - Simulation Q687
!SW2 - preconfigured
en
conf t 
   vlan 99
      name Available
      end
wr



!SW1 - solution
en
conf t
  	vlan 100
            name Compute
	 vlan 200
		name Telephony
	!
	int fa0/1
		switchport mode access
		switchport voice vlan 200
		switchport access vlan 100
	!
	int g0/1
		switchport mode access
	end
wr

!SW2 - solution
show vlan
! look for Available vlan ID . Which is 99.
en
conf t
	int fa0/1
		switchport mode access
		switchport access vlan 99
		no cdp enable
	end
wr

!There is nothing to test since all end points is connected to different vlans, just verify configuration

!SW1 & SW2
show vlan
show int trunk

PassLeader - Simulation Q688
!Sw1 - solution
en
conf t
	vlan 210
		name FINANCE
	!
	interface FastEthernet0/1
		switchport access vlan 210
	 	switchport mode access
	!
	int fa0/2
		switchport  trunk encapsulation dot1q
		switchport mode trunk
		switchport trunk allowed vlan 210
		end
wr



!Sw2 - solution
en
conf t
	vlan 110
		name MARKETING
	vlan 210
		name FINANCE
	!
	interface FastEthernet0/1
		switchport access vlan 110
		switchport mode access
	!	
	int range fa0/2
		switchport  trunk encapsulation dot1q
		switchport mode trunk
		switchport trunk allowed vlan 210
	!
	interface FastEthernet0/3
		switchport trunk encapsulation dot1q
		switchport mode trunk
		switchport trunk allowed vlan 110,210
	end
wr

!Sw3 - solution
en
conf t
	vlan 110
		name MARKETING
	vlan 210
		name FINANCE
	!
	interface FastEthernet0/1
		switchport access vlan 210
		switchport mode access
	!
	interface FastEthernet0/2
		switchport access vlan 110
		switchport mode access
	!
	interface fa0/3
		switchport  trunk encapsulation dot1q
		switchport mode trunk
		switchport trunk allowed vlan 110,210
	end
wr




PassLeader - Simulation Q689
!R1 - preconfigured
en
conf t
	hostname R1
	int loopback 1
		ip add 192.168.1.1 255.255.255.0
	int g0/0
		ip add 10.1.2.1 255.255.255.0
		no shut
	int g0/1
		no ip add
		shut
	int g0/2
		ip add 10.1.3.1 255.255.255.0
		no shut
	!Default route back to R3 for NAT testing
	ip route 0.0.0.0 0.0.0.0 10.1.2.2

	end
wr

!R2 - preconfigured
en
conf t
	hostname R2
	enable password Cisco
	int loopback 1
		ip add 192.168.2.1 255.255.255.0
	int g0/0
		ip add 10.1.2.2 255.255.255.0
		no shut
	int g0/1
		ip add 10.2.3.2 255.255.255.0
		no shut
	int g0/2
		no ip add
		shut
	!Static route to R1's loopback1 via R2
	ip route 192.168.1.0 255.255.255.0 10.1.2.1
	end
wr

!R3 - preconfigured
en
conf t
	ip domain-name test.com
	hostname R3
	int loopback 1
		ip add 192.168.3.1 255.255.255.0
	int g0/1
		ip add 10.2.3.3 255.255.255.0
		no shut
	int g0/2
		no ip add 
		shut
	!Static route to R1's loopback1 via R2
	ip route 192.168.1.0 255.255.255.0 10.2.3.2
	ip route 10.1.2.0 255.255.255.0 10.2.3.2
	end
wr

!R1 - solution
en
!Task 2
clock set 00:00:00 1 jan 2019
conf t
	!Task 2
	ntp master 1
	!Task 3
	ip dhcp pool TEST
		network 10.1.3.0 255.255.255.0
	!Task 3
	ip dhcp excluded-address 10.1.3.1 10.1.3.10

!R2 - solution
en
conf t
	!Task 1
	ip access-list standard NAT
		permit 10.1.3.0 0.0.0.255
		permit 10.2.3.0 0.0.0.255
		permit 192.168.3.0 0.0.0.255
	!Task 1
	ip nat inside source list NAT interface g0/0
	!Task 2
	ntp server 10.1.3.1
	end
wr

!R3 - solution
en
conf t
	!Task 3
	int g0/2
		ip address dhcp
		no shut
	!Task 4
	username root password Cisco
	!Task 4
	line vty 0 4
		transport input ssh
		login local
	!Task 4
	crypto key generate rsa 
	<enter 1024 when prompted for how many bits in the modulus>
	end
wr

PassLeader - Simulation Q690
!Internet-GW - preconfigured
en
conf t
hostname Internet-GW
!
interface Loopback0
	ip address 172.20.20.129 255.255.255.128
!
interface GigabitEthernet0/1
	ip address 10.10.254.254 255.255.255.0
	no shut
!
router ospf 1
	network 172.20.20.128 0.0.0.127 area 0
	network 10.10.254.0 0.0.0.255 area 0
	end
wr

!R1 - solution
en 
conf t
hostname R1
interface Loopback0
	ip address 10.10.1.1 255.255.255.0
!
interface GigabitEthernet0/0
	ip address 10.10.13.1 255.255.255.0
	no shut
!
interface GigabitEthernet0/1
	ip address 10.10.12.1 255.255.255.128
	no shut
!
interface GigabitEthernet0/2
	ip address 10.10.12.129 255.255.255.128
	no shut
!
router ospf 1
	network 10.10.0.0 0.0.255.255 area 0
	end
wr


!R2 - solution
en
conf t
hostname R2
interface GigabitEthernet0/0
	ip address 192.168.0.2 255.255.255.0
	no shut
!
interface GigabitEthernet0/1
	ip address 10.10.12.2 255.255.255.128
	no shut
!
interface GigabitEthernet0/2
	ip address 10.10.12.130 255.255.255.128
	no shut
	end
wr


!R3 - solution
en 
conf t
hostname R3
interface GigabitEthernet0/0
	ip address 10.10.13.3 255.255.255.0
	no shut
!
interface GigabitEthernet0/1
	ip address 10.10.254.3 255.255.255.0
	no shut
!
router ospf 1
	network 10.10.0.0 0.0.255.255 area 0
	end
wr

!SW1
en
conf t
	hostname SW1
!
interface Vlan1
	ip address 192.168.0.1 255.255.255.0
	no shut
	end
wr



















