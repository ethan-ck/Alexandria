
# Switching

- Forwarding Database - Same as a CAM table
- MAC address sends data to the switch, switch sends data to the other mac address that is matched by the forwarding database or cam table

- Learning, Forwarding, Filtering
- Learning, as data gets sent to and from MAC Addresses, the switch makes entries according to the source and destination class
- Forwarding 
	- Sends data to stuff
- Filtering 

- Out-of-Band Management
	- Separate from the normal network, imagine connecting a laptop not in the network to a switch via a USB 
	- The connection is called a Console Port

- In-Band Management
	- Connection via Telnet or SSL, getting into a device remotely 

- Switch Aggregation
	- Connect multiple switches together for better bandwidth and connection. 

- Review cables
	- Crossover
	- Rollover 
		- For console ports
		- Flat

# Basic Switch Config

- GUI and CLI 
	- Trunk ports
		- Can talk with the same computer groups (ex. sales) in two separate VLANs without going out to a router
		- Trunk ports are always tagged
	- Access ports
		- Normal switch ports
		- untagged
	- Auto-MDIX
		- Switch Port will automatically detect and configure itself to whatever device is connected to the port, used so you do not have to have a rollover cable

- 802.1q VLAN Tags
	- Tagged in the header
	- Can configure default VLANs
	- Default is a native VLAN
	- Links untagged packets to native VLAN
	- 