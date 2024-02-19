<h1>Applying User Authentication and Access Controls</h1>

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
<img src="https://i.imgur.com/FucHtGI.png" height="80%" width="80%" alt="Section 1 Steps"/>


 <h2>Create Folders and Configure Security Permissions:</h2>







<p align="center">
Show the updated Security permissions for the HRfiles folder: <br/>
<img src="https://i.imgur.com/pwIPjdA.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the updated Security permissions for the MGRfiles folder:  <br/>
<img src="https://i.imgur.com/e2MJiHQ.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the updated Security permissions for the DEVfiles folder:  <br/>
<img src="https://i.imgur.com/gO2icU1.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the three folders within the LabFiles folder:  <br/>
<img src="https://i.imgur.com/vlnWPJQ.png" height="80%" width="80%" alt="Section 1 Steps"/>


<h2>Verify Authentication and Access Controls:</h2>







<p align="center">
Show the unsuccessful access error message for the HRfiles folder as scarpenter: <br/>
<img src="https://i.imgur.com/4L8yeyF.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the unsuccessful access error message for the MGRfiles folder as scarpenter:  <br/>
<img src="https://i.imgur.com/eMuU9vf.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the Properties dialog box for the file created in the DEVfiles folder by scarpenter:  <br/>
<img src="https://i.imgur.com/CHfMEaP.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the Properties dialog box for the file created in the HRfiles folder by lcasado:  <br/>
<img src="https://i.imgur.com/3vZRrzp.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the unsuccessful access error message for the MGRfiles folder as lcasado:  <br/>
<img src="https://i.imgur.com/u6xRvEF.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the unsuccessful access error message for the DEVfiles folder as lcasado:  <br/>
<img src="https://i.imgur.com/3tIJH2h.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the Properties dialog box for the file created in the MGRfiles folder by cprince:  <br/>
<img src="https://i.imgur.com/oiBbkcv.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the Properties dialog box for the file created in the DEVfiles folder by cprince:  <br/>
<img src="https://i.imgur.com/G8Nbokk.png" height="80%" width="80%" alt="Section 1 Steps"/>
<br />
<br />
Show the unsuccessful access error message for the HRfiles folder as cprince:  <br/>
<img src="https://i.imgur.com/tSgVenV.png" height="80%" width="80%" alt="Section 1 Steps"/>


 

 ### Section 2

<h2>Creating an SMB Share:</h2>










<p align="center">
Show the Employees dataset on the TrueNAS Pools page: <br/>
<img src="https://i.imgur.com/k1GZcWO.png" height="80%" width="80%" alt="Section 2 Steps"/>


 <h2>Create Shared Folders and Configure ACLs:</h2>










<p align="center">
Show the three new datasets on the TrueNAS Pools page: <br/>
<img src="https://i.imgur.com/ph9LTVU.png" height="80%" width="80%" alt="Section 2 Steps"/>

<h2>Verify Access Controls:</h2>










<p align="center">
Show the Employees folder while signed in as scarpenter: <br/>
<img src="https://i.imgur.com/95rtwyH.png" height="80%" width="80%" alt="Section 2 Steps"/>
<br />
<br />
Show the Employees folder while signed in as lcasado: <br/>
<img src="https://i.imgur.com/laCY0D4.png" height="80%" width="80%" alt="Section 2 Steps"/>
<br />
<br />
Show the Employees folder while signed in as cprince: <br/>
<img src="https://i.imgur.com/7xkmrPF.png" height="80%" width="80%" alt="Section 2 Steps"/>






 ### Section 3

<h2>Create Users and Security Groups:</h2>










<p align="center">
Show the Member Of tab of the Properties dialog box for Abernathy Bobbleshaw: <br/>
<img src="https://i.imgur.com/lyc3KsB.png" height="80%" width="80%" alt="Section 3 Steps"/>
<br />
<br />
Show the Member Of tab of the Properties dialog box for Leslie Wu: <br/>
<img src="https://i.imgur.com/39PyLkx.png" height="80%" width="80%" alt="Section 3 Steps"/>


 <h2>Create Shared Folders and Configure ACLs:</h2>










<p align="center">
Show the new GG Studios datasets on the TrueNAS Pools page: <br/>
<img src="https://i.imgur.com/2yXHPHl.png" height="80%" width="80%" alt="Section 3 Steps"/>


<h2>Verify Authentication and Access Controls:</h2>










<p align="center">
Show the Employees folder while signed in as abobbleshaw: <br/>
<img src="https://i.imgur.com/HtnOD9A.png" height="80%" width="80%" alt="Section 3 Steps"/>
<br />
<br />
Show the Employees folder while signed in as lwu: <br/>
<img src="https://i.imgur.com/Z1nF3Es.png" height="80%" width="80%" alt="Section 3 Steps"/>








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
