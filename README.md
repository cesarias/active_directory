<p align="center">
<img src="https://i.imgur.com/Ze6Cwdc.png" alt="Sentinel logo"/>
</p>

<h1> Azure Active Directory Installation and utilizing some of its resources </h1>
This tutorial outlines the prerequisites and installation of Azure Active Directory on a Windows VMs <br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- MAC OS / Windows 10 (VM)</b>
- Azure Active Directory
- Microsoft Remote Desktop
- Powershell


<h2> Lab Description </h2>

<p>
<img src="https://i.imgur.com/CobDAas.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Begin to create resources within Azure. For the Domain Controller VM the NIC Private IP address will be set to static. We don't want the IP address to constantly change since it will be providing a service to our client Window's VM.  
</p>
<br />

<p>
<img src="https://i.imgur.com/sAfENTC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 For the Client VM the DNS must be manually set to use the Domain Controllers IP address as its DNS Server.
</p>
<br />

<p>
<img src="https://i.imgur.com/B4wtuFE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Topology Map of our Virtual Network. 
</p>
<br />

<p>
<img src="https://i.imgur.com/I2vkrs3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Log into our Client VM using Microsoft Remote Desktop.
</p>
<br />

<p>
<img src="https://i.imgur.com/h1hM7zR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Pinging Domain Controllers Private IP Address. At first the requestes were being timed out, but after enabling ICMPv4 on our Domain Controller VM the  ping requests were receiving a reply. 
</p>
<br />

<p>
<img src="https://i.imgur.com/wRiouTM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Enabling ICMPv4 on our Domain Controller verified that the Domain Controller can accept requests in our network from our Client VM. 
</p>
<br />

<p>
<img src="https://i.imgur.com/glmywx3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Begin the installation process for Azure Active Directory. 
</p>
<br />

<p>
<img src="https://i.imgur.com/ujYleW6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Creating a new Organizational unit within Active Directory. 
</p>
<br />

<p>
<img src="https://i.imgur.com/QnvFaxc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Adding a user to the Domain Admins(OU). 
</p>
<br />

<p>
<img src="https://i.imgur.com/WcFbQkw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Adding the client VM to the domain. 
</p>
<br />

<p>
<img src="https://i.imgur.com/aB4KTT3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Allowing all of the domain users(OU) to sign in remotely. 
</p>
<br />

<p>
<img src="https://i.imgur.com/XE268Ks.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Using PowerShell to randomly create users for our Domain User(OU). 
</p>
<br />

<p>
<img src="https://i.imgur.com/iVsP9KB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Choosing one of the newly created users and verifying that they have access to log in remotley  into our domain.  
</p>
<br />


