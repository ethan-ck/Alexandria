- IP Addressing 
	- Minimum for connecting to the internet is the IP address and subnets 

- APIPA 
	- DHCP server could not be found 
	- Automatic Private 
	- ONLY FOR MICROSOFT PLATFORMS 

- DHCP 
	- Lease stuff
	- DHCP assigns leases 
	- Great time saver - more efficient
	- You do not use the DHCP for switches and some network devices 

- DNS (Domain Name System)
	- It's the web address for us. For example 
	- www.BC3.edu is the host address that we read
	- However, the computer reads www.BC3.edu as 123.456.789
	- DNS is the automatic conversion between the host address and IP address. 
	- One of the "Look-up tables" 
	- "Scarecrow Wizard of Oz example"
	- Forward lookup zone = host name to the IP address
	- Reverse lookup zone = IP address to the host name 

- Configuring IP addresses on a mobile device 
	- Settings -> WIFI -> CorpNet -> Connect to WiFi with password
	- Click static and continue 
		- Remember default gateway = router 

- Configure Alternative Addressing 
	- Go to the IPv4 properties
	- Make sure to obtain DNS and IP address automatically
	- Go to the other tab and manually enter the addresses 

- Configure a DHCP Server
	- DHCP
		- Scope is a range or pool of IP addresses
		- These groups of IP addresses will be given out as leases 
		- WINs are DNS for old Microsoft windows machines 
		- "Activate the scope"
	- Hyper V is a windows VM 
	- CORPSERVER -> CORPSDHCP
	- A windows server is called an NOS, (Network Operating System) it manages the server and allows it to manage other devices
	- "Different hat examples" 
	- Remember to be in Ethernet 
	- Tools -> DHCP 

- Configure DHCP Options
	- Configure the router and default gateway and what URL they are going to use
	- **Remember that server options are different from DNS options** 

- Create DHCP Exclusions
	- Exclusions pull a subset from the pool of IP addresses for network devices 

- Reservations of DHCP 
	- For printers (hellspawn)


- Configure a DHCP Relay Agent 
	- There is a problem if a device on LAN1 needs to broadcast to the DHCP server which is on LAN 2
	- A Relay allows you to handle this odd situation
	- "Jury-rigging" example
	- It allows you to pass broadcasts 
	- Command Line final step = enter ipconfig /renew
	- DORA process
	- Routers do not pass broadcasts as an anti- DDoS feature 

- Add a  DHCP Server on another Subnet 
	- Rouge = Unauthorized 
	- Wizards = A series of dialogue boxes that 

- Configure DNS Addresses 
	- There are zones, and there are records in those zones 
	- DNS 
		- A matchup of the Domain name and Ip address 
	- Host A record
		- (Pointer record)
	- Ethernet Properties -> IPv4 -> Use the following DNS server addresses -> advanced 
	- /ipconfig all 

- Create standard DNS Zones 
	- Two main zones
		- Forward Lookup zones
			- Web address to the IP address
		- Reverse lookup zones 
			- IP Address to the Web Address
			- (Pointer)
	- This will allow a user to 
	- CORPDc -> Tools -> DNS 
	- Need a resource record in both zones 
	- Dynamic updates is IP address and web address working together, it will automatically update the DNS 
		- This is called Dynamic Domain Name (DDNS) 
	- Remember to select the new forward lookup zone to allow any server in the properties dialogue box
		- This is for data backups or load-sharing 
		- It takes data from the first zone and copies it to the second zone

- Active Directory + Group Policy 
	-  A role that you can install on a windows server that turns the server into a domain controller (DC) 

- Create Host Records 
	- Rmemeber to click PTR box 

- Create CNAME Records (Canonical)
	- Alias that allow www.BC3.edu or BC3.edu to work 

- Troubleshoot DNS Records 
	- 