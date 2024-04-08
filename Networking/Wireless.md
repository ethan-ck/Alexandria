- Limitations
	- Wireless Interference
	- Bandwidth Sharing
	- Frequency ranges
	- Router type and configuration can impact the following facts above

- Frequency Ranges
	- 2.4 GHz
		- Waves are less compact and longer than 5 GHz
		- Travels further
	- 5 GHz
		- More data is being transmitted
	- Higher frequency = lower distances 
	- Dual-Band Wireless Routers can do both at the same time, 5 GHz on the first floor, and 2.4 GHz on higher floors 

- Service Set Identifier (SSID) 
	- Wireless network's public name
	- Name of the wireless network 
	- It broadcasts out like a lighthouse

- Service Set 
	- A group of devices that share an SSID in a network

- Channels
	- Frequency is one string constantly moving 
	- A lot of channels for each 2 frequency ranges
	- Channels can overlap, so 5 GHz introduced more channels 
	- Overlap is bad (Duh)

- Wireless Architecture 
	- STA 
		- A Station that is usually the host itself
		- Two modes 
			- Ad hoc network 
				-  uses a mesh topology and communicates with each other
			- Infrastructure mode
				- Uses a wireless access point that acts as a hub or switch. The access point in the middle acts as a keeper towards all other device
	- BSS 
		- Basic Service Set
	- Media Access Control Methods
		- CSMA/CA
			- Collision Avoidance 
			- Works similar to the bus topology collision detection/prevention 
			- RTS - Wait until the data is received
			- CTS - Clear to Send
			- Waits for an ACK, if no ACK is received, the wireless device assumes that there was a collision and sends the data again
			- Uses a star topology, but uses the logical bus topology 

- Two Frequencies 
	- 5Ghz (The towers are controlling your brain) 
		- 12 out of 23 channels 
	- 2.4Ghz
		- Only has three channels (3 arcs) 
	- 

- MIMO (Multiple Input/Multiple Output)


- NFC (Near Field Communication)
	- Similar to RFID, has the same freqeuncy (13.56 MHz)
	- <= 4 cm between devices
	- used in smartphones, notebooks, laptops, tablets, NFC readers and tags 

- SOHO (Small Office, Home Office)
	- Sort of like a HAN - Hoem Area network
	- It is used for a small office area network
	- not for large businesses obviously 

- General configuration steps
	- Connect workstation to WAP ethernet port
	- Set workstation static Ip address or use DHCP 
	- Connect and power on the workstation 
	- Access the web service on WAP in browser
		- Key in IP address in browser 
	- Make configuration changes 

- Security
	- WEP 
		- Old, easier to exploit
	- WPA Personal (PSK - Preshared Key)
	- WPA Enterprise (RADIUS/TACACS server)
	- WPA2 Personal (PSK) 
	- WPA2 Enterprise (Radius/TACACS server)
	- Essentially the encryption gets better 
		- More bits = stronger encryption algorithm 
	- Access controls
		- MAC Address filtering 
		- Whitelist certain MAC addresses to connect to network 
