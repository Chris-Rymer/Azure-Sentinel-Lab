<h1>Azure Sentinel (SIEM) Honeypot Attack Map Lab</h1>

<h2>Description</h2>
Setup a Virtual Machine in Azure to use as a Honeypot, use a PowerShell script to extract Metadata from Windows Event Viewer to a third party API for geographic information, configure Log Analytics Workspace in Azure for custom logs with geographic information and configure Azure Sentinel Workbook with KQL to display attack data on world map based on location and magnitude of attacks.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b>
- <b>IPGeoLocation.io</b>
- <b>KQL</b> 

<h2>Environments Used </h2>

- <b>Azure Virtual Machine</b>
- <b>Azure Log Analytics</b>
- <b>Azure Sentinel</b>

<h2>Program walk-through:</h2>

<p align="center">
Create a Windows 10 Virtual Machine in Azure to act as a Honeypot: <br/>
<img src="https://i.imgur.com/0fzLxnF.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Create inbound firewall rule to allow all incoming data:  <br/>
<img src="https://i.imgur.com/874MF5v.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Deploy Honeypot Virtual Machine: <br/>
<img src="https://i.imgur.com/ijqIScQ.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Create Log Analytics Workspace:  <br/>
<img src="https://i.imgur.com/wqE8XOW.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Turn on Microsoft Defender for Cloud:  <br/>
<img src="https://i.imgur.com/kFJjVs4.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Connect Log Analytics to Honeypot Virtual Machine:  <br/>
<img src="https://i.imgur.com/rAA7K7w.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Add Microsoft Sentinel to Honeypot Workspace:  <br/>
<img src="https://i.imgur.com/520Zpa1.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Copy Public IP Address for Honeypot Virtual Machine:  <br/>
<img src="https://i.imgur.com/X41zi8t.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Connect to Honeypot Virtual Machine with Remote Desktop Connection:  <br/>
<img src="https://i.imgur.com/kd2tLFK.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Attempt to ping Honeypot Virtual Machine with personal PC and find ping fails due to firewall blocking ICMP:  <br/>
<img src="https://i.imgur.com/duVran6.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Turn off firewall on Honeypot Virtual Machine:  <br/>
<img src="https://i.imgur.com/ehO4UA8.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Attempt to ping Honeypot Virtual Machine with personal PC again and find can now successfully ping:  <br/>
<img src="https://i.imgur.com/jXjP2FL.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Run PowerShell script with IPGeoLocation.io API Key to log failed log in attempts and location:  <br/>
<img src="https://i.imgur.com/m1SlwqZ.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Create Custom Log in Microsoft Log Analytics with sample of log created by PowerShell Script and set path to location of log on Honeypot Virtual Machine:  <br/>
<img src="https://i.imgur.com/HbflsJe.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
After waiting 30 minutes, logs From Honeypot Virtual Machine appear in Microsoft Log Analytics:  <br/>
<img src="https://i.imgur.com/nMtDvgJ.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Create new Workbook in Microsoft Sentinel and use KQL Script to extract/map geo location:  <br/>
<img src="https://i.imgur.com/hzwsc92.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
After 24 Hours, map shows failed log in attempts from around the world:  <br/>
<img src="https://i.imgur.com/P8PQ4AC.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
View attempts also from Honeypot Virtual Machine PowerShell:  <br/>
<img src="https://i.imgur.com/9UVBhPl.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
