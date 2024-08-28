
- File and directory names are case sensitive 
	- Testout.txt, testout.txt, and tEstout.txt are all different files

- It is standard to use dots (.) to identify file extensions
	- ex. file.tar.gz <--- gz = compressed tar file 

- At the beginning of each file, there is a file header which identifies the file type
	- Unlike windows, which uses file extensions

- Starting Commands

	- pwd = Displays the current working directory

	- cd = Changes the current working directory 
		- One dot represents the current directory
		- Two dots represents the parent directory
				Ex. cd .. brings you up one
				cd ../.. brings you up two 

	- ls = shows all contents in the current directory
		- Options
			- -a = shows all directory contents
			- -l = displays extended information, such as the owner, modified date, size, etc...
			- -R = displays the contents of a directory and all of its subdirectories
			- -r = reverses the sort order
			- -d = displays the directories but not the files 
		- You can combine options
			- ex. ls -al would list all directory contents as well as the extended information 
