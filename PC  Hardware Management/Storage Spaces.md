- It makes it easier to add space
- Just add an additional disk lmao 
- Storage Spaces Components
	- Devices 
		- Represented by hard drives, they get thrown into a pool 
		- We take the pool and distribute it into storage spaces
			- Ex. E: and F: 
			- Benefits include the fact that we only have to buy new storage devices, which makes the data resilience and easy to set up
	- Thin Provisioning (Over-booking)
		- Not all users will use all of their space in their allocated storage space, so space is added to a user's storage space as the user consumes space
		- If the storage space runs out of disk space, it will immediately unmount, leaving it vulnerable to data corruption
		- It must be brought back online manually
		- Add more physical disk space to the pool and add it to the storage space in order to use the storage space 