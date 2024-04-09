<h1>Azure Sentinel Attack Map Cloud Lab</h1>

<h2>Description</h2>
Use a PowerShell Script to Extract Metadata from Windows Event Viewer to a Third Party API, Configure Log Analytics Workspace in Azure for Custom Logs with Geographic Information, Configure Customer Fields in Log Analytics Workspace, and Configure Azure Sentinel Workbook to Display Attack Data on World Map Based on Location and Magnitude of Attacks.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 

<h2>Environments Used </h2>

- <b>Azure Sentinel</b>

<h2>Program walk-through:</h2>

<p align="center">
Setup Windows Server 2019 Virtual Machine and Set Second Network Adapter to Internal Network: <br/>
<img src="https://i.imgur.com/wOQoLAH.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Install Windows Server 2019:  <br/>
<img src="https://i.imgur.com/s6NwCpQ.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Identify and Rename Internal Network Adapter by Finding Adapter with an APIPA: <br/>
<img src="https://i.imgur.com/yTRE0d4.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Rename Server PC:  <br/>
<img src="https://i.imgur.com/rEetYO6.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Assign Server IPv4 Address and Set DNS to Loopback Address:  <br/>
<img src="https://i.imgur.com/b1Emikx.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Install Azure Sentinel Attack Map:  <br/>
<img src="https://i.imgur.com/lfaetmf.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Promote Server to a Domain Controller:  <br/>
<img src="https://i.imgur.com/mfQqQWt.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Create Organizational Unit for Admin Users:  <br/>
<img src="https://i.imgur.com/DrewKHC.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Create New Admin User:  <br/>
<img src="https://i.imgur.com/OBby43P.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Make User Member Of Domain Admin Group:  <br/>
<img src="https://i.imgur.com/3oloAVc.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Sign Out of Main Admin Account and Sign In with Newly Created Admin User:  <br/>
<img src="https://i.imgur.com/6eBOaTC.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Install Remote Access for NAT and RAS:  <br/>
<img src="https://i.imgur.com/gLNkrYJ.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Set NAT Internet Connection to Internet Adapter:  <br/>
<img src="https://i.imgur.com/pGkypis.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Install DHCP Role:  <br/>
<img src="https://i.imgur.com/gyKhEMH.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Set Scope for IPv4 Range:  <br/>
<img src="https://i.imgur.com/dXxoNeE.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Set Default Gateway to Server IP Address:  <br/>
<img src="https://i.imgur.com/tKWi1C7.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Set DNS to Server IP Address:  <br/>
<img src="https://i.imgur.com/ej8Yu0c.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Create Users with PowerShell Script:  <br/>
<img src="https://i.imgur.com/mTDxMTO.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Create New Windows 10 Virtual Machine for a Client and Set Network Adapter to Internal:  <br/>
<img src="https://i.imgur.com/AO3Tt4F.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Rename Client PC and Join the Server Domain:  <br/>
<img src="https://i.imgur.com/VfQKOEo.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
<br />
<br />
Sign In to Domain from Client:  <br/>
<img src="https://i.imgur.com/ThF84jN.png" height="80%" width="80%" alt="Azure Sentinel Attack Map Lab Steps"/>
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
