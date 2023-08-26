

<h1>Network File Shares and Permissions</h1>
This tutorial outlines the lifecycle of a ticket from intake to resolution within the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Stages</h2>

- Sharing out resources over the network
- Creating File Shares to allow Read, Write, or Deny access to indiviual users or groups

<h2></h2>
<h2>A-Record Exercise
</h2>

<p>
<p>
Connect/log into DC-1 as your domain admin account (mydomain.com\john_admin)
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Connect/log into Client-1 as an admin (mydomain\john_admin)
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
From Client-1 try to ping “mainframe” notice that it fails
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Nslookup “mainframe” notice that it fails (no DNS record)
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Create a DNS A-record on DC-1 for “mainframe” and have it point to DC-1’s Private IP address
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Go back to Client-1 and try to ping it. Observe that it works
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h2></h2>
<h2>Local DNS Cache Exercise
</h2>

<p>
Go back to DC-1 and change mainframe’s record address to 8.8.8.8
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Go back to Client-1 and ping “mainframe” again. Observe that it still pings the old address
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Observe the local dns cache (ipconfig /displaydns)
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Flush the DNS cache (ipconfig /flushdns). Observe that the cache is empty
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Attempt to ping “mainframe” again. Observe the address of the new record is showing up
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
