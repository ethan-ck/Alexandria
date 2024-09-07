
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

- Linux Stuff