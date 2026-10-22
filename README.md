# Date :22.10.2026
## Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration


# Objective
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram
 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>

<img width="1600" height="1001" alt="image" src="https://github.com/user-attachments/assets/2f5d6580-84a3-4b0d-bec1-da036682a6d2" />

________________________________________
# IP Addressing Table
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure
1.	Open Cisco Packet Tracer and add 2 PCs, 2 Switches, and 1 Router.
2.	Connect each PC to a switch, and each switch to the router using straight-through cables.
3.	Assign IP addresses to both PCs according to the IP table.
4.	Configure the router interfaces:
o	FastEthernet0/0 → 192.168.1.1
o	FastEthernet0/1 → 192.168.2.1
5.	Use no shutdown on both router interfaces to activate them.
6.	Set each PC’s default gateway:<br>
o	PC0 → 192.168.1.1<br>
o	PC1 → 192.168.2.1<br>
7.	Test connectivity using ping from PC0 to PC1.<br>
________________________________________
# Commands Used (Router CLI)
bash<br>
CopyEdit<br>
Router> enable<br>
Router# configure terminal<br>
Router(config)# interface fastethernet0/0<br>
Router(config-if)# ip address 192.168.1.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>

Router(config)# interface fastethernet0/1<br>
Router(config-if)# ip address 192.168.2.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>
________________________________________
# Output 
•	Router CLI configuration<br>
•	IP configurations on PCs<br>
•	Successful ping between PC0 and PC1<br>

<img width="1600" height="1002" alt="image" src="https://github.com/user-attachments/assets/0f32fff1-2f46-4636-a9ea-6b08d1f2f296" />

<img width="1600" height="993" alt="image" src="https://github.com/user-attachments/assets/25c853d4-86b2-4d49-b09d-c8e0b5b9e0a8" />

<img width="1600" height="1002" alt="image" src="https://github.com/user-attachments/assets/2b8cd8d7-5c1f-4a70-a6c8-a18ac36a2b54" />

<img width="1600" height="999" alt="image" src="https://github.com/user-attachments/assets/2619e6da-9639-4dbd-af00-e69df9674638" />

<img width="1600" height="996" alt="image" src="https://github.com/user-attachments/assets/34992b4d-eccf-4e6c-9fd1-cb16dd29cf7f" />

<img width="1600" height="986" alt="image" src="https://github.com/user-attachments/assets/dff6f8db-d41d-4b95-810f-de5a59567efb" />

<img width="1600" height="999" alt="image" src="https://github.com/user-attachments/assets/c0d0b2ef-c7e4-4069-900d-8509065d186c" />

________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

