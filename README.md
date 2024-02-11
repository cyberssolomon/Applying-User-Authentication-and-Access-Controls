<h1>Performing Packet Capture and Traffic Analysis</h1>

<h2>Tools and Software Used</h2>

- <b>Active Directory Users and Computers</b> 
- <b>PowerShell</b>
- <b>TrueNAS</b>



<h2>Environments Used </h2>

- <b>vWorkstation (Windows: Server 2022)</b>
- <b>pfSense-office (FreeBSD: pfSense)</b>
- <b>pfSense-dc (FreeBSD: pfSense)</b>
- <b>DomainController01 (Windows: Server 2019)</b>
- <b>FileServer01 (FreeBSD: TrueNAS)</b>
    

 
<h2>Description</h2>
Project consists of using using Microsoft's Active Directory Domain Services to implement an authetication and access control framework: creating new user accounts, security groups, and access control lists in a Wondows environment, distinguish Windows Security permissions from Windows Share permissions, and configuring access controls for a remote file server using Active Directory Security Groups.
<br />

### Section 1

<h2>Create Users and Security Groups:</h2>








<p align="center">
Show the new users and groups in Active Directory Users and Computers: <br/>
<img src="https://i.imgur.com/RHnjyGJ.png" height="80%" width="80%" alt="Section 1 Steps"/>


 <h2>Create Folders and Configure Security Permissions:</h2>







<p align="center">
Show the updated Security permissions for the HRfiles folder: <br/>
<img src="https://i.imgur.com/7d0nd5I.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the updated Security permissions for the MGRfiles folder:  <br/>
<img src="https://i.imgur.com/Asde0Rf.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the SSHv2 encryption and mac selections for the SSH connection:  <br/>
<img src="https://i.imgur.com/Hl3WgQL.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the highlighted encrypted data in the Packet Bytes pane:  <br/>
<img src="https://i.imgur.com/yMFpc6U.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the passive port specified by the FTP server in the Packet Details pane:  <br/>
<img src="https://i.imgur.com/34MYpz0.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the Destination Port field value in the Packet Details pane:  <br/>
<img src="https://i.imgur.com/hFjkHSp.png" height="80%" width="80%" alt="Section 1 Steps"/>



 

 ### Section 2

<h2>Configure Wireshark and Generate Network Traffic:</h2>










<p align="center">
Show the sta1-wlan0 connected to the SecureLabs-WiFi network: <br/>
<img src="https://i.imgur.com/49vAuBq.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the updated security mode on the Status page:  <br/>
<img src="https://i.imgur.com/AcqhIdC.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the connection to the now-encrypted WLAN:  <br/>
<img src="https://i.imgur.com/Xuqyk6u.png" height="80%" width="80%" alt="Section 1 Steps"/>


 <h2>Analyze Traffic Using Wireshark:</h2>










<p align="center">
Show the SSID and channel in the Packet Details pane: <br/>
<img src="https://i.imgur.com/wWAr1pH.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the Packet Details for the ICMP packet:  <br/>
<img src="https://i.imgur.com/A179tO3.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the Packet Details for the HTTP packet:  <br/>
<img src="https://i.imgur.com/VzYHDMR.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the key information for Message 3 in the four-way handshake:  <br/>
<img src="https://i.imgur.com/ORj7kYF.png" height="80%" width="80%" alt="Section 1 Steps"/>





 ### Section 3

<h2>Generate Malicious Network Traffic:</h2>










<p align="center">
Show the aireplay-ng --deauth output: <br/>
<img src="https://i.imgur.com/wjKfVKX.png" height="80%" width="80%" alt="Section 1 Steps"/>



 <h2>Analyze Malicious Network Traffic:</h2>










<p align="center">
Show one of the deauth packets that you generated between the BSSID and your selected station: <br/>
<img src="https://i.imgur.com/cmimqDJ.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the packets related to the four-way handshake:  <br/>
<img src="https://i.imgur.com/SoaaGZ3.png" height="80%" width="80%" alt="Section 1 Steps"/>







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
