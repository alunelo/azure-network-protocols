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

- DNS Analysis
    - Captured and analyzed DNS queries and responses using Wireshark.

- DHCP Packet Inspection
    - Observed the DORA (Discover, Offer, Request, Acknowledge) process for DHCP leases.
    - Monitored DHCP-assigned IP addresses and renewal times.
    - Used Get-DhcpServerv4Scope in PowerShell to check DHCP scope settings.
- RDP Traffic Analysis
    - Captured Remote Desktop Protocol (RDP) traffic between a Windows client and a remote server.

- Examined encryption methods in RDP traffic.
    - SSH Connection & Private IP Usage
    - Initiated an SSH session from PowerShell to a Linux VM using its private IP address:
ssh user@192.168.X.X

- Analyzed SSH handshake and encryption methods in Wireshark.
    - Captured ICMP, TCP, and UDP traffic for deeper insights.
    - Observed HTTP vs. HTTPS traffic to analyze encrypted vs. unencrypted data.
    - Used Test-NetConnection and ping to check network connectivity.


<h2>Actions and Observations</h2>

<p> 
<img src="https://imgur.com/NBtcTu5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<b>STEP 1</b> - Creating a RG-Network-Activities Resource Group On Azure.
<p>
<br />

<p>
<img src="https://imgur.com/C6g91J3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<b>STEP 2</b> - Creating A Windows 10 Virtual Machine.
<p>
<br />

<p>
<img src="https://imgur.com/5ttcJ5E.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 3</b> - Validation of Virtual Machine Succeeded.
</p>
<br />

<p>
<img src="https://imgur.com/InKcqIb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 4</b> - Creating a Linux and Windows VM Within The Same Lab-V2 Subnet.
</p>
<br />

<p>
<img src="https://imgur.com/fM8cVIz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 5</b> - Connecting Windows VM to Remote Desktop.
</p>
<br />

<p>
<img src="https://imgur.com/FQdKowC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 6</b> - Successfully Connected to VM.
</p>
<br />

<p>
<img src="https://imgur.com/Rz8FkWU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 7</b> - Downloading Wireshark on VM.
</p>
<br />

<p>
<img src="https://imgur.com/NkJB2LH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 8</b> - Installation of Wireshark.
</p>
<br />

<p>
<img src="https://imgur.com/MMQvhm5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 9</b> - Wireshark Displaying Network Activity On VM Adapter.
</p>
<br />

<p>
<img src="https://imgur.com/pKkjcnW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 10</b> - Filtering For ICMP Traffic.
</p>
<br />

<p>
<img src="https://imgur.com/6fIPwAI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 11</b> - Retrieving Linux Ubuntu VM Private IP Address.
</p>
<br />

<p> 
<img src="https://imgur.com/mRsWN6U.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<b>STEP 12</b> - Pinging Linux Private IP Address.
<p>
<br />

<p>
<img src="https://imgur.com/6ctDv3e.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<b>STEP 13</b> - Traffic of The Ping Is Displayed.
<p>
<br />

<p>
<img src="https://imgur.com/gKrKVFt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 14</b> - Initiating a Perpetual Ping of Linux VM.
</p>
<br />

<p>
<img src="https://imgur.com/zI2aqMW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 15</b> - Disabling Incoming (Inbound) ICMP Traffic.
</p>
<br />

<p>
<img src="https://imgur.com/uTPk31g.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 16</b> - Observed That ICMP Requests Have Timed Out.
</p>
<br />

<p>
<img src="https://imgur.com/Nb76Nfs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 17</b> - Filtering For <B>SSH</B> Traffic.
</p>
<br />


<p>
<img src="https://imgur.com/8AEYEjz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 18</b> - Initiating <b>SSH</b> Connection In Powershell.
</p>
<br />

<p>
<img src="https://imgur.com/xpu6Y3r.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 19</b> - Using Commands Such As <b>pwd</b> & <b>touch</b> to create a txt File Named <b>alo.txt</b>.
</p>
<br />

<p>
<img src="https://imgur.com/OTyq8Nb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 20</b> - Terminating SSH Connection.
</p>
<br />

<p>
<img src="https://imgur.com/wBqA89H.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 21</b> - Creating txt File With <b>/release</b> & <b>/renew</b> commands.
</p>
<br />

<p> 
<img src=https://imgur.com/30voGtd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<b>STEP 22</b> - Saving <b>dhcp.bat</b> File.
<p>
<br />

<p>
<img src="https://imgur.com/perc2WQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<b>STEP 23</b> - DCHP Traffic <b>DORA</b> Process Initiated & Displayed.
<p>
<br />

<p>
<img src="https://imgur.com/duXq8Xm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 24</b> - Switching To DC-1 PC To Create a DNS-A Record Named "mainframe" With DC-1's Private IP Address.
</p>
<br />

<p>
<img src="https://imgur.com/faow4j8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 25</b> - Pinged "mainframe" Succesfully on CLIENT 1 PC.
</p>
<br />

<p>
<img src="https://imgur.com/egWjE8X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 26</b> - Changing "mainframe" IP Address To 8.8.8.8 ON DC-1 PC.
</p>
<br />

<p>
<img src="https://imgur.com/TkPYyuw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 27</b> - "mainframe" Still Pinging From 10.0.0.4 IP Despite IP Address Change.
</p>
<br />


<p>
<img src="https://imgur.com/TkPYyuw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 28</b> - "mainframe" Still Holds A (Host) 10.0.0.4 When Initiating "ping" Command.
</p>
<br />












































