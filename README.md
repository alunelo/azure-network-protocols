<p align="center">
<img src="https://imgur.com/UB1KIvZ.png" alt="Traffic Examination"/>
</p>

<h1>Domain Name Server Configuration </h1>
This project explores the fundamental IT concepts behind VPN technology using Proton VPN. The primary objective was to observe how a VPN affects network behavior, including IP address changes, location masking, DNS resolution, and encrypted traffic. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
    - "CLIENT 1" (User PC) & "DC-1" (Domain Controller PC)
- Remote Desktop
- Domain Name Server
- Powershell Terminal

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)

<h2>Key Observations</h2>

- IP Address Changes – Tracked how the public IP address changed when connecting to different Proton VPN servers worldwide.
- Location Masking – Verified geolocation data before and after VPN connection to analyze how websites and services detect user location.

<h2>DISCLAIMER</h2>

- There was supposed to a screenshot after STEP 9 that showed the process of creating a CNAME called "search."
- This CNAME was also configured to point to the URL of "www.google.com"

<h2>Actions and Observations</h2>

<p> 
<img src="https://imgur.com/2ASqzhP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
STEP 1 - Attempting To Ping "mainframe" on CLIENT 1 PC
<p>
<br />

<p>
<img src="https://imgur.com/uuTOGup.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
STEP 2 - "nslookup" mainframe Attempt Fails on CLIENT 1 PC
<p>
<br />

<p>
<img src="https://imgur.com/wTlivcl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
STEP 3 - Switching To DC-1 PC To Create a DNS-A Record Named "mainframe" With DC-1's Private IP Address.
</p>
<br />

<p>
<img src="https://imgur.com/SyYPi6a.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
STEP 4 - Pinged "mainframe" Succesfully on CLIENT 1 PC.
</p>
<br />

<p>
<img src="https://imgur.com/2cvdip0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
STEP 5 - Changing "mainframe" IP Address To 8.8.8.8 ON DC-1 PC.
</p>
<br />

<p>
<img src="https://imgur.com/GkXzhqv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
STEP 6 - "mainframe" Still Pinging From 10.0.0.4 IP Despite IP Address Change.
</p>
<br />


<p>
<img src="https://imgur.com/XqyPjA8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
STEP 7 - "mainframe" Still Holds A (Host) 10.0.0.4 When Initiating "ping" Command.
</p>
<br />

<p>
<img src="https://imgur.com/hCFM2av.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
STEP 8 - Initiated "flushdns" Command To Get Rid of The Cache on DC-1 PC.
</p>
<br />

<p>
<img src="https://imgur.com/E5AQ6x8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
*STEP 9* - The Ping Is Now Showing The New 8.8.8.8 IP Address.
</p>
<br />

<p>
<img src="https://imgur.com/2uj185b.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
STEP 10 - Pinged search CNAME Successfully.
</p>
<br />

<p>
<img src="https://imgur.com/7R0CRWg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
STEP 11 - "nslookup" Results for search CNAME.
</p>
<br />










