<h1>VULNERABILITY MANAGEMENT</h1>

 ### [YouTube Demonstration Coming Soon](https://youtu.be)

<h2>Description</h2>
Utilized Nessus Essentials to perform credentialed scans on local VMs hosted within VMWare Workstation. Following the discovery of vulnerabilities, initiated remediation procedures for specific issues. Subsequently, conducted rescan operations to verify the effectiveness of the remediation efforts.
<br />


<h2>Tools and Utilities Used</h2>

- <b>Nessuss Essentials</b> 
- <b>VmWare</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (64bit)

<h2>Lab walk-through:</h2>

<p align="center">

 
Spun up a virtual machine in VMware : <br/>
<img src="https://imgur.com/YTA3xYz.png" height="80%" width="80%" alt=""/>
<br /> Spun up a virtual machine in VMware running windows 10, pulled up the CL to find the IP address of the virtual machine using “Ipconfig” command. Pinged the found IP address using Command “ping type IP address” from my native pc also using CL: 
<br/>
<br />


<img src="https://imgur.com/5jE0SCy.png" height="80%" width="80%" alt=""/>

Installed Deprecated version of Firefox on VM: <br/>
<img src="https://imgur.com/cv74TNR.png" height="80%" width="80%" alt=""/>
<br />
<br />

 
Inputted VM IP Address into Nessus :  <br/>
<img src="https://imgur.com/jCNzNJS.png" height="80%" width="80%" alt=""/>
<br /> Once the IP address for the VM was been established I then entered it into Nessus (which was already installed and set up at this stage). Logged in and created a new scan. Pasted the VM IP Address into the “target box” to do a light manual port scan just to verify the scanner is connecting to the VM. I then Configured the VM to accept authenticated scans.
<br />


Add credentials into Nessus :  <br/>
<br /> Went back into Nessus to add a set of credentials to prep for a deeper scan. Typed in the username and password of your VM into the respective columns in Nessus and ran another scan.
<br /> 


 Started Nessus Scan (Discover, Assess and Report):  <br/>
<img src="https://imgur.com/8mAMBN4.png" height="80%" width="80%" alt=""/>
<br /> Launched the new scan. Once the scan was finished and all the vulnerabilities were listed, I assess from critical to low. I then Clicked the remediation tab to see suggestion. 
<br />

<img src="https://imgur.com/rJJ2HCo.png" height="80%" width="80%" alt=""/>


Remediate/Verify based on suggestion:  <br/>
<img src="https://imgur.com/H3zM40U.png" height="80%" width="80%" alt=""/>
<br /> Went into the VM and pulled up the Firefox uninstall file to uninstall the deprecated version of Firefox previously installed as part of the remediation process.
<br />


windows update:  <br/>
<img src="https://imgur.com/JqmbsZB.png"/>
<br /> Launched windows update and restarted the VM once the update process finished.
<br />
 relaunch scan and Verify :  <br/>
<br /> Logged back into Nessus to relaunch the scan and Verified that the critical vulnerabilities have been removed.
<br />
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
