
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
			- 
	- Assignment Methods 