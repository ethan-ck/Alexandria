
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

- groupadd, usermod, useradd, groupmod, tail, 
	- new name first, old name second

- 