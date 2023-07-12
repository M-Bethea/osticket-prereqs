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
- Link to downloads: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

<h2>Installation Steps</h2>

<p>
1. The first step is to create a virtual machine by going to https://portal.azure.com/. Setup your virtual machine with Windows 10 Pro, version 22H2. Note. Be sure to create a virtual machine with at least 2 vcpus and 16 gbs of memory.

2. When your virtual machine is created, connect to it by using the public ip address the vm is setup with. Connect using the remote desktop connection (RDC) app.
</p>
<br />

<p>
<img src="https://github.com/M-Bethea/osticket-prereqs/assets/139162550/3c9be0ca-1a1e-4268-b2a1-eeeee80d86ab" height="70%" width="70%" alt="Azure VM Setup"/>
</p>
<br />

3. Once you have connected to your virtual machine, go to your control panel. From the control panel open up programs. Select "Turn Windows features on and off".
  
<p>
<img src="https://imgur.com/LBGkAw6.png" height="70%" width="70%" alt="Windows Programs and Features"/>
</p>
<p>
  
4. Next install / enable IIS in Windows with CGI and Common HTTP Features
  - World Wide Web Services -> Application Development Features -> 
[X] CGI
[X] Common HTTP Features
  
<p>
<img src="https://imgur.com/LQjw9le.png" height="70%" width="70%" alt="Enabling ISS Features"/>
</p>
<p>
  
<p>
<img src="https://imgur.com/pbPeHb1.png" height="70%" width="70%" alt="Enabling ISS Features"/>
</p>
<p>
  
***NOTE*** Make sure all Common HTTP Features are checked.
 
 To make sure the IIS is installed / enabled go to a browser of your choice and search for 127.0.0.1 
  It should look something like this. 
  
<p>
<img src="https://imgur.com/eICujoq.png" height="70%" width="70%" alt="ISS Webpage"/>
</p>
<p>
  
5. With IIS enabled, from the installation files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
  Go through the install wizard and complete the install using the default settings.
  
6. Now from the installation files, download and install the Rewrite Module (rewrite_amd64_en-US.msi)
  
7. Create a folder in the C drive called PHP.
  
8. From the Installation Files, download PHP 7.3.8 (php-7.3.88-nts-Win32-VC15-x866.zip) and unzip the contents into C:\PHP
  
  !! ATTENTION !!
If this appears, choose to “Keep” the file then "Keep anyway":
  
<p>
<img src="https://imgur.com/xZv1Yhw.png" height="70%" width="70%" alt="Keep file"/>
</p>
<p>

9. When you have downloaded and extracted the zip file into the PHP folder on the C drive, download and install the VC_redist.x86.exe from the installation files. Go through the setup wizard to finish installing the VC_redist.x86.exe. Use default settings.
  
10. Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
  Run the setup wizard:
Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration ->

  Create a new root password (remember it)
  
<p>
<img src="https://imgur.com/KxcUy7C.png" height="70%" width="70%" alt="Root password setup"/>
</p>
<p>
  
  Execute the process on the next page.
  
<p>
<img src="https://imgur.com/i7sn6hT.png" height="70%" width="70%" alt="Execute process"/>
</p>
<p>
  
11. With all the required files downloaded and installed, search for IIS in the windows search bar. Open IIS as an ADMINISTRATOR.
  The program should look something like this:
  
<p>
<img src="https://imgur.com/rgdZwmM.png" height="70%" width="70%" alt="ISS Administrator"/>
</p>
<p>
  
12. Register PHP from within IIS.
  Click on PHP Manager
  
<p>
<img src="https://imgur.com/vvTLNBH.png" height="70%" width="70%" alt="Register ISS"/>
<p>
  
Register new PHP version.
  
<p>
<img src="https://imgur.com/qdbn5zQ.png" height="70%" width="70%" alt="Register PHP version"/>
</p>
<p>
  
Provide a path to the php executable file (php-cgi.exe)). 
  Go to C Drive -> PHP -> click on php-cgi file.
  
<p>
<img src="https://imgur.com/oJZ0gp9.png" height="70%" width="70%" alt="PHP path"/>
</p>
<p>
  
  Restart the IIS server.
  
<p>
<img src="https://imgur.com/CJ3RUbG.png" height="70%" width="70%" alt="Restart ISS server"/>
</p>
<p>
  
13. Install osTicket v1.15.8
  -Download osTicket from the Installation Files Folder
  -Extract and copy "upload" folder to c:\inetpub\wwwroot
  -Within c:\inetpub\root, Rename "upload" to "osTicket"
  
  Reload IIS again.
  
14. On IIS go to sites -> Default -> osTicket
  -On the right, click “Browse *:80”
  
<p>
<img src="https://imgur.com/Yw55d5b.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
  Some extensions are not enabled on the osTicket browser.
  
<p>
<img src="https://imgur.com/eJIsGTn.png" height="70%" width="70%" alt="Extentions not enabled"/>
</p>
<p>
  
  To enable the extensions:
  -Go back to IIS, sites -> Default -> osTicket
  -Double click PHP manager
  -Click "Enable or disable an extension"
  
<p>
<img src="https://imgur.com/vvTLNBH.png" height="70%" width="70%" alt="Enable extentions"/>
</p>
<p>
  
<p>
<img src="https://imgur.com/uigyKjb.png" height="70%" width="70%" alt="Enable extentions"/>
</p>
<p>
  
  Enable three extensions from here:
  
  1.) php_imap.dll
 
  2.) php_intl.dll
  
  3.) php_opcache.dll
  
<p>
<img src="https://imgur.com/cOem7Nb.png" height="70%" width="70%" alt="Enabling three extentions"/>
</p>
<p>
  
15.) Once those extensions enabled in IIS, rename one of the files in our osTicket folder.
  Go into the file explorer and search for C;\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
  
  Rename the ost-sampleconfig.php to ost-config.php
  
  When the file is renamed, right click on the file and go to properties.
  From there click security, click on advance, and disable the inheritance.
  Select "Remove all inherited permissions" from this object.
  
  Now we will add new permissions.
  
  Click "Add"
  
<p>
<img src="https://imgur.com/VPZvOdo.png" height="70%" width="70%" alt="Add permissions"/>
</p>
<p>
  
Select a principal
  
<p>
<img src="https://imgur.com/PoGk34d.png" height="70%" width="70%" alt="Select principal"/>
</p>
<p>
  
  
 Type "Everyone" in the box.
  
<p>
<img src="https://imgur.com/F4H3ppM.png" height="70%" width="70%" alt="Everyone"/>
</p>
<p>
  
  Make sure "Full Control" and all the other boxes are checked.
  
<p>
<img src="https://imgur.com/rbbGqwB.png" height="70%" width="70%" alt="Full control"/>
</p>
<p>
  
  Click Apply and Ok.
  
<p>
<img src="https://imgur.com/saRO3y5.png" height="70%" width="70%" alt="Apply and OK"/>
</p>
<p>
  
  Now continue to setup osTicket in the browser. Click Continue on the osTicket browser page.
  Fill out the page as required except the Database Settings at the bottom of the page. We will get to that. 
  
  Download and install HeidiSQL from the Installation Files. 
  
<p>
<img src="https://imgur.com/i7a4gWC.png" height="70%" width="70%" alt="Download and install HeidiSQL"/>
</p>
<p>
  
  When the program is open we will create a new session in it.
  
<p>
<img src="https://imgur.com/g5M1i61.png" height="70%" width="70%" alt="Create new session"/>
</p>
<p>
  
  Make the username root and create your password (remember your previous root password).
  
<p>
<img src="https://imgur.com/LEAZNOc.png" height="70%" width="70%" alt="Root username and password creation"/>
</p>
<p>
  
  Once you're connected to the session, go back to the browser to finish the set up. Under the Database Settings in the browser the username will be root and the password you created for root.
  
  Now create a new database within HeidiSQL. In Heidi right click on the left side where is says "Unnamed", select "create new", and then select "database". Name the new database osTicket. Once the new database is setup, go back to the osTicket browser and under "MySQL Database" type in osTicket.
  
<p>
<img src="https://imgur.com/0rG1AJm.png" height="70%" width="70%" alt="Create database in HeidiSQL"/>
</p>
<p>
  
 16. The last step is to do some clean up by deleting the setup folder in your system. 
  -Delete: C:\inetpub\wwwroot\osTicket\setup
  ONLY DELETE THE SETUP FOLDER.
  
 Next set the permissions back to "Read only" in the ost-config.php file.
  
<p>
<img src="https://imgur.com/wFr0pkK.png" height="70%" width="70%" alt="System cleanup"/>
</p>
<p>
  
<p>
<img src="https://imgur.com/jsJOPyn.png" height="70%" width="70%" alt="System cleanup"/>
</p>
<p>
  
Now you can login to osTicket in the browser.
  
<p>
<img src="https://imgur.com/uHVdDsx.png" height="70%" width="70%" alt="osTicket login page"/>
</p>
<p>
  
  Congrats! You have now successfully installed and setup osTicket.
