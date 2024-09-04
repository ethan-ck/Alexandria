- Active Directory - A centralized database that contains user accounts and security information (user groups, computer accounts, domains, trees, forests, etc...) 
	- Included in most Windows Server OSes
	- Four main containers:
	- Forest
		- Tree
			- Domains - We live here and down in the OUs
				- OUs (user accounts, groups, computer accounts, other OUs)

- Organizational Unit (OU) - A way to organize users, groups, and etc... in an active directory

- Domain objects - All resources (users, groups, computers, printers, etc...) are stored as objects in the AD

- You can add functionalities to servers by assigning it roles
	- Graves' hats example

- Azure Active Directory 
	- Microsoft's cloud based directory

- Standalone 
	- Not locally networked but connected to the internet

- Peer to peer
	- Each server is a workstation
	- No boss, they all work together
	- called a workgroup in Microsoft server
	- easy to implement, inexpensive, no special hardware or software required
	- Does not scale well, 10 to 15 computers, lacks control and security, has to duplicate user accounts and backup each workstation

- Client Server
	- 