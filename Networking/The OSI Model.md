The OSI Model 

**All People Seem To Need Data Processing** 

The OSI Model has 7 layers:

Application - Integrate network services w / OS 
	- Has Multiple Protocols
		- HTTP 
		- FTP
		- SMTP
		- DNS
		- DHCP

Presentation - Data Format Encryption and Compression 

Session - Crate Session between Devices
	- Session-ID 

Transport - Delivers Data: Segment, Flow 
Control, Sequencing PORTS LIVE HERE 
	- PORT
	- Has two Protocols 
		- TCP
		- UDP 
	- PDU in this layer are called Segments

Network - Routes Data over Network 
	- IP Address 
	- Devices include a Router 
	-  Two Protocols:
		- IP 
		- ARP 
	- PDU is called Packet 

Data Link - Error checking [CRC]
	- MAC Address 
	- Devices include: 
		- a Switch
		- Wireless Application Protocol (WAP) 
		- Network Interface controller (NIC)
		- Bridge
	- PDUs are called Frames 

Physical - Puts Signal on Wire or Channel 
	- Devices include:
		- Hub
		- Repeater
	- PDUs are called Bits 

5 Look-Up Tables Encountered in Networking 

ARP 