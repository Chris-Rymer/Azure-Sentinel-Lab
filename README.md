<h1>Azure Sentinel (SIEM) Honeypot Attack Map Cloud Lab</h1>

<h2>Description</h2>
Setup a Virtual Machine in Azure to use as a Honeypot, Use a PowerShell Script to Extract Metadata from Windows Event Viewer to a Third Party API for Geographic Information, Configure Log Analytics Workspace in Azure for Custom Logs with Geographic Information, Configure Customer Fields in Log Analytics Workspace, and Configure Azure Sentinel Workbook to Display Attack Data on World Map Based on Location and Magnitude of Attacks.
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
Create a Windows 10 Virtual Machine in Azure to Act as a Honeypot: <br/>
<img src="https://i.imgur.com/0fzLxnF.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Create Inbound Firewall Rule to Allow All Incoming Data:  <br/>
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
Turn On Mircosoft Defender for Cloud:  <br/>
<img src="https://i.imgur.com/kFJjVs4.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Connect Log Anaytics to Honeypot Virtual Machine:  <br/>
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
Attempt to Ping Honeypot Virtual Machine with Personal PC and Find Ping Fails Due to Firewall Blocking ICMP:  <br/>
<img src="https://i.imgur.com/duVran6.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Turn Off Firewall on Honeypot Virtual Machine:  <br/>
<img src="https://i.imgur.com/ehO4UA8.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Attempt to Ping Honeypot Virtual Machine with Personal PC Again and Find Can Now Successfully Ping:  <br/>
<img src="https://i.imgur.com/jXjP2FL.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Run PowerShell Script with IPGeoLocation.io API Key to Log Failed Log In Attempts and Location:  <br/>
<img src="https://i.imgur.com/m1SlwqZ.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Create Custom Log in Microsoft Log Analytics with Sample of Log Created by PowerShell Script and Set Path to Location of Log on Honeypot Virtual Machine:  <br/>
<img src="https://i.imgur.com/HbflsJe.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
After Waiting 30 Minutes, Logs From Honeypot Virtual Machine Appear in Microsoft Log Analytics:  <br/>
<img src="https://i.imgur.com/nMtDvgJ.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Create New Workbook in Microsoft Sentinel and Use KQL Script to Extract/Map Geo Location:  <br/>
<img src="https://i.imgur.com/hzwsc92.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
After Waiting 1 Hour, Map Shows Failed Log In Attempts From Around the World:  <br/>
<img src="https://i.imgur.com/AKd7ERo.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
View Attempts also from Honeypot Virtual Machine PowerShell:  <br/>
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
