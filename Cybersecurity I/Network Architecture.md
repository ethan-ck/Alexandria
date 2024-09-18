
- Attack Surface
	- All points in which a malicious actor could gain unauthorized access to 

- CIA
	- Confidentiality
		- Information that must be kept secret for people who do not need to know
		- Encryption
	- Availability
		- Can the information be accessed?
	- Integrity
		- The information is trusted and verified 

- 47,000 vulnerabilities can be condensed down into 3 fixes:
	- Social Engineering
		- User education
	- Patch Management
		- Make sure that your antivirus and OS or other software is up to date
	- Password Management 
		- Complex passwords
		- Password history
		- Change password every x time period 
		- password manager

- Segmentation
	- Group things together as separate entities 
	- Separate networks (VLANs) 

- Controls
	- Active Controls
		- Configuration and Data Exchange
	- Passive Controls
		- In the background

# Security Appliances

- All-In-One
- Unified Threat Management
- Network Security Appliances 

- Security Zone
	- Portions of the network that have certain security requirements or concerns

- Ad Hoc
	- This, temporary 
	- A decentralized network that allows connection without a traditional base station

- Intranet, Internet, Extranet
	- Intra - Within (BC3 Portal)
	- Inter - Between (BC3.Edu) 
	- Extra - Outside (BC3 and other businesses that access information, maybe other colleges)

- DMZ - Screened Subnet 
	- Publicly Accessible
	- Acts as a middle-man
	- AKA a Bastion Host

- Multi-interfaces
	- An interface is a way in or out of anything, usually used within switches, firewalls, etc...

- Network Access Control (NAC) 
	- Remediation 
		- Something that needs to be corrected
		- If computer does not pass health checks, it gets sent to a security zone 

- Jump Server
	- A hardened server that provides access to other hosts 
		- Usually used by admins

# Security Zones

- Sensors (Endpoints)
	- Information gathers to figure out what's going on in your network
		- SCADA/ICS
		- IDS
		- SIEM/SOAR

- Wireless Zones
	- Guest Networks
	- HoneyNet or HoneyPot Zones
	- Ad Hoc Network
	- Network Address Translation (NAT) 
		- Usually done through PAT (Port Address Translation)
		- xxxx:8001: p.p.p.p.8001
		- the Ip and a colon is called a socket

# All in One Security Devices 

- Integrated Security
	- URL filtering against gambling, adult sites, shopping etc...
	- Spam filtering 

- Personal Identifiable Information (PII) 

# Firewalls

- Host Firewall

- Network Firewall

- Host based IDS

- Network Based IDS 

- Host based Anti-Virus 

- Network based Anti-Virus

- Web Application Firewalls (WAFs)

- Next Generation Firewall
	- Yuge upgrades

- Software is host based
- Hardware is network based


- Stateful firewalls
	- circuit-level
	- more resource intensive but stops larger attacks
- Stateless Firewalls
	- ACLs 
	- Rule-based
	- inspects IP packets based on header details
	- Implicit Deny (Deny All) and whitelist others

# Network Address Translation

- Conserves the limited 4 billion IP addresses through Port Address Translation (PAT)
- Is used instead of IPv6, because we stopped the apocalypse
- NAT Router Table, Sequential Port differentiates (8001, 8002, etc...)

# Virtual Private Networks

- Secure tunnel that uses encryption and encapsulation (hide)
- L2TP, IPsec, SSL 

- IPsec
	- 2 Protocols
	- Authentication Header (AH) and Encapsulating Security Payload (ESP)

- 
