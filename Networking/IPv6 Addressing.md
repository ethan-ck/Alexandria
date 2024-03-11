
- COLD HARD FACTS about IPv6
	- There is an IP cloud company called Cloudflare
		- In Oct 2023, the company said that 36% of internet traffic is IPv6 
		- It's growing 
		- In Dec. 1998 the Internet Engineering Task Force created IPv6, in 2012, it went live. And  in 2017, it became the internet standard. 
		- IPv6 deals in multicasting, not broadcasting 
		-  

- IPv4 

- IPv6 Format
	- 128 Bit address
	- One or more blocks consist of all zeros, we can remove two consectutive blocks and replace it with ::, we can also remove the beginning zeros
		- Ex. 2001:0F56:0000:0000:C429:0008:0000:02D5
		- 2001:F56::C429:8:0000:2D5
		- IPv6 Prefix, usually the MAC address
		- Interface ID - used to identify the host 
			- EUI-64 
- IPv6 Components

- Dual Stack Configuration
	- Supports both IPv6 and IPv4 packets simultaneously
	- Sometimes we have to use Tunneling instead
		- Tunneling is when we have one packet inside another (encapsulate)
		- Sort of like VPNs 

- Teredo Tunneling
	- IPv6 inside IPv4 packets
	- Encapsulation/Decapsulation completed by each host

- 6to4 Tunneling
	- IPv6 packets inside an IPv4 packets
	- Encapsulation/decapsulation handled by routers

- ISATAP Tunneling
	- IPv4 Network and IPv6 Network, the dual-stack router converts the IPv4 packets to IPv6 and vice versa, like a translator. 

- IPv6 Assignment 
	- Address Types
		- Identified by the first two hexdigits 
		- Link-Local
			- Valid only on local subnet
			- Talk to hosts on same subnet only 
			- Cannot get past the switch
			- Similar to APIPA addresses
			- one will always be assigned
			- Starts with a hex value of FE 
		- Unique Local Address
			- Private, between sites or local network
			- FC00::/6 prefix
				- Look at those ::, they could be important
			- Starts with either FC 
			- ::1 is the local loopback for IPv6 
		- Global Unicast Address
			- Unique registered IPv6 address, one to many, broadcasts to all
			- Global routing prefix assigned by ISP 
			- public networks 
			- starts with 2003 (unfinished)
		- Multicast 
			- One to many
			- Unique for a set of devices, only devices that meet a specific function, will respond 
			- FF00::/8 prefix
			- FF02::/16 prefix aren't forwarded to the routers
		- Anycast 
			- Casts to literally any particular device, like DHCP servers across the globe
		- Loopback Address 
			- It loops 
			- ::1/128
			- Literally all zeros but with a 1/128 at the end
	- Assignment Methods 
		- Static Assignment
			- Static Full Assignment
				- Manually configure everything
			- Static-Partial Assignment
			- -DHCPv6  
				- Stateful autoconfiguration 
				- Stateless autoconfiguration (SLACK)

- Labs
	- Network and Sharing, it looks the same as the dialogue box for IPv4, but we are using IPv6 instead 

- Ping -6 
	- Ping always wants to ping IPv4 addresses, we have to specify to ping IPv6 addresses before we can ping 

- Internet
	- DNS
	- DHCP
	- IPv4 and IPv6 addresses

- IPv6 is 8 blocks of 4 hex-digits 

- Ipconfig /release 
	- Releases alias 
	
- Ipconfig /renew 
	fills alias 

DORA process (4 steps)

- Only do lab 4.9.5 2x (it's long) 
	- This lab wants you to make use of the command line tools, as well as use everything we learned (where do you look to find important information?) 
	- use PowerShell instead of command prompt 
	- How many hops? (Traceroute)
	- Remember the exhibits menu we get the IP address
	- 4 hops is the answer
	- The name of the device on the third hop is PF sense 
	- NIC port, lights are good 
	- ipconfig /all 
	- default gateway does not match, 