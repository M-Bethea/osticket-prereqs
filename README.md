<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- Internet Information Services (IIS)
- PHP Manager
- Rewrite Module
- VC Redist
- MySQL
- Heidi SQL
- osTicket v1.15.8

<h2>Installation Steps</h2>

<p>
1. Create a Virtual Machine in Azure
A. Create a Resource Group
B. Create a Windows 10 Pro Virtual Machine (VM) with 2-4 Virtual CPUs
 i. Create a name, username, and password (remember the username and password)
 ii. It will create a new Virtual Network (Vnet)
<p>
<img src="https://github.com/M-Bethea/osticket-prereqs/assets/139162550/740e9d6d-ca18-40e8-b571-832da69a8c90" height="80%" width="80%" alt="Create a VM"/>
</p>
<br />


<p>
2. Open the <a href="https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)">Installation Files</a> in the VM
  A. Righ click start menu -> Run -> Type "control" -> Programs -> Turn Windows Features On or Off
  B. Install / Enable IIS in Windows WITH:
CGI and Common HTTP Features
World Wide Web Services -> Application Development Features ->
[X] CGI
[X] Common HTTP Features
</p>
<p>
<img src="https://github.com/M-Bethea/osticket-prereqs/assets/139162550/c87c2862-4a15-46e5-b246-f9a4b407c812" height="80%" width="80%" alt="Create a VM"/>
</p>
<p>
<img src="https://github.com/M-Bethea/osticket-prereqs/assets/139162550/fcb01f44-78c7-4bab-a7b0-328269bcc17e" height="80%" width="80%" alt="Create a VM"/>
</p>
<p>
 Internet Information Services -> Web Management Tools -> IIS Management Console
	[X] IIS Management Console -> Ok
</p>
<p>
<img src="https://github.com/M-Bethea/osticket-prereqs/assets/139162550/2b132258-c893-405d-8d05-4f38dcd63c83" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/M-Bethea/osticket-prereqs/assets/139162550/98279b81-1b8e-4b8c-b6b6-9410db315dbd" height="80%" width="80%" alt="Create a VM"/>
</p>
C. Check if it's working by typing the following IP address into the browser: 127.0.0.1
<p>
<img src="https://github.com/M-Bethea/osticket-prereqs/assets/139162550/417dfb31-1f1d-43d8-b0dc-4eb4ee08d4f7" height="80%" width="80%" alt="Create a VM"/>
</p>
</p>

<br />

<p>
3. From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

A. From the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US.msi)
i. Create the directory C:\PHP in your files: 
<p>
<img src="https://github.com/M-Bethea/osticket-prereqs/assets/139162550/02283963-9182-4c4a-827e-031947aeff68" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
B. From the Installation Files, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP
i. !!! Attention!!! If you get a caution sign from the download, click on it -> Keep -> Keep anyway

C. From the Installation Files, download and install VC_redist.x86.exe.

D. From the Installation Files, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
Typical Setup -> Launch Configuration Wizard (after install) -> Standard Configuration -> (make a password and remember it) -> Execute -> Finish
<p>
<img src="https://github.com/M-Bethea/osticket-prereqs/assets/139162550/3a4e2053-0604-40bb-8dbe-5bd07a25f58a" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/M-Bethea/osticket-prereqs/assets/139162550/d6674cc3-5c7d-495e-8dce-d9ae533d36b3" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/M-Bethea/osticket-prereqs/assets/139162550/6569d389-b4dc-4dde-96cf-f60c0421ab7c" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
</ br>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
