- Active Directory - A centralized database that contains user accounts and security information (user groups, computer accounts, domains, trees, forests, etc...) 
	- Included in most Windows Server OSes
	- Four main containers:
	- Forest
		- Tree
			- Domains - We live here and down in the OUs
				- OUs (user accounts, groups, computer accounts, other OUs)

- Organizational Unit (OU) - A way to organize users, groups, and etc... in an active directory
	- Basically folders 
	- Org - Department, region, or division - mirrors the business structure (or process)
	- Stores user and security information


- Domain objects - All resources (users, groups, computers, printers, etc...) are stored as objects in the AD

- Member Servers 
	- Other windows servers that do other things other than the active directory 
	- They have different roles
	- Email server, storage server, web server, database server

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
	- Each host has a role

- Domain Controller (DC)
	- It is a Windows Server that has the active directory role installed
	- A single point of failure, if it goes down, you're screwed
	- That's why you have multiple (redundancy) set up at the same time
	- Devices must join the domain
		- Easier with a centralized networking model
	- Expensive, specialized hardware and software, implementation is more complex

- Cloud-based Domain Networking
	- Use somebody else's server
	- as a service
	- metered use
		- Only pay for what you use 
	- Great ROI 
	- Frees up resources

- On-Premise Active Directory and Azure Active Directory (Cloud)
	- Must sync them up

- ADUC 
	- One of 5 roles that we are in the most

- Keep the structure broad to prevent resources from being spent 
	- No deeper than 5 folders

- Built-In Containers
	- OU Icons have a golden box on the folder icon
		- We make these
	- Built-in folders do not, they're stuck there
		- We cannot create, move, rename, or delete them

- 