
- DRAM Types
	- Double Data Rate RAM (DDR)
	- DDR Ratings 
	- DRAM processes one command per clock cycle 
	- Word = 640 bits of data
	- Double pumping
	- MT/s = mega transfers/scond
	- DDR Rating = the MT/s spec
	- MHz = base speed of RAM
	- MT/s = base MHz x 2 

- PC Rating
	- Bandwidth in MB/s 
	- Data is processed in 64 bit (8-byte) words
	- to find PC rating, DDR rate x 8
	- Example DDR-266
		- 133 MHz
		- DDR2 

- DDR Ram Types
	- DDR 133-200 MHz, 266-400 MT/s, PC2100-PC3200, 2.5 Volts
	- DDR2 266 - 400 MHz, 533 - 800 MT/s, PC4200 - PC6400, 1.8 V
	- DDR3 533 - 800 MHz, 1066 - 1600 Mt/s, PC8500 - PC14900 1.5 V
	- DDR4 1066 - 1600 MHz, 2133 - 3200 MT/s PC12800 - PC25600 1.2 V, Power saving features, increased chip densities 
	- DDR -2133 -> Transfer Rate 17,066MB/s DDR-2400 -> Transfer Rate 19,200MB/s
	- DDR4-2666 -> Transfer Rate 21,333MB/s DDR4-3200 -> Transfer Rate 25,600MB/s
	- DDR5 2133 - 3200 MHz, 3200 - 6400 MT/s, PC38400 - PC51200 1.1 Volts, Power management on chip, two or four 32-bit channels for increased efficiency 
- * Remember that DDR4 is 260, DDR is 240*

- Physical Characteristics
	- DDR has pin slightly off to the side
	- DDR2 has more pins that aren't as wide, and the notch is in the middle
	- DDR3 has more pins that aren't as wide, towards the left
	- DDr4 Notch in middle 
	- DDR5 Pin count is the same and notch to the left 

- Form Factors
	- DIMM
		- Used in desktop slots
	- So-DIMM
		- Used in laptops, half the size
	- UniDIMM
		- Upgrade to the So-DIMM, allows mobile platform users to have DDR3 or DDR4 in the same slot 

- Multi-Channel Memory
	- All data must pass through memory controllers before reaching the RAM. The multi-channel adds more memory controllers. 
	- 5% to 15% increase only
	- Also specific to motherboard and not the memory itself
	- Supported with DDR2, DDR3, DDR4, and DDR5
	- Triple are supported with DDR3, DDR4, and DDR5 

- Memory Installation 
	- Check Existing Memory through the Motherboard or System documentation, or check online
	- Crucial is a great website/online source
	- If all else fails, examine the hardware
		- Serial number, pin count, and where the notch is
		- Sticker/model all that fun stuff
	- Choose memory that fits within the motherboard, check that the frequency and form factor is compatible with the motherboard
	- Check the memory package AKA memory form
		- Check to see if your system requires DDR2, DDR3. or DDR4 memory
	- Maximum Supported Memory
		- Dictated by the motherboard configuration
		- 32-bit: 4 GB max, does not mean that it supports 4 gigs though, some may be limited to 2
		- PAE allows system to access more than 4 GB if windows supports it 
		- 64-bit motherboard: accesses Terabytes of ram. Theoretical 16 EB, Practical 1-2 TB 
		- Check documentation for correct memory speed (PC5400, PC26400,PC31066) Ensure that the speeds match the MB and RAM
		- ECC Memory (Error Correcting Code)
			- Detects data corruption 
			- High-end systems 
			- Adds an extra chip to the ram slot that compares data through 1's and 0's (Parity check)
				- EX. ECC has 9 chips
				- EX. Non-ECC has 8 chips
				- ECC and Non-ECC cannot be mixed, if they are, the ECC is disabled
				- ECC decreases performance by 2%
				- Registered Memory (Buffered memory)
					- again used in high-end systems
					- offers an extra chip that acts as a buffer to hold data to prevent overload
					- Check MB documentation (lol)
			- CAS Latency (CL) Column Address Strobe
				- Tells you what performance you are going to get out of the module
				- Response time delay
				- Measures clock cycles
				- Special chip does magic shit
				- Lower CL = better
			- Timing Parameters
				- Measures memory module performance through four parameters (ex. 5-5-5-15), the parameters are measured below 
					- CL: CAS latency
					- tRCD: Row to column address
					- tRP: Row pre-charge time
					- tRAS: Row active time 
			- Serial Presence Detect (SPD)
				- Stored on an EEPROM chip
				- Located on the SDRAM 
					- Module size
					- Data width
					- Speed
					- Voltage 

- For Servers, it is essential to choose the correct memory chip to ensure the smoothest transfer of data possible. A one-second delay can be terrible.

- Dallas wants 10 computers or so 

- JayzTwoCents 

- Dallas learning techniques, professor graves and chewing gum example

- RAID 5 - Striping with Parity, can strike data between multiple disks \

- RAID 1 - Mirroring, used if you want to keep a system up at all times  