<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1 Create some sample file shares with various permissions
- Step 2 Attempt to access file shares as a normal user
- Step 3 Create an “ACCOUNTANTS” Security Group, assign permissions, an test access
- Step 4

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/7W7rH1B.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
starting off from the last project log in to the domain controller then login to the other Vm client-1 with one of the user you created last project in the _EMPLOYEES folders then go back to the domain controller and go to windows(c) in file explorer and create a “read-access”, “write-access”, “no-access”, “accounting” then right click each folder execpt accounting then go to properties, sharing, share then add domain users and give it the permission that it says but for no-access give it both read and write.

</p>
<br />

<p>
<img src="https://i.imgur.com/ulX1YW2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
back to client-1 right click start then go to run and paste this \\dc-1 to access the four folders you created.
</p>
<br />

<p>
<img src="https://i.imgur.com/tvIwuXt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
go back to the domain controller and go to Active Directory Users and Computers and create a new folder organizatonal folder in your domain name called security groups then inside that folder create a new group called accountants and make suere the group type is security group. 
</p>
<br />
