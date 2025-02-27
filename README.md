<p align="center">
<img src="https://imgur.com/436aG7m.png" alt="Traffic Examination"/>
</p>

<h1> Wireshark & Network Protocols</h1> </h1>
This project explores network traffic behavior by capturing and analyzing DNS, DHCP, RDP, and SSH packets using Wireshark. The focus is on understanding how these protocols operate, troubleshooting network connectivity, and leveraging PowerShell for network administration. Additionally, it covers initiating an SSH connection to a Linux VM using its private IP address from a Windows machine. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
    - "CLIENT 1" (User PC) & "DC-1" (Domain Controller PC)
- Remote Desktop
- Wireshark
- Linux VM (Ubuntu/Debian-based) – For SSH testing.
- Powershell Terminal

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)

<h2>Key Observations</h2>
(WILL CHANGE THIS)
- DNS Resolution Analysis – Used PowerShell to query and analyze how domain names resolve to IP addresses.
- CNAME Record Configuration – Created and tested a CNAME record and pointed it to a web server.
- DNS Server Management – Configured and monitored DNS services using Windows Server Manager.
- PowerShell DNS Commands – Executed various commands such as flushdns, ping, & nslookup.


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










