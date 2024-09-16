
![[Pasted image 20240915210155.png]]


![[Pasted image 20240915210843.png]]

![[Pasted image 20240915210922.png]]

![[Pasted image 20240915211629.png]]

![[Pasted image 20240915212414.png]]


![[Pasted image 20240915212519.png]]


![[Pasted image 20240915212554.png]]


![[Pasted image 20240915212636.png]]



![[Pasted image 20240915212959.png]]


- Sign in to pfSense using:
    - Username: admin
    - Password: P@ssw0rd (zero)
- Create a new certificate authority certificate using the following settings:
    - Name: **CorpNet-CA**
    - Country Code: **GB**
    - State: **Cambridgeshire**
    - City: **Woodwalton**
    - Organization: **CorpNet**
- Create a new server certificate using the following settings:
    - Name: **CorpNet**
    - Country Code: **GB**
    - State: **Cambridgeshire**
    - City: **Woodwalton**
- Configure the VPN server using the following settings:
    - Interface: **WAN**
    - Protocol: **UDP on IPv4 only**
    - Description: **CorpNet-VPN**
    - Tunnel network IP: **198.28.20.0/24**
    - Local network IP: **198.28.56.18/24**
    - Concurrent Connections: **4**
    - DNS Server 1: **198.28.56.1**
- Configure the following:
    - A firewall rule
    - An OpenVPN rule
- Set the OpenVPN server just created to **Remote Access (User Auth)**.
- Create and configure the following standard remote VPN users


![[Pasted image 20240915213307.png]]

![[Pasted image 20240915213702.png]]

![[Pasted image 20240915213749.png]]

![[Pasted image 20240915213814.png]]


