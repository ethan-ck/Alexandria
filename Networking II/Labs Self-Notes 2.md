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

![[Screenshot 2024-09-09 191135.png]]
![[Screenshot 2024-09-09 192139.png]]

