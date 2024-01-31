Wired and Wireless (Chap 9)

For Wired, there are 3 main cables 

1. Twisted Pair (UTP/STP)
2. Coaxial 
3. Fiber Optic 

Twisted Pair: 

U is for unshielded, which is widely used and supported

Twisted pair is exactly as it sounds, 8 pairs of individual wire twisted together in pairs 

Crosstalk - Occurs with twisted pair, interferes with data 

Electric Magnetic Interference 

The FBI is using Twisted Pair to watch me 

STP - Shielded TP 
Extra cost, used mainly to counter EMI 
Needed in manufacturing with electrical motors 
Has a drain wire - special grounding wire 

Plenum and Riser 

Plenum is the empty space above a dropped ceiling or raised floor

- Fire can spread rapidly in these areas, so plenum rated cables must be installed in these areas
- They are flame retardant (respectfully)

TP Wire Types 
Solid -
- Conducts signal better, but prone to breaks if bent repeatedly 
- best for permanent installation

Stranded 
- More flexible 
- better for frequently moved cables
- for wall plates and patch panels 

UTP Categories

Lower the number, the earlier technology and features available 
Speed and distance 

Cat 3 is old and in the retirement home
Cat 4 never existed (Big tech is lying to you)
Cat 5 is 4x the improvement of cat 3 
Cat 5e - lessens crosstalk and other stuff, also faster
Cat 6 - Speed, also backwards compatible with all the stuff 
Cat 6a - improvement (wow) - not backwards compatible (cringe) 
Cat 7 - shielded and two new connectors also 10gig (speed) (not backwards compatible, the Playstation of categories)

Once again, the higher the cats, faster and better it is 


UTP Connectors 

RJ11 - phone lines (DSL (lol) router to phone)

Coaxial Cable 

- one wire, infinite blah blah blah
- cable 
- old, no one wants it anymore 
- Bus (in) topologies
- THICK (god damn)
- not modern, expensive

Fiber Optic Cable 
- Let there be light 
-  expensive and hard to work with 

SMF (Single Mode)
- Faster and goes longer
- single (duh) 
- Very thin, thinner than a strand of hair (it's shy, don't bully its size)
- 10 Gbs for 40 Km 

MMF(Multi Mode Fiber)
- not as fast and shorter
- Multiple signals 
- Thicker than SMF
- Shorter Distances, Lower speeds
- Outside cladding traps light inside and makes it bounce. (Refractive Index)
- When Refractive indexes are different, shit gets wacky 
- 100 Mbps - 2 km, 10 Gb/s - 500m

Attenuation - signal loss over distance 

Fiber optic splicing 
- They splice inside of the truck, uses a specialized tool with a specialist (expensive)
- super complex and takes a long time 
- Cleaning (Polishing glass before installation) 
Wavelength Division Multiplexing 
- Joins signals before transmission
- expands network capacity 

Fiber Optic Connectors

- SC ("set and click" or square connector for SMF and MMF, locking tab)

LC ("Lift and Click") 
SMF and MMF 
MTRJ 
SMF and MMF 
send and receive (duplex)
plastic with locking tab

FC ("Fiber Connector")
- Single mode only, threaded to prevent loose connections) 

Media Convertor 
- Converts stuff or something idk 

Topologies (LAN)

1. Ring (Christmas lights, all connected to one another)
2. Bus (starts literally a line, with branching connections, think of a hallway with rooms on each side.)
3. Star (If one pc goes down, it doesn't break the connection, all PCs connect to the middle, its the BOSS)
4. hybrid (boring)
5. Mesh (clusterfuck but reliable)


Wiring Implementation 
- Straight-Through cable - The pinning ends on both sides is in the same order, used to connect unlike devices
	- T568A on one end and T568B on the other 
	- Hourglass 
	- One pair is for transmit, another pair is for receive
	- EX. (Transmit = 1 and 2, R = 3 and 6)
	- Solids and Stripes 

T568A: GOBOBr 

Starts with the stripes, except for the Blue. Blue is a weirdo, pins 4 and 5 

Green Orange Blue Orange Brown 

T568B: 
Orange Green Blue Green Brown 
Once again, blue starts with the solid, doesn't change 

RJ45 Connector 

RJ45 Crimping tool, it crimps dawg 
- It also strips, "How much do we have to pay"
- Talk to the wire, it's self-conscious, offer words of encouragement.  

- Cross-Over cable - to connect two devices that are the same, ("two laptop example")
	- Takes one Transmit pin on one side, and connects it to the receiving pin on the other side
	- Pin 1 goes to pin 3, 3 to 1, Pin 2 goes to 6, 6 to 2, it crosses (like Jesus)  
- Roll-Over Cable   

Demarc is the location point in which the ISP responsibility ends, and yours begin. 

MDF - Main Distribution Frame that connects to the Demarc 

IDF - 

VCC Vertical Cross Connect 










