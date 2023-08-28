

<h1>Building Intuition for DNS</h1>



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Stages</h2>

A-Record Exercise
- Connect/log into Client-1 as an admin (mydomain\john_admin)
- Create a DNS A-record on DC-1 for “mainframe” and have it point to DC-1’s Private IP address
- Go to Client-1 and try to ping it. Observe that it works


Local DNS Cache Exercise
- Go back to DC-1 and change mainframe’s record address to 8.8.8.8
- Go back to Client-1 and ping “mainframe” again. Observe that it still pings the old address
- Observe the local dns cache (ipconfig /displaydns)
- Flush the DNS cache (ipconfig /flushdns). Observe that the cache is empty
- Attempt to ping “mainframe” again. Observe the address of the new record is showing up

<h2></h2>
<h2>A-Record Exercise
</h2>

<p>

<p>
With remote desktop, log into Client-1 with (mydomain\john_admin). You can confirm that you are logged in as john_admin by using the command prompt and typing in "whoami".
</p>
</p>
<br />

<p>
In order to create a DNS A-record on the Domain controller, you have to point it to the Domain controllers private IP address.
</p>
<img src="https://i.imgur.com/q5Og6Yw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Go back to client-1 and use the ping command to insure connectivity.
</p>
<img src="https://i.imgur.com/BigO9GT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h2></h2>
<h2>Local DNS Cache Exercise
</h2>

<p>
Go to the Domain controller and right click the "mainframe" option, select "New Host", then change the mainframe's record address to 8.8.8.8.
</p>
<img src="https://i.imgur.com/cYJbS7L.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Go to Client-1 and use cmd to ping “mainframe”. Notice how it still pings the old address.
</p>
<img src="https://i.imgur.com/1bqGoR7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Use the ipconfig/displaydns to observe the local dns cache
</p>
<img src="https://i.imgur.com/vgwPvQ2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
In order to flush the DNS cache, you have to use the ipconfig/flushdns option to reset the cache. Confirm that the cache is empty.
</p>
<img src="https://i.imgur.com/Zxb6IoO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Ping the "mainframe". A new address should appear.
</p>
<img src="https://i.imgur.com/WKZB91W.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
