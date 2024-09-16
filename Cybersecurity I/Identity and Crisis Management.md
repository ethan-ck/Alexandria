
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

- 