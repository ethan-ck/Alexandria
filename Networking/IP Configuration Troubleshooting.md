- Check the subnet mask 
	- For example, there are four computers
		- 192.168.1.1
		- 192.168.1.2
		- 192.168.1.3
			- These three 
		- 192.168.2.1 - This one would be on a different subnet 255.255.255.0 

- Default Gateway
	- ARP broadcast to determine proper destination
	- if the default gateway is misconfigured, the packet fails to send 
		- The switch uses the CAM table to find the correct MAC address, if it doesn't find the correct matchup, the switch sends it to the default gateway. 
	- Using the PING command, we can ping the loopback address (127.0.0.1) then another ip address in the local network. Then we ping the default gateway to ensure that it works 

- DNS Configuration 
	- Ping the web IP address
	- Ping the domain name address

- DHCP issues
	- Check for APIPA 
	- Ipconfig e

- Improper IP configuration

- Command line tools
	- ipconfig and ipconfig /all
		- Default mask
		- Ip address
		- MAC address
	- ping
		- 
	- tracert
	- 