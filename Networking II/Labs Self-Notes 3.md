![[Pasted image 20240912181622.png]]


![[Pasted image 20240914135043.png]]

mplete this lab as follows:

1. Begin a Wireshark capture.
    1. From the Favorites bar, select **Wireshark**.
    2. Maximize the window for easier viewing.
    3. Under Capture, select **enp2s0**.
    4. Select the _**blue fin**_ to begin a Wireshark capture.
2. Apply the **net 192.168.0.0** filter.
    1. In the _Apply a display filter_ field, type **net 192.168.0.0** and press **Enter**.  
        Look at the source and destination addresses of the filtered packets.
    2. Select the _**red** **square**_ to stop the Wireshark capture.
    3. In the top right, select **Answer Questions**.
    4. Answer Question 1.
3. Apply the **host 192.168.0.45** filter.
    1. Select the _**blue** **fin**_ to begin a Wireshark capture.
    2. In the _Apply a display filter_ field, type **host 192.168.0.45** and press **Enter**.  
        Look at the source and destination addresses of the filtered packets.
    3. Answer Question 2.
4. Apply the **ip.src==192.168.0.45** filter.
    1. In the _Apply a display filter_ field, type **ip.src==192.168.0.45** and press **Enter**.  
        Look at the source and destination addresses of the filtered packets.
    2. Answer Question 3.
5. Apply the **ip.dst==192.168.0.45** filter.
    1. In the _Apply a display filter_ field, type **ip.dst==192.168.0.45** and press **Enter**.  
        Look at the source and destination addresses of the filtered packets.
    2. Answer Question 4.
6. Apply the **tcp.port==80** filter.
    1. In the _Apply a display filter_ field, type **tcp.port==80** and press **Enter**.  
        Look in the Info column of the filtered packets.
    2. Answer Question 5.
7. Apply the **eth contains 11:12:13** filter.
    1. In the _Apply a display filter_ field, type **eth contains 11:12:13** and press **Enter**.  
        Look at the source and destination addresses of the filtered packets.
    2. Answer Question 6.
8. Apply the **tcp contains password** filter.
    1. In the _Apply a display filter_ field, type **tcp contains password** and press **Enter**.
    2. Select the _**red box**_ to stop the Wireshark capture.
    3. From the bottom pane, locate the password.
    4. Answer Question 7.
    5. Select **Score Lab**.



1. Ports 4, 5, 6
2. Ports 4, 5, 6
3. Ports 1 and 3
4. Exec and Office1
5. Office1, exec
6. 2 workstations do not have accesss to the netowrk, all systems successfuly pinged are function
7. the network card was bad