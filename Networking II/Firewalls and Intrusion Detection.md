
# Intrusion Detection Systems

- Best practice is to use both an IDS, and a firewall. IDS do not prevent intrusions, but detects them. An example of an IDS is an anti-virus. 

- IDS usually detects intrusions through two different methods:
	- Signatures
		- Known malicious actors
	- Anomalies
		- Not normal (baseline)

- HIDS
	- Host Intrusion Systems
		- Only one device
- NIDS 
	- Network Intrusion Systems
		- For the whole network

# Intrusion Prevention Systems

- Similar to a firewall, but the same. Will detect and prevent malicious actors

# Firewalls

- A software or hardware-based network security system that allows or denies network traffic according to a configured set of rules.
	- Configured access control lists (ACLs) that filters traffic to permit or deny 
		- These ACLs are usually found on a router

- Hardware Firewalls
	- Usually a router
	- Network, protects the devices in a network from the untrusted internet 

- Software Firewall
	- Protects a single computer or device 

- Access Control Lists (ACLs)
	- Implicit Deny
		- Blocks everything not found by the AC

- Firewall Types
	- Packet Filtering (Network Layer)
		- Filters source (src) and destination (dest) IP addresses, ports and protocols (srvcs), 
		- Also known as stateless, as the state is associated with the session layer
		- More detailed than other types, looks at the IP's header (source and destination IP address)
	- Circuit Level Gateways (Session Layer)
		- Allows or denies sessions (connection state) 
		- Known as stateful, which describes the process of SYN-ACK, the 3-way handshake
		- Slower 
	- Application Layer Firewall (Application Layer)
		- Filters by content (HTTP and URLs)
		- Data
		- Slowest 
	- Proxy Server (Application Firewall)
		- Acts as a stand-in to public and private networks
			- Voting by proxy example (You have permission to vote for someone to their wishes)
		- IN or OUT, caches content for better performance
		- Hides the private network 
			- VPN, connects to a proxy server and hides your personal IP from the internet
	- Reverse Proxy Server
		- Internet to Private Network
		- Used for load-balancing and caching

# Firewall Design and Implementation

- All-in-One, Network Security Appliance (NSA), Unified Threat Management (UTF) all meant the same thing
	- Includes Firewalls, IDS, and IPS 

- Screened Subnet or DMZ
	- A buffer network (subnet) that sits between the private network and an untrusted network

- Routed Firewall
	- Layer 3 router, supports multiple interfaces and transmit data as a router hop

- Transparent Firewall
	- Operates at layer 2 and is not seen as a router hop by connected devices

- UTM Devices
	- Firewall
	- VPNs
	- Anti-Spam
	- Anti-Viruses 
	- Load balancing
	- Single point of failure 
	- URL Filtering
	- Content Inspection of websites
	- IDS and bandwidth shaping

- Firewall Features
	- Encryption
	- User auth
	- Etc...

- Interfaces
	- A way in and out of a device

- Two Firewalls to separate a high security zone (private network), low security zone (web server), and a unsecure zone (internet)

- One firewall with multiple interfaces set up 

- 


