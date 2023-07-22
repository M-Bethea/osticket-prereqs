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
2. Open the <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)">Installation Files</a> in the VM
  A. Righ click start menu -> Run -> Type "control" -> Programs -> Turn Windows Features On or Off
  B. Install / Enable IIS in Windows WITH:
CGI and Common HTTP Features
World Wide Web Services -> Application Development Features ->
[X] CGI
[X] Common HTTP Features
</p>
<p>
<img src="https://github.com/M-Bethea/osticket-prereqs/assets/139162550/2b132258-c893-405d-8d05-4f38dcd63c83 height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
