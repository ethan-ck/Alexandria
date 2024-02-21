- Remember the subnet masks
- We need more networks (fucking business people)
	- Compartmentalize for security reasons 
- 1 - 126 is class A, 255.0.0.0 
- 128 - 191 is class B, 255.255.0.0
- 192 - 223 is class C, 255.255.255.0 
- 127 is the local loopback 

- Private Address (non-routable IP addresses)
	- Class A is 10.x
	- Class B is 172.16.x.x to 172.31.x.x
	- Class C is 192.168.x.x
	- APIPA is a special one that is non-routable, this means that something is wrong with the DHCP server 
		- Range is 169.254.x.x
		- Automatic Private 
	- 127.0.0.0 is the local loopback 

- Other Important Info 
	- IPV4 - has 4 billion addresses
	- IPV6 - 4 billion x 4 billion addresses 
	- Minimum need to get on the internet is to have an IP address and Subnet mask 
	- 255 is for network, 0's are for hosts
		- Ex. Class A Subnet Mask 255.0.0.0 is one network for multiple hosts 

- Subnet Black Magic
	- For subnetting, we can take 2 octets in the binary system
		- 00 = 0, 01 = 64, 10 = 128, 11 = 192
		- We borrow the 2 left most binary digits, 128 and 64
		- For example, if we need to divide 10.0.0.0 into 4 subnets 
			- The 4 subnet masks become:
			- 10.0.0.0
			- 10.64.0.0
			- 10.128.0.0
			- 10.192.0.0

- Supernetting (Super black magic)
	- Goes the other way, for when we need more hosts per network 
	- We still steal bits form network octet, but we use shorter masks to combine into larger address spaces
	- If you see a subnet mask that has a number other than 255 or 0, it's most likely supernetting 
	- We have networks and hosts
		- Class A = 1 network, 3 hosts
		- Class B = 2 network, 2 hosts
		- Class C = 3 network, 1 host

- (Apple) CIDR (Classless Inter Domain Routing)
		- Remember 32 bits 
	- Allows VLSM ( Variable Length Subnet Mask)
		- ex. 192.168.11.3/24
			- Means that the 255.255.255.0 default subnet is used 
			- 24 is divisible by 
		- ex. 192.168.11.3/20 
			- Means that 255.255.240 VLSM is used (It lost 4 bits) (these are called classless)
	- Usually we will only see /8, /16, or /24. Class A, Class B, Class C  (Classful)

- Subnet Part 1 Video Notes
	- "Taking a lake and breaking it into several ponds"
		- Benefits include
			- Increased security
			- network management 
			- network performance
			- separation 
	- "how many bits do I have to steal?"
	- "Interesting octet", the host id begins with it x.x.x.192
	- Remember the subnetting formula 
		- (enter formula here)
		- Remember we subtract two addresses for the network and broadcast addresses)

- Subnet Part 2 Video Notes (Supernetting)
	- Fixed length subnet masking
	- Variable Length Subnet Masking
	- 



- First 14 labs in chapter 4
- OSI Model quiz (5 times)