```

AAA
- Authentication : username + password / identity
- Authorization  : tasks / capabilities / permissions
- Accounting : log, record


Access Control List (ACL)
- read from top down
- extended ACL nearer to source
- standard ACL nearer to destination
- by default deny any any rule is at bottom of ACL
- must have at least one permit rule
- 
Collapsed-Core
- combined distribution and core layer devices into one
- reduce cost and complexity design
- used by small to medium size companies

Controller-Based Networking
- centralized configuration, monitoring, management
- leverage controllers to handle network management and configurations
- automation of devices (networks) and services
- like Cisco DNA Center

Cisco Discovery Protocol (CDP)
- Layer 2 protocol
- can used to discover only cisco neigbor devices
- enabled globally
- question says enable on particular interface
- Configuration

CDP Configuration
```
en 
conf t 
(conf)#	no cdp run  # disable globally
(conf)#	int g0/1 # enable per interface
(conf-if)# cdp enable 
```
vs Link-Layer Discovery Protocol (LLDP)
- can used to discover multi-vendor neighbor devices
- not enabled globally
- question says enable on particular interface en conf t int g0/1 lldp receive/transmit

EtherChannel / LACP /PAGP
- LACP (universal) mode : active/passive
- PAGP (cisco) mode : desirable/auto
- Static mode : on

First hop redundancy protocol (FHRP)
- Three type: HSRP, VRRP, GLBP
- Default Mac address configured
  -- HRSP - 00:00:0c:...
  -- VRRP - 00:00:5x:...
  -- GLBP - 00:06:xx:...
- HSRP
  : Active and Standby routers
  : Cisco propietory
- VRRP
  : Master and Backup routers
  : vendor neutral
Dynamic Host Configuration Protocol (DHCP)
- DORA Discover Offer Request and Acknowledge
- when conflict - ip is removed
- Relay Agent 
  To see relay agent / helper address 
```
# show ip interface
```
- Lease : list of ip assigned to clients
```
# show ip dhcp bindings
```
- Pool :  list of ip available 
```
# show ip dhcp pool
```

Domain Name Service (DNS)
- resolve FQDN/hostname into IP
- TCP/53 and UDP/53


Dynamic ARP Inspection (DAI)
- prevent man-in-the-middle attack

Enable Secret 
- complete control, similar to enable secret privilege 15 cisco:
```
# enable secret cisco
```
or
- User can only logout, enable, disable, help and exit
```
# enable secret privilege zero aaa111
```
- Limited read-only access to router
```
# enable secret privilege user bbb222 
```
- User have complete control
```
# enable secret privilege 15 ccc333
```

Fibre-optics

FTP
- TCP/20 and TCP/21
- send data plain text
- has separate control and data connections
- requires authentication / username+password

JSON
- define/describe structured data including arrays
- Starts/ends with curly braces {} a name/value pairs consists of field name (in double quotes), followed by colon and values
- Example:
[
{"load balancer": "LB1", "port": "fe2/0"},
{"firewall": "FW20", "port": "fe3/1"},
{"router": "R41", "port": "fe8/5"},
]
- Keys: load balancer, firewall, router
- Values: LB1, fe2/0, FW20, fe3/1, R41, fe8/5
- Array: enclosed within [] and consists of multiple values separated by coma
  "numbers": [23, 44, 76, 34, 98]
  "employees": ["ali", "chong", 'murthi"]
- Boolean: true, false
- Object: unordered set of attribute-value pairs
  {"data": ["fe0/3", "fe0/1", "fe0/2"]}
  
IEEE 802.1x
- provide security based on identity
- Combined with AAA solution, it can provides authentication and configuration for both wireless and wired network
- Layer 2 security mechanism
- 
Interface - slow / poor performance
- lots of CRC/frame 	: physical / hw error
- lots of collision 	: duplex mismatch
- lots of runts		: small frame (<64 bytes)
- lots of giants	: large frame (>mtu)
- late collision	: occurs in first 64 bytes. 

IPv4
- Private IPv4 address
  - conserve public address
  - always private, cannot route to internet
  - unless configured with NAT to be translate into public
  - RFC 1918: 10.x.x.x, 172.16.x.x-172.31.x.x, 192.168.x.x
- Multicast (224.x.x.x - 239.x.x.x)
- loopback (127.x.x.x) 127.0.0.1
- unknown: 0.0.0.0

IPv6 addresses type
- global 
  - routable all to the way out to internet
  - 200x:x:/3
- link local
  - fe80::/10
  - no routeable to another network/internet
- site-local
  - fc/fd:xx
  - routable to another network within intranet
- multicast
  - ffxx
- loopback
  - ::1
- unknown
  - ::

IPSEC vs GRE
- IPSEC 
  : is unicast traffic, better security
- GRE
  : support multicast traffics, less secure
- hence GRE with IPSEC to have both 

Network Address Translation (NAT)
- Static nat
config) # ip nat source static ....
- Dynamic nat
config) # access-list ...
config) # ip nat pool static ....
- Pat or Port Address Translation
config) # ip nat  ... overload

LLDP
- Layer 2 protocol
- vendor neutral vs CDP (is Cisco propietory)
- by default it is disabled
- can be enabled on global, as well as on interface level
- 
 
Network Time Protocol (NTP)
- configure as server # ntp master 4 (stratum level)
- configure as client # ntp server <master-ip>
- UDP/123

Open Shortest Path First (OSPF) 
- best path : bandwitdh
- if all bandwitdh same : load-balance all routes

Quality Of Service (QOS)
- Low-Latency Queue (LLQ) : suited for voice and video
- Weighted Random Early Detection (WRED)
  : when queue is full then start dropping low priority packet
- Policing : implement by ISP 
  : limit both incoming and outgoing flow
  : Discards or re-marks packets
- Traffic Shaping 
	: limit bandwitdh that an outgoing flow can use
     : reschedules packets by delaying or queueing when traffic exceed limits
- Precision Queue (PQ) : congestion management : suited for voice 
- Class-Based Weighted Fair Queueing (CBWFQ) : congestion management

Port Security
- has 3 modes: protect, restrict and shutdown
- protect mode : temp disable port
- restrict mode : temp disable port + syslog + snmp + increment counter
- shutdown mode : permanent shutdown port + syslog + snmp + increment counter

RADIUS
- provides AAA services except it does support encrypt password 
- do not encrypt all traffic

Software Defined Networking (SDN)
1. Management plane
    - business criteria / conditions
2. Control plane
    - Routing configuration / decision
    - NAT configuration
    - ACL configuration
    - VLAN configuration
3. Data plane
    - switching using MAC address table
    - forward traffic according to routing from control plane
    - Vlan tagging / trunking
    - encrypt (VPN)
    - drop frame (if denied by ACL)
    - Change source IP (when configured with NAT)

SNMP
- is UDP/162
- MIB : collection of variables that can be monitored
- Agent: responds to status requests for information about a device
- Manager - resides on NMS
- Trap - unsolicited message

SSH
- TCP/22
- command:
 ``` 
  config terminal
  	hostname demo1
		ip domain-name abc.com
		username sam password ABC!23
		username mary password ABC!23
		crypto key generate rsa 
	line vty 0 15
		transport input ssh
		login local
```	
Spanning Tree (PVST+ or Rapid PVST+)
- one spanning tree instance for each VLAN
- Elect Root bridge
  1. Lowest priority number (0 - 61440)
  2. Lowest MAC address 
- spanning-tree vlan <number> root primary: only set priority to 24576. This still loses to priority 0
  
SYSLOG
- UDP/514
- use command to set #logging trap level
- lower level will send all messages
- Level: 
  - level 0 - Emergencies 	: Every	
  - level 1 - Alerts	: Awesome 
  - level 2 - Critical	: Cisco
  - level 3 - Errors	: Engineeer
  - level 4 - Warnings	: Will
  - level 5 - Notifications	: Need
  - level 6 - Informational	: Icecream
  - level 7 - Debug	        : Daily
			
- Example when to use each level:
  - 0 Emergencies System unstable / System shutting down due to missing fan tray / 
  - 1 Alerts Immediate action needed / Temperature limit exceeded
  - 2 Critical (default) Memory allocation failures
  - 3 Errors Interface Up/Down messages
  - 4 Warnings Configuration file written to server, via SNMP request
  - 5 Notifications Normal but significant condition / Line protocol Up/Down
  - 6 Information list violation logging
  - 7 Debugging Appears during debugging only

Transmission Control Protocol (TCP)
- reliable, statefull, connection-oriented (three way handshake)
- use sequential, acknowledge
- has control bits 
- can use checksum
- ftp, smtp, ssh, www, database, pop3, dns

Trivial File Transfer Protocol (TFTP)
- UDP/69
- backup Cisco IOS or configuration/nvram to TFTP server
- upgrade Cisco IOS
- convenient : no need authentication / username+password

User Datagram Protocol (UDP)
- unreliable, stateless, connection-less
- can use checksum
- fast, less overhead
- snmp, tftp, voice, audio, dns, NTP

VLAN
- default vlan: cannot change nor delete, always set to 1. all ports by default in vlan 1
- native vlan: untagged vlan, can be change. To secure management traffic such as prevent VLAN hopping attacks

VLAN hopping attacks
- Following method to mitigate / protect / prevent against VLAN hopping attacks:
  - VLAN ACL (VACL)
  - change native/default VLAN 1 to unused VLAN ID
  - Configure as trunk port
  - Disable DTP

WIFI Protected Access (WPA)
- TKIP/MIC encryption

WIFI Protected Access-Version 2 (WPA-2)
- only 8-63 ASCII characters or 64 HEXADECIMAL characters
- 128 bits
- use pre-shared key

WIFI Protected Access-Version 3 (WPA-3)
- AES : for encryption 
- SAE : Simultaneous Authentication of Equals
  - is resistant to dictionary and brute force attacks
- relies on Perfect Forward Secrecy 
- defends against brute force, deauthentication and disassociation attacks
- 
WLC
- centrally manage many AP
- enable "Protected Management Frame" to secure spoofed assoication request
- 

Rectified question with confirm answer:
205 D
206 C
212 BE
213 C
216 AE
227 B (the spelling toot supposed to be root)

243 B
245 A CAM table is MAC Address table
247 A (cisco is using grammar to test knowledge here. "passively" means auto, "must" means desirable
350 AD . why? bcos only two different network : 10.0.0.0 and 10.0.0.1. among the 10.0.0.0 OSPF wins
432 A 
719 BC
722 C (no semicolon, must use colon)
787 C (should be seven only by looking at curly braces {}
1231 C Layer 3 only means IP. All the answer choice has either Layer 2 or MAC
1281,1303 D Look for FFFE only
1297 A Look for lowest AD then lowest Metric

Look for following keywords:
JSON
longest prefix  > AD > Metrics
destined
ssh
```


