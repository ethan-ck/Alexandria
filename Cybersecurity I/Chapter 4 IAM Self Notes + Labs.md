
- Active Directory is Microsoft's way of simplifying the authentication process in a large-scale environment. 
	- It does this by assigning users to specific roles within an organization that has access to role-specific folders, networks, etc...

- Joining a Domain
	- Start -> System -> Domain or Workgroup -> Rename Computer or join workgroup 

- Managing Active Directory Objects
	- AD DS on Server Manager -> Tools -> Active Directory Users and Computers 
	- Objects are on the right (OUs and Containers)
	- To create new OUs, there is an icon that brings up a wizard. To create a user, there is a separate icon that also brings up a wizard
	- To create group accounts click the icon that brings up the wizard. From there you can add the users to the group by going to members -> add -> enter user here

- Group Policy
	- Allows you to configure multiple users within one thing
	- GPOs are an object, just like OUs
	- Start -> gpedit.mse -> Computer Configuration OR User Configuration 
	- Tools -> Group Policy Management 
	- gpmc.msc
	  1. Open the Group Policy Management Console (GPMC) on CorpDC.
	1. Navigate to the “Group Policy Objects” folder and locate the “Workstation Settings” GPO.
	2. Right-click the GPO and select “Edit” to open the Group Policy Editor.
	3. In the Group Policy Editor, navigate to the “Computer Configuration” section.
	4. Expand “Policies” > “Windows Settings” > “Security Settings”.
	5. Right-click “Security Settings” and select “Import Policy…”.
	6. Browse to `C:\Templates` and select the `ws_sec.inf` template file.
	7. Click “Open” to import the template file into the GPO.

- Sign in to only certain computers![[Screenshot 2024-09-06 211520.png]]

- Linux General Stuff
	- passwd file is stored in the /etc directory
		- It contains user account information but DOES NOT contain any password information
			- USER_NAME:PW:UID:GID:FULL_NAME:HOME:SHELL
			- PW will always be x, since passwords are NOT stored in teh passwd file
	- Shadow file is where passwords are stored
		- USER:PASSWD:LASTMOD:MINDAYS:MAXDAYS:WARN:DIS:EXP

- Linux Group Files
	- Groups are easier to manage large amounts of users 
	- GROUP:PASSWORD:GID:USER
	- Sine linux distro store these group files in a group file (gshadow)

Managing Linux Users
	- useradd command
		- /etc/default/useradd
		-  To set a home directory to be in a different location by default, you can set that default by typing useradd -D 
		- man useradd shows all aavailable options for the useradd command
		- -c for a comment 
		- -g to add single primary gorup
		- -G to add supplementary groups separated by commas
		- sudo useradd =c "Kim Sanders" -m ksanders

# User Files

Linux is highly flexible regarding where user and group information is stored. The options for storing the data are:

- Local file system.
- LDAP-compliant database.
- Network Information System (NIS). NIS allows many Linux computers to share common user accounts, group accounts, and passwords.
- A Windows domain.  
    

When files are stored in the local file system, the following files are used:

|File|Description|
|---|---|
|/etc/passwd|The /etc/passwd file contains the user account information. Each user's data is stored in a single line on this file. There are two types of accounts in a Linux system:  <br><br>- Standard accounts (these are user accounts).<br>- System user accounts (these are used by services).|
|/etc/shadow|In Linux, local user account names are stored in /etc/passwd. When a user logs in to a local interactive shell, the password is checked against a hash stored in /etc/shadow. There are corresponding entries in both files, and they must stay synchronized. The system provides password and user management utilities, allowing you to edit and keep the files synchronized. You can use the following commands to identify errors and synchronize the files:  <br><br>- **pwck** verifies each line in the two files and identifies discrepancies.<br>- **pwconv** adds the necessary information to synchronize the files.  <br>    <br><br>Interactive login over a network is typically accomplished using Secure Shell (SSH). With SSH, the user can be authenticated using cryptographic keys instead of a password.  <br>A pluggable authentication module (PAM) is a package for enabling different authentication providers, such as smart-card log-in. The PAM framework can also be used to implement authentication to network directory services.|
|/etc/group|As with Active Directory, groups can be used to simplify user access to network resources. The /etc/group file contains information about each group.|

Be aware of the following configuration files when managing user accounts:

|File|Description|
|---|---|
|/etc/default/useradd|The /etc/default/useradd file contains default values used by the useradd utility when creating a user account, including:  <br><br>- Group ID.<br>- Home directory.<br>- Account expiration.<br>- Default shell.<br>- Secondary group membership.|
|/etc/login.defs|The /etc/login.defs file contains:  <br><br>- Values used for the group and user ID numbers.<br>- Parameters for password encryption in the shadow file.<br>- Password expiration values for user accounts.|
|/etc/skel|The /etc/skel directory contains a set of configuration file templates that are copied into a new user's home directory when it is created, including the following files:  <br><br>- .bashrc<br>- .bash_logout<br>- .bash_profile<br>- .kshrc|

# User Management Commands

Although it is possible to edit the /etc/passwd and /etc/shadow files manually to manage user accounts, doing so can disable your system. Instead, use the following commands to manage user accounts:

|Command|Command Function|
|---|---|
|**useradd**|Create a user account. The following options override the settings as found in /etc/default/useradd:  <br><br>- **-c** adds a description for the account in the GECOS field of /etc/passwd.<br>- **-d** assigns an absolute pathname to a custom home directory location.<br>- **-D** displays the default values specified in the /etc/default/useradd file.<br>- **-e** specifies the date on which the user account will be disabled.<br>- **-f** specifies the number of days after a password expires until the account is permanently disabled.<br>- **-M** defines the secondary group membership.<br>- **-m** creates the user's home directory (if it does not exist).<br>- **-n** does not create a group with the same name as the user (Red Hat and Fedora, respectively).<br>- **-p** defines the encrypted password.<br>- **-r** specifies that the user account is a system user.<br>- **-s** defines the default shell.<br>- **-u** assigns the user a custom UID. This is useful when assigning ownership of files and directories to a different user.|
|**passwd**|Assign or change a password for a user:  <br><br>- **passwd** (without a username or options) changes the current user's password.<br>- Users can change their own passwords. The root user can execute all other **passwd** commands.  <br>    <br><br>Be aware of the following options:  <br><br>- **-S** username displays the status of the user account. LK indicates that the user account is locked, and PS indicates the user account has a password.<br>- **-l** disables (locks) an account. This command inserts a !! before the password in the /etc/shadow file, effectively disabling the account.<br>- **-u** enables (unlocks) an account.<br>- **-d** removes the password from an account.<br>- **-n** sets the minimum days before a password can be changed.<br>- **-x** sets the number of days before a user must change the password (password expiration time).<br>- **-w** sets the number of days before the password expires that the user is warned.<br>- **-t** sets the number of days following the password expiration that the account will be disabled.|
|**usermod**|Used to modify an existing user account; usermod uses several of the same switches as useradd. Be aware of the following switches:  <br><br>- **-c** changes the description for the account.<br>- **-l** renames a user account.<br>- **-L** locks the user account. This command inserts a ! before the password in the /etc/shadow file, effectively disabling the account.<br>- **-U** unlocks the user account.|
|**userdel**|Remove the user from the system. Be aware of the following options:  <br><br>- **userdel** [username] (without options) removes the user account.<br>- **-r** removes the user's home directory.<br>- **-f** forces removing the user account even when the user is logged into the system.|