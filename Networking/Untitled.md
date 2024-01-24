NBR Sys and Conversions 

Data Encapsulation for TCP/IP Module 
- Puts data inside packet 
- "Hiding the data
- PDU is the generic name for frame, packet or segment
- Top to bottom 
- DE-encapsulated bottom to top 
- Devices have intelligence driving them to specific headers/trailers 

ARP - Address Resolution Protocol 
- Builds  packet with destination IP and source Ip
- sends broadcast requests (locally) , replies are as unicast 
- on the same network 
- lives at layer 3 - the Network Layer (IP address, router, IP and ARP)

Packets and Frames
- IP addresses are logical (variable) 
- Packets live in the Network layer (Ip addresses, router)
- Frames are in the Data Link layer (Switch and data access link)

TCP 3 Way Handshake and TCP Flags
- Connection 
- SYN ad ACK 
- SYN sends, ACK is acknowledged
- Three steps: C1 Sends a SYN Pack,  C2 sends SYNACK, C3 sends ACK 
- Idle scan, directs a SYN through a "zombie" computer 

Troubleshooting tools 
	ipconfig 
	nslookup 
	ping 

Hexademical 
1 Hex digit is 4 bits grouped 
Hex digits are 0 - 9, and A - F, which add in total 16 

11001100 = 204 
 
11010110 = 214 

1110 0111 = E7 

DE = 1101 1110
