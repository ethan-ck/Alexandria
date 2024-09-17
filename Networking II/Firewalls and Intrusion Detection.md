
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
		- More detailed than other types, looks at the IP's header and source 
	- Circuit Level Gateways (Session Layer)
		- Allows or denies sessions (connection state) 
		- Known as stateful, which describes the process of SYN-ACK, the 3-way handshake
		- Slower 
	- Application Layer Firewall (Application Layer)
		- 