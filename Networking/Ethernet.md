- Topologies
	- Bus
		- Invisible terminators on each end, straight line like a bus route (wow) 
		- Line must be clear in order for data to transmit 
		- If line or node goes down, it's all down (Fault tolerance)
	- Ring
		- Each node is connected to 2 other nodes on each side like a ring (wow)
		- Line or node goes down, its all down 
	- Star
		- All nodes are connected to a switch, like a star (wow)
	- Mesh
		- Every node is connected to each other, best for fault tolerance 

- Hubs send to all, inefficient and insecure
	- They're evil
- Switches send to one, switches replaced hubs 
	- No collisions

- CSMA/CD (Carrier Sense Multiple Access / Collision Detection)
	- It detects collisions, not prevent them
	- Sending devices send a jam signal
	- They wait with a backoff time in ms (RNG) 
	- one retransmits first

- Process of Transmitting on a bus 
	- Device senses line (carrier) free
	- Message broadcast
	- Received only by the intended destination  
	- Dropped by all others 

- Plexes
	- Simplex
		- Send-all
		- PA system
	- Half-Duplex
		- Send OR receive 
		- one-way
		- walkie-talkie
		- may cut speed in half
	- Full-Duplex
		- Send AND Receive
		- Cellphone

- Frame (Layer 2) Component 
	- Remember this is the PDU for Layer 2 
	- Normal Frame Size = 50 - 1500 Bytes

- CRC (Cyclical Redundacy Check) 
	- Detects errors 
	- IF CRC-Dest = CRC-Source
		- OK
	- ELSE
		- ERROR (Collision)
			- IF Collision, frames seize < 64 bytes 

- Ethernet Specifications
	- Speed, Base, Medium 
		- Speeds = 10 Mbps, 10 Gbps 
		- Base 
			-  Baseband = 1 Signal
			- Broadband = multiple signals
		- Medium - What type of fiber (TP, Coaxial, Fiber optic) 

- 