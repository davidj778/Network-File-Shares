

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
Connect/log into Client-1 as an admin (mydomain\john_admin)
</p>
<img src="https://i.imgur.com/KVFkXwb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Create a DNS A-record on DC-1 for “mainframe” and have it point to DC-1’s Private IP address
</p>
<img src="https://i.imgur.com/q5Og6Yw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Go to Client-1 and try to ping it. Observe that it works
</p>
<img src="https://i.imgur.com/BigO9GT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
