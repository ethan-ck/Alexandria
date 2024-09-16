
- Hardening 
	- Increase security

- Authentication
	- The log-on process

- Multifactor Authentication
	- Username + password
	- What you know, what you have, what you are, where you are

- Microprobing 
	- Accessing a smart cards chip

- Malicious actors rely on basic trust, authority, etc...

- Remember that Multifactor is multiple DIFFERENT authentication methods
	- Username + password
	- Smart ID

- Access Levels
	- Domain Accounts
		- Stored on domain controller (DC)
		- Managed by admins
	- Local user accounts
		- Stored locally
		- No local admin user accounts (change admin name to yoda)
		- creates standard users 

- Remote Access
	- Limit it, only need it
	- Connect through the DMZ 
		- Screened Subnet means the same thing


- Linux account types
	- Standard
	- System
		- used by services running in the background

- Encryption
	- Asymmetric
		- Public and Private key, both are separate, but connected
	- Symmetric
		- 

- Linux Re-sync 
	- pwck (password check) to resync passwords

- Chage command
	- Chage [options] [username/LOGIN]
	- Options:
		- -m days (minimum)
		- -M days (maximum)
		- -w (warning) 

- groupadd, usermod, useradd, groupmod, tail, man (command)
	- new name first, old name second
	- man = manual, the help version of manual
	- tail means view the end of the result

# Remote Access

- Policies which restrict access 
- Point-to-Point Protocol
	- Data link connecction
	- Assigns IP addresses and authentication

- Passwod Authentication Protocl
	- Sends in clear text, bad

- Chap
	- Passphrases, but not passwords

- EAP 
	- More secure than CHAP, 
	- Client/Server negotiates
	- Multi-factor authentication

- RAS
	- remote authoristion

- user base, time base, group base 


- AAA Server
	- Authentication
	- Authorizing
	- Accounting
		- Tracks connection

- RADIUS
	- Runs on 1-2 devices (accounting)
	- UDP for authorization (UDP is connection-less)
	- used with Microsoft

- TACACS+
	- Runs on 1-3 devices (all three A's can be split)
	- TCP for authentication (connected, 3-way handshake)
	- Encrypted communications
	- Cisco

# Network Authentication

- Kerberos
	- Linux, Unix, and Windows Active Directory
	- Single-sign on 
	- Mutual Authentication
	- Uses tickets to indicate authorization 
	- think SSO and TICKETS and TIME
	- 
- plain text/ clear text = bad, unencrypted 


- 802.1x Authentication
	- Switch or WAP allows authentic traffic between it and RADIUS Server 
	- is an extension of EAP 
	- uses many authentications

- RADIUS
	- think REMOTE AUTHENTICATION

- LDAP
	- Protocol for accessing directory services, but is not a directory service itself
	- open source
	- lightweight
	- Runs over TCP/IP
	- defaults to clear text, but can be secured via SSL/TLS

- 3 Security Protocols
	- SSH
	- SSL/TLS
	- IPsec 

- SASL
	- Simple authentication and security layer

- Kerberos Authentication
	- Key Distribution Center
		- Kind of like a scavenger hunt but with tickets
	-  You get a ticket granting session key (TGS) from the authentication server
	- You go to the ticket granting server, which grants a ticket for a certain time period
	- Ticket granting a ticket, which then gives a key to access the Acct File Server
	- Acct File Server gives you a file server session key for the File Server, which can decrpyt the ticket and session key
	- All of this setup is more trust-sake
	- All handshakes are encrypted, safe from malicious actors
	- Basically signing into the BC3 protocol, which allows you to enter blackboard, email, student planning, etc... Single sign on b/c we trust you since you went throguh a bunch of security hoops. 

- 

- 

- 