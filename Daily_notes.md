```
Training Material
- email - subject : ccna student kit
  - redemption / license code
- google cisco learning network space

Course Start Date: 2026-04-06 01:00:00 (UTC)
Course End Date: 2026-04-10 13:00:00 (UTC)

Automatically Extended up to 90 days or 60 hours lab time
URL:  https://htdlab.cisco.com
 
Student Credentials :

Name: Amirun 
Username: FlavorfulHeraldry90
Password: TruthFlip-92L9Lt3

Name: Ammar (virt)
Username: SatireBotanical12
Password: DischargeClose!18rAwkb

Name: Dang (virt)
Username: SickleRedder31
Password: FustianLonging-52!dfx7

Name: Fikri (classroom)
Username: BasisDownhill46
Password: SmogWye#60b9nf7

Name: Michael (classroom)
Username: EmigrantLye51
Password: EmeritusPostage%90EW@Kr

Name: Arif (virt)
Username: SmokyFalcon90
Password: FermentMannered-669-V3b

Name: Naquib (virt) = Habib
Username: LoadCanyon44
Password: ThereinMiasma_49whw4P

Name: Faizal 
Username: CaucusLuscious49
Password: CallousFoment%19kavRp

Name: Hashemi
Username: SmidgenBeaklike66
Password: MutationTense?064bsuy

Name: Ain (virt)
Username: RavineHeterodox28
Password: HiltPractice!36@HaCe






Star 
- switch/router
- ethernet technology
- IEEE 802.3 wire
  - CSMA/CD access method
    -- if the collision detected
       then execute backoff algo

Wireless
- IEEE 802.11
  - CSMA/CA access method
    -- RTS / RTC


bandwidth vs speed

25GB, 40GB --> 1.6GB

9a- 10:30am
10:30-12:30pm
1:30pm-3:00pm
5pm

Physical (1) Please
Data link Do / MAC/ VLAN/STP-BPDU/VTP/CSMA/CD/switch/bridge
Network Not / IP / Router / ICMP / PING
Transport Trust / TCP / UDP
Session Sales (user login information)
Presentation  Person (format ASCII / EBCDIC)
Application (7th) Please email / telnet /ssh/http/https/ftp/ftps/tftp

ethernet II frame


Remote lab
- htdlab.cisco.com
- guided lab
- 90 days or 60 hours
- 
vs
local lab
- cisco packet tracer
- netacad.com



<tab> <tab>
?
enter = <cr>

ctrl+z : end
ctrl+c : cancel
ctrl+a : place cursor at start of line
ctrl+e : place cursor at end of line
ctrl+w : delete last word
ctrl+u : erase everything to left from current cursor position
ctrl+k : erase everything to right from current cursor position


ctrl+shift+6,.
ctrl+^

LAN
- 
vs
WAN
- subscribe to SP

Straight-thru (different device type)
- PC-SW/HB
- RO-SW
- Server-SW/HB
Crossover (same device type
- PC-PC
- PC-SERVER
- SW-HB

IPv6
- 128 bits
  2^128
IPv4 car number plate
- 32 bits (2^32)
  0.0.0.0 -- 255.255.255.255
- decimal
- Layer 3
- logically
- can change frequently
- routable
vs
MAC engine chassis number
- 48 bits
- hexadecimal
- first 24 bits (assigned by IEEE)
- last 24 bits (assigned by the vendor)
- Layer 2
- physically (ROM)
- cannot change (unless vmac)
- non-routable



CPU GHz

DRAM (MB)  GHz
- contain run (live configuration)
- contain IOS

Flash drive (MB) microsecond
- internal drive
- cisco ios.bin
- html
- vlan database
- ui binary/library/

NVRAM (KB) 
- store (saved configuration)
- show start / copy run start /  write mem

Network ports 
- MB/GB - ms

rom mon
- reset password

copy run (dram) start(nvram)

boot
make gila gila configuration

copy start (nvram)  run(dram)
- restore original configuration


IP address
Subnet mask


x 0/1
xy 00,01,10,11

abcd
000
001
010
011
100
101
110
111


2^n


binary 0/1
decimal 0-9
octal 0-7
hexadecimal  0-9,A-F

A-10
B-11
C-12
D-13
2|C --> binary --> decimal
00101100 -> 44

hexadecimal < binary < 100
0110 | 0100
6 4



172.16.12.22/27n

8n.8n.8n.3n 5c
255.255.255.224
172.16.12.31

IPv6
FFxx:xxxx:x... Multicast
2xxx           Global unicast

IPv4
A 0.x.x.x/8 (255.0.0.0)   - 127.255.255.255
  8n.8c.8c.8c - fixed first bit
  0nnn nnnn.cccc cccc.cccc cccc.cccc cccc
  0000 0000
  0111 1111.1111
B 128.x.x.x/16 (255.255.0.0) - 191.x.x.x
  8n.8n.8c.8c - fixed first two bits

C 192.x.x.x/24 (255.255.255.0) - 223.x.x.x
  8n.8n.8n.8c - fixed first three bits
  110n nnnn.nnnn nnnn.nnnn nnnn.cccc cccc
D 224.x.x.x - 239.x.x.x
              - fixed first four bits
  1110 xxxx.xxxx....

E 240.x.x.x - 255.x.x.x Reserved for future use


AND
OR
XOR

RFC 1918
- must be NAT (translated) in order to connect to the internet




Router
- routing
- forwarding





ARP
- resolve IP into MAC

router use ARP find MAC based on IP


https://github.com/jasonwcc/learntocisco/



1. different routing protocol
- then we look at AD (lowest win)
2. same routing protocol
- then we look at metrics 
3. same routing protocol and metrics
- then we look at longest prefix

router
192.168.1.128/28 via 1.1.1.1
192.168.1.0/28 via 2.2.2.2
192.168.1.0/24 via 2.2.2.2

192.168.2.0/16 via 3.3.3.3
192.168.2.0/18 via 1.1.1.1

user wants to go to 192.168.1.207, which route it will use?


EIGRP us BW + DELAY ==> Feasible Distance value (5-6 digits)


128
nnnn cccc
1011 1111 = 191


Enable LLDP globally
en
conf t
lldp run

Enable LLDP on g0/0
- int g0/0
    lldp receive
    no lldp transmit

169.254.x.y

DHCP --> APIPA

Static X DHCP X APIPA
```



1`
