
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
		- 510

# User Files

Linux is highly flexible regarding where user and group information is stored. The options for storing the data are:

- Local file system.
- LDAP-compliant database.
- Network Information System (NIS). NIS allows many Linux computers to share common user accounts, group accounts, and passwords.
- A Windows domain.  
    

When files are stored in the local file system, the following files are used:

| File        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| /etc/passwd | The /etc/passwd file contains the user account information. Each user's data is stored in a single line on this file. There are two types of accounts in a Linux system:  <br><br>- Standard accounts (these are user accounts).<br>- System user accounts (these are used by services).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /etc/shadow | In Linux, local user account names are stored in /etc/passwd. When a user logs in to a local interactive shell, the password is checked against a hash stored in /etc/shadow. There are corresponding entries in both files, and they must stay synchronized. The system provides password and user management utilities, allowing you to edit and keep the files synchronized. You can use the following commands to identify errors and synchronize the files:  <br><br>- **pwck** verifies each line in the two files and identifies discrepancies.<br>- **pwconv** adds the necessary information to synchronize the files.  <br>    <br><br>Interactive login over a network is typically accomplished using Secure Shell (SSH). With SSH, the user can be authenticated using cryptographic keys instead of a password.  <br>A pluggable authentication module (PAM) is a package for enabling different authentication providers, such as smart-card log-in. The PAM framework can also be used to implement authentication to network directory services. |
| /etc/group  | As with Active Directory, groups can be used to simplify user access to network resources. The /etc/group file contains information about each group.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

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
![[Screenshot 2024-09-07 115907.png]]

![[Screenshot 2024-09-07 120555.png]]
usermod -l (lowcase L)

1. Delete the Terry Haslam account and home directory.
    1. From the Favorites bar, select **Terminal**.
    2. At the prompt, type **userdel -r thaslam** and press **Enter**.
2. Verify the account's removal.
    1. Type **cat** **/etc/passwd** and press **Enter**.
    2. Type **ls /home** and press **Enter** to verify the account was removed.

1. Change your password.
    1. From the Favorites bar, select **Terminal**.
    2. At the prompt, type **passwd** and press **Enter**.
    3. When prompted, enter **7hevn9jan** and press **Enter**. This is the current password.
    4. At the _New password_ prompt, enter **r8ting4str** and press **Enter**.
    5. Retype **r8ting4str** as the new password and press **Enter**.

1. Change Salman Chawla's password.
    1. From the Favorites bar, select **Terminal**.
    2. At the prompt, type **su -c "passwd schawla"**, then press **Enter**.
    3. Type **1worm4b8**, then press **Enter**. This is the password for the root user.
    4. At the _New password_ prompt, type **G20oly04**, then press **Enter**. This is the new password for the schawla user account.
    5. At the _Retype new password_ prompt, type **G20oly04**, then press **Enter**.
    6. cat /etc/shadow

1. Lock the applicable accounts.
    1. From the Favorites bar, select **Terminal**.
    2. At the prompt, type **usermod -L vedwards** or **passwd -l** **vedwards** and press **Enter**.
    3. Type **usermod -L cflynn** or **passwd -l** **cflynn** and press **Enter**.
    4. Type **usermod -L bkahn** or **passwd -l bkahn** and press **Enter**.
2. Unlock the applicable accounts.
    1. Type **usermod -U mbrown** or **passwd -u mbrown** and press **Enter**.
    2. Type **usermod -U bcassini** or **passwd -u bcassini** and press **Enter**.
    3. Type **usermod -U aespinoza** or **passwd -u aespinoza** and press **Enter**.
3. Verify your changes by typing **cat /etc/shadow** and pressing **Enter**.  
    The inclusion of the exclamation point (**!**) in the password field indicates whether the account is disabled.


- groupadd 
- su -root 
- less /etc/login.defs
- groupmod -n (newname) (existinggroup) 
- tail /etc/group 
- man usermod 
- usermod -g (only one primary group)
- usermod -G (supplementary) (this will remove any other group memberships)
- usermod -G -a (groupname) this will add the group to the group list without overwriting anything
- groups  (lists all groups of the user)
- groupdel (username) tail /etc/group to verify

1. Rename the sales group _western_sales_division_ and create the _eastern_sales_division_ group.
    1. From the Favorites bar, select **Terminal**.
    2. At the prompt, type **groupmod -n western_sales_division sales** and press **Enter**.
    3. Type **groupadd eastern_sales_division** and press **Enter**.
2. Modify the group membership as needed.
    - Type **usermod -G eastern_sales_division aespinoza** and press **Enter**.
        
        > When you assign aespinoza to the _eastern_sales_division_ group using the **usermod -G** option, the user account is removed from the _western_sales_division_ group.
        
3. Use **cat /etc/group** or **groups aespinoza** to verify aespinoza's group membership.


1. Add users to the hr group.
    1. From the Favorites bar, select **Terminal**.
    2. At the prompt, type **usermod -G hr mbrown** and press **Enter**.
    3. Use **usermod -G hr cflynn** and press **Enter**.
2. Verify the group membership for the users added to each group.
    1. Use **groups mbrown** and press **Enter**.
    2. Use **groups cflynn** and press **Enter**.


1. View a list of all groups to which Cory Flynn belongs.
    1. From the Favorites bar, select **Terminal**.
    2. At the prompt, type **groups cflynn** and press **Enter**.  
        Notice that cflynn currently belongs to the _mgmt1_, _hr_, and _it_ secondary groups. The cflynn group is the user's primary group.
2. Change and verify Cory Flynn's group membership.
    1. Type **usermod -G mgmt1,it cflynn** and press **Enter**.
    2. Type **groups cflynn** and press **Enter**.  
        Cory now only belongs to the _mgmt1_ and _it_ groups.

"Permissions Issue" 
View -> Advanced Features -> Right click OU and properties -> 


"Configure password settings" 
Searchbar -> Local Security Policy -> Account Policies 


"Restrict Local Accounts"
Tools -> Group Policy Management -> 
1. Access the **CorpNet.local** domain under Group Policy Management.
    1. From Server Manager, select **Tools** > **Group Policy Management**.
    2. Maximize the windows for better viewing.
    3. Expand **Forest: CorpNet.local** > **Domains** > **CorpNet.local**.
2. Create a policy to update the built-in Administrator local group.
    1. Right-click **Default Domain Policy** and select **Edit**.
    2. Maximize the windows for better viewing.
    3. Under Computer Configuration, expand **Preferences** > **Control Panel Settings**.
    4. Right-click **Local Users and Groups** and select **New** > **Local Group**.
    5. Using the _Group name_ drop-down, select **Administrators (built-in)**.
    6. Select **Delete all member users** to remove all member users.
    7. Select **Delete all member groups** to remove all member groups.
    8. Select **Add**.
    9. In the _Name_ field, enter **BUILTIN\Administrator** and then select **OK**.
    10. Select **Add**.
    11. In the _Name_ field, enter **%DOMAINNAME%\Domain Admins** and then select **OK**.
    12. Select **OK** to save the policy.

1. Access the computer's Computer Management tool.
    1. Right-click **Start** and select **Computer Management**.
    2. Under System Tools, expand **Local Users and Groups**.
    3. Select **Users**.
2. Rename the Administrator account.
    1. From the center pane, right-click **Administrator** and select **Rename**.
    2. Enter **Yoda** and press **Enter**.
3. Disable the Guest account.
    1. Right-click **Guest** and select **Properties**.
    2. Select **Account is disabled** and select **OK**.
4. Remove Password never expires option if it is selected.
    1. Right-click a _**user**_ and select **Properties**.
    2. Deselect **Password never expires** (if selected) and then select **OK**.
    3. Make a note of any user who has _User must change password at next logon_.
    4. Repeat steps 4a-4c for each user.
5. Delete any unused accounts.
    1. Right-click the **_user_** that has **User must change password at next logon** selected and select **Delete**.
    2. Select **Yes** to confirm the deletion of the account.

1. On CorpDC, access the **CorpNet.local** domain for Group Policy Management.
    1. From Server Manager, select **Tools** > **Group Policy Management**.
    2. Maximize the window for easy viewing.
    3. Expand **Forest: CorpNet.local** > **Domains** > **CorpNet.local**.
2. Configure the UAC settings.
    1. Right-click **Default Domain Policy** and select **Edit**.
    2. Maximize the window for better viewing.
    3. Under Computer Configuration, expand and select **Policies** > **Windows Settings** > **Security Settings** > **Local Policies** > **Security Options**.
    4. From the right pane, double-click the _**policy**_ you want to edit.
    5. Select **Define this policy setting**.
    6. Select **Enable** or **Disable** as necessary.
    7. Edit the _**value**_ for the policy as needed, and then select **OK**.
    8. Repeat steps 2d–2g for each policy setting.

![[Screenshot 2024-09-07 141131.png]]


A -> G -> (u) -> DL <- P 

Account, Global, User/ account, Domain local, permissions