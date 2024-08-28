
- 1. Identify the users 
	- This happens once
- 2. Authentication 
	- Make sure you are who you say you are - fancy term for the log-in process
	- A match in the look-up table between username and password
	- Remember the look-up tables
	- Multi-Factor 
		- What you know (passwords, pins, etc..)
		- What you have (phone, key, etc...)
		- What you are (biometrics = fingerprints, face ID, retina, voice)
		- Where you are (geolocation)
- 3. Authorization 
	- What you can do 
- 4. Auditing and Accounting
	- Logs
	- Objects = data applications, systems, and networks
	- Subjects = the user 
	- 

Steps 2 - 4 are called the three A's (The triple A's)

- Two servers do this, Radius and Tacacs

-- There are several different ways to implement the triple A's

- CIA Triad, 
	- Confidential - encrypting data
	- Availability - allowing the data to be accessed  
	- Integrity - Check hashing data, ensure that the data has not been modified 

- Non-repudiation 
	- You cannot dispute that this did not happen

- Gap Analysis 
	- What is missing in our security procedures? Potential areas of attack

- Principle of Least Privilege 
	- Prevents snowball effect by only assigning users what they absolutely need 
	- Users can request privilege escalation only when absolutely needed

- Need to know basis 
	- Why do you need to know?
	  

- Implicit Denial
	- Whitelists

- Separation of Duties
	- Have multiple people who have to sign off to get something

- Job rotation 
	- Cross train 