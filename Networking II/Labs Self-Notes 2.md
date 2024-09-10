NAT Forwarding
1. Sign into the pfSense management console.
    1. In the Username field, enter **admin**.
    2. In the Password field, enter **P@ssw0rd** (zero).
    3. Select **SIGN IN** or press **Enter**.
2. Configure NAT port forwarding for the PC1 computer.
    1. From the pfSense menu bar, select **Firewall** > **NAT**.
    2. Select **Add** (either one).
    3. Configure or verify the following settings:
        - Interface: **LAN**
        - Protocol: **TCP**
        - Destination type: **LAN address**
        - Destination port range (From and To): **MS RDP**
        - Redirect target IP: **172.16.1.100**
        - Redirect target port: **MS RDP**
        - Description: **RDP from LAN to PC1**
    4. Select **Save**.
3. Configure NAT port forwarding for the Kali Linux server.
    1. Select **Add** (either one).
    2. Configure or verify the following settings:
        - Interface: **LAN**
        - Protocol: **TCP**
        - Destination type: **LAN address**
        - Destination port range (From and To): **SSH**
        - Redirect target IP: **172.16.1.6**
        - Redirect target port: **SSH**
        - Description: **SSH from LAN to Kali**
    3. Select **Save**.
4. Configure NAT port forwarding for the web server.
    1. Select **Add** (either one).
    2. Configure or verify the following settings:
        - Interface: **LAN**
        - Protocol: **TCP**
        - Destination type: **LAN address**
        - Destination port range (From and To): **Other**
            - Custom (From and To) **5151**
        - Redirect target IP: **172.16.1.5**
        - Redirect target port: **Other 5151**
        - Description: **RDP from LAN to web server using custom port**
    3. Select **Save**.
    4. Select **Apply Changes**.

Username and Password fields, enter cisco (case-sensitive).Select Log In.  

Assign port GE26 to VLAN 
1.From the left pane, expand and select VLAN Management > Port VLAN Membership.Select GE26 and then select Join VLAN.From the left pane, under Select VLAN, select 1 (for VLAN 1).

Select > to move VLAN 1 from the available pane to the attached VLAN pane.Select Apply and then select Close.  

Mirror the received traffic from port GE28 to port GE26.

From the left pane, expand and select Administration > Diagnostics > Port and VLAN Mirroring.Select Add.

For the Destination Port, use the drop-down list to select GE26.For the Source Interface, use the drop-down list to select GE28.For the Type, make sure that Rx only is selected. This allows you to only mirror the incoming packets.

Select Apply and then select Close.  

Save the changes to the switch's startup configuration file.
From the upper right of the switch window, select Save.
For the Source File Name, make sure Running configuration is selected.

For the Destination File Name, make sure Startup configuration is selected.

Select Apply.Select OK.Select Done.

![[Screenshot 2024-09-09 191135.png]]
![[Screenshot 2024-09-09 192139.png]]

![[Screenshot 2024-09-09 194324.png]]


![[Screenshot 2024-09-09 194936.png]]
Complete this lab as follows:

1. Sign in to the pfSense management console.
    1. In the Username field, enter **admin**.
    2. In the Password field, enter **P@ssw0rd** (0 = zero).
    3. Select **SIGN IN** or press **Enter**.
2. Create a high bandwidth usage alias.
    1. From the pfSense menu bar, select **Firewall** > **Aliases**.
    2. Select **Add**.
    3. Configure the Properties as follows:
        - Name: **HighBW**
        - Description: **High bandwidth users**
        - Type: **Host(s)**
    4. Add the IP addresses of the offending computers to the host(s) configuration as follows:
        - Under Host(s), in the _IP or FQDN_ field, enter **172.14.1.25** for Vera's system.
        - Select **Add Host**.
        - In the new _IP or FQDN_ field, enter **172.14.1.100** for Paul's system_._
    5. Select **Save**.
    6. Select **Apply Changes**.
3. Start the Traffic Shaper wizard for dedicated links.
    1. From the pfSense menu bar, select **Firewall** > **Traffic Shaper**.
    2. Under the Firewall bread crumb, select **Wizards**.
    3. Select **traffic_shaper_wizard_dedicated.xml**.
    4. Under Traffic Shaper wizard, in the _Enter number of WAN type connections_ field, enter **1** and then select **Next**.
4. Configure the Traffic Shaper.
    1. Make sure you are on Step 1 of 8.
    2. Using the drop-down menu for the upper Local interface, select **GuestWi-Fi**.
    3. Using the drop-down menu for lower Local interface, make sure **PRIQ** is selected.
    4. For the upper _Upload_ field, enter **8**.
    5. Using the drop-down menu for the lower _Upload_ field, select **Mbit/s**.
    6. For the top Download field, enter **50**.
    7. Using the drop-down menu for the lower _Download_ field, select **Mbit/s**.
    8. Select **Next**.
5. Prioritize voice over IP traffic.
    1. Make sure you are on Step 2 of 8.
    2. Under _Voice over IP_, select **Enable** to prioritize the voice over IP traffic.
    3. Under _Connection #1 parameters_, in the Upload rate field, enter **10**.
    4. Using the drop-down menu for the top Units, select **Mbit/s**.
    5. For the Download rate, enter **20**.
    6. Using the drop-down menu for the bottom Units, select **Mbit/s**.
    7. Select **Next**.
6. Enable and configure a penalty box.
    1. Make sure you are on Step 3 of 8.
    2. Under Penalty Box, select **Enable** to enable the penalize IP or alias option.
    3. In the Address field, enter **HighBW**. This is the alias created earlier.
    4. For Bandwidth, enter **3**.
    5. Select **Next**.
7. Continue to step 6 of 8.
    1. For Step 4 of 8, scroll to the bottom and select **Next**.
    2. For Step 5 of 8, scroll to the bottom and select **Next**.
8. Raise and lower the applicable application's priority.
    1. Make sure you are on Step 6 of 8.
    2. Under Raise or lower other Applications, select **Enable** to enable other networking protocols.
    3. Under Remote Service / Terminal emulation, use the:
        - MSRDP drop-down menu to select **Higher priority**.
        - VNC drop-down menu to select **Higher priority**.
    4. Under VPN:
        - Use the PPTP drop-down menu to select **Higher priority**.
        - Use the IPSEC drop-down menu to select **Higher priority.**
    5. Scroll to the bottom and select **Next**.
    6. For step 7 of 8, select **Finish**.  
        Wait for the reload status to indicate that the rules have been created (look for Done).
9. View the floating rules created for the firewall.
    1. Select **Firewall** > **Rules**.
    2. Under the Firewall breadcrumb, select **Floating**.
    3. From the top right, select **Answer Questions**.
    4. Answer the question and then minimize the question dialog.
10. Change the port number used for the MSRDP outbound rule.
    1. For the _m_Other MSRDP outbound_ rule, select the _**edit**_ icon (pencil).
    2. Under Edit Firewall Rule, in the _Interface_ field, select **GuestWi-Fi**.
    3. Under Destination, use the Destination Port Range drop-down menu to select **Other**.
    4. In both Custom fields, enter **3391**.
    5. Select **Save**.
    6. Select **Apply Changes**.
    7. From the top right, select **Answer Questions**.
    8. Select **Score Lab**.

1. Log in to the CISCO switch.
    1. From the taskbar, select **Google Chrome**.
    2. In the URL field, enter **192.168.0.2** and press **Enter**.
    3. Maximize the window for better viewing.
    4. In the Username and Password fields, enter **cisco** (the password is case sensitive).
    5. Select **Log In**.
2. Examine the switch port defaults.
    1. From the left navigation bar, expand and select **VLAN Management** > **Interface Settings**.
    2. Using the interface shown in the right pane, examine the settings for all ports.
        
        > For a detailed view of a single port, you can select **Edit**.
        
    3. From the upper right, select **Answer Questions**.
    4. Answer Question 1.
    5. Minimize the Lab Questions dialog.
3. Set ports GE1 through GE26 to Access Mode.
    1. From the Interface Settings pane, select **GE1**.
    2. Select **Edit**.
    3. Maximize the window for better viewing.
    4. For _Interface VLAN Mode_, select **Access**.
    5. Select **Apply** and then select **Close**.
    6. With GE1 still selected, click **Copy Settings**.
    7. In the _to_ field, type **2-26** and then select **Apply**.  
        Notice that under the _Interface VLAN Mode_ column, ports GE1-GE26 are now set to Access.
4. Set the port VLAN ID (PVID) for ports GE27-GE28 to the value of 2.
    1. Select the desired _**port**_ and then select **Edit**.
    2. For the Administrative PVID, enter **2**.
    3. Select **Apply** and then **Close**.
    4. Repeat steps 4a - 4c for the second _**port**_.
5. Add VLANs 22, 44, and 67 to ports GE27 and GE28.
    1. From the left pane, under VLAN Management, select **Port VLAN Membership**.
    2. Select port **GE27** and then select **Join VLAN**.
    3. From the new window, hold down the _**Shift**_ key and select VLANs **22**, **44**, and **67**; then select the **>** button to assign the VLANs.
    4. Select **Apply** and then select **Close**.
    5. Repeat steps 5b - 5d for port **GE28**.
6. Save the changes to the switch's startup configuration file.
    1. From the top of the switch window, select **Save**.
    2. For _Source File Name_, make sure **Running configuration** is selected.
    3. For _Destination File Name_, make sure **Startup configuration** is selected.
    4. Select **Apply**.
    5. Select **OK**.
    6. Select **Done**.
7. Score the lab.
    1. From the upper right, select **Answer Questions**.
    2. Select **Score Lab**.

![[Screenshot 2024-09-09 200038.png]]
