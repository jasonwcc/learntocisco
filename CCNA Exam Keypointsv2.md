,,,
AAA
- Authentication : username + password / identity
- Authorization  : tasks / capabilities / permissions
- Accounting : log, record


ACL
- read from top down
- extended ACL nearer to source
- standard ACL nearer to destination
- permit any any always at bottom of ACL

Collapsed-Core
- combined distribution and core layer devices into one
- reduce cost and complexity design
- used by small to medium size companies

Controller-Based Networking
- centralized configuraiton, monitoring, management
- leverage controllers to handle network management and configurations
- automation of devices (networks) and services
- like Cisco DNA Center

CDP
    can used to discover only cisco neigbor devices
    enabled globally
    question says enable on particular interface
en 
conf t 
	no cdp run 
	int g0/1 
		cdp enable 
vs LLDP
    can used to discover multi-vendor neighbor devices
    not enabled globally
    question says enable on particular interface en conf t int g0/1 lldp receive/transmit



DHCP
- DORA Discover Offer Request and Acknowledge
- when conflict - ip is removed
- Relay Agent 
  To see relay agent / helper address # show ip interface
- Lease : list of ip assigned to clients
   \# show ip dhcp bindings
- Pool :  list of ip available 
   \# show ip dhcp pool

DNS
- resolve FQDN/hostname into IP
- TCP/53 and UDP/53


Dynamic ARP Inspection (DAI)
- prevent man-in-the-middle attack

# Dynamic Trunking Protocols (DTP)
- Dynamic Desirable 	+ Dynamic Desirable	= Trunk
- Dynamic Desirable	+ Dynamic Auto		= Trunk
- Dynamic Desirable	+ Trunk			= Trunk
- Dynamic Desirable	+ Access		= Access
- Dynamic Auto		+ Dynamic Desirable	= Trunk
- Dynamic Auto		+ Dynamic Auto		= Access
- Dynamic Auto		+ Trunk			= Trunk
- Dynamic Auto		+ Access		= Access



Enable Secret 
enable secret cisco : complete control, similar to enable secret privilege 15 cisco
or
enable secret privilege zero aaa111 : only logout, enable, disable, help and exit
enable secret privilege user bbb222 : limited read-only access to router
enable secret privilege 15 ccc333     : complte control

EtherChannel / LACP /PAGP
    LACP (universal) mode : active/passive
    PAGP (cisco) mode : auto/desirable
    Static mode : on


Fibre-optics

First hop redundancy protocol (FHRP)
- HSRP
- VRRP
- GLBP
- Default Mac address configured
  - HRSP - 00:00:0c:...
  - VRRP - 00:00:5x:...
  - GLBP - 00:06:xx:...

FTP
- TCP/20 and TCP/21
- send data plain text
- has separate control and data connections
- requires authentication / username+password

Interface - slow / poor performance
- lots of CRC/frame 	: physical / hw error
- lots of collision 	: duplex mismatch
- lots of runts		: small frame (<64 bytes)
- lots of giants	: large frame (>mtu)
- late collision	: occurs in first 64 bytes. 
- Example Q234, 829

IPv4
- Private IPv4 address
  : conserve public address
  : always private, cannot route to internet
  : unless configured with NAT to be translate into public

IPSEC vs GRE
- IPSEC 
  : is unicast traffic, better security
- GRE
  : support multicast traffics, less secure
- hence GRE with IPSEC to have both 

IPv6 addresses type
1 global
  - routable all to the way out to internet
  - 200x:x:/3
2  link local
  -    fe80::/10
  -   no routeable to another network/internet
3      site-local
  -    fc/fd:xx
  -    routable to another network within intranet
4 multicast
 -    ffxx
5 loopback
     :   ::1
6 unknown
     :   ::

JSON
- define/describe structured data including arrays
- Starts/ends with curly braces {} a name/value pairs consists of field name (in double quotes), followed by colon and values
- Example: [ {"load balancer": "LB1", "port": "fe2/0"}, {"firewall": "FW20", "port": "fe3/1"}, {"router": "R41", "port": "fe8/5"}, ]
- Keys: load balancer, firewall, router
- Values: LB1, fe2/0, FW20, fe3/1, R41, fe8/5
- Array: enclosed within [] and consists of multiple values separated by coma "numbers": [23, 44, 76, 34, 98] "employees": ["ali", "chong", 'murthi"]
- Boolean: true, false
- Object: unordered set of attribute-value pairs {"data": ["fe0/3", "fe0/1", "fe0/2"]}

NAT
static nat
config) # ip nat source static ....
dynamic nat
config) # access-list ...
config) # ip nat pool static ....
pat
config) # ip nat  ... overload

NTP
- configure as server # ntp master 4 (stratum level)
- configure as client # ntp server <master-ip>
- UDP/123

OSPF 
- best path : bandwitdh
- if all bandwitdh same : load-balance all routes

QOS
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
  config terminal
  	hostname demo1
		ip domain-name abc.com
		username sam password ABC!23
		username mary password ABC!23
		crypto key generate rsa 
	line vty 0 15
		transport input ssh
		login local
		
Spanning Tree (PVST+ or Rapid PVST+)
- one spanning tree instance for each VLAN
- Elect Root bridge
  1. Lowest priority number (0 - 61440)
  2. Lowest MAC address 

SYSLOG
- UDP/514
- use command to set #logging trap level
- lower level will send all messages

Severity Level:
- 0 Emergencies (Every) System unstable / System shutting down due to missing fan tray / 
- 1 Alerts (Awesome) Immediate action needed / Temperature limit exceeded
- 2 Critical (Cisco) Memory allocation failures
- 3 Errors (Engineer) Interface Up/Down messages
- 4 Warnings (Will) Configuration file written to server, via SNMP request
- 5 Notifications (Need) Normal but significant condition / Line protocol Up/Down
- 6 Information (Ice Cream)list violation logging
- 7 Debugging (Daily) Appears during debugging only

TCP
- reliable, statefull, connection-oriented (three way handshake)
- use sequential, acknowledge
- has control bits 
- can use checksum
- ftp, smtp, ssh, www, database, pop3, dns

TFTP
- UDP/69
- backup Cisco IOS or configuration/nvram to TFTP server
- upgrade Cisco IOS
- convenient : no need authentication / username+password

UDP
- unreliable, stateless, connection-less
- can use checksum
- fast, less overhead
- snmp, tftp, voice, audio, dns, NTP

VLAN hopping attacks
- to mitigate / protect :
  1. VLAN ACL (VACL)
  2. change native/default VLAN 1 to unused VLAN ID
  3. Configure as trunk port
  4. Disable DTP

WPA
- TKIP/MIC encryption

WPA-2
- only 8-63 ASCII characters or 64 HEXADECIMAL characters
- 128 bits
- use pre-shared key

WPA-3
- AES : for encryption 
- SAE : Simultaneous Authentication of Equals
  - is resistant to dictionary and brute force attacks
- relies on Perfect Forward Secrecy 










,,,
