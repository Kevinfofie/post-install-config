# post-install-config<p align="center">
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

- install / Enable IIS in Windows WITH CGI
-  install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

-  install the Rewrite Module (rewrite_amd64_en-US.msi)
- install  PHP 7.3.8
-  install VC_redist.x86.exe.
-  install MySQL 5.5.62 (mysql-5.5.62-win32.msi)

-  install HeidiSQL.


<h2>Installation Steps</h2>
<p>
<p> We start by Creating an Azure Virtual Machine Windows 10, with a 4 vCPUs
</p>
<p>
<img src="https://i.imgur.com/kPwn8Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p> We start by Creating an Azure Virtual Machine Windows 10, with a 4 vCPUs
</p>
<p>
<img src="https://i.imgur.com/XgmkW30.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p> After the deploment is complete, we copy the public ip address and remotedesktop login to the vm created.
</p>

<p> After sucessfully login into the VM, we go to control panel, programs, then to Turn Windows features on or off to eneble IIS in Windows WITH CGI.Install / Enable IIS in Windows WITH CGI
World Wide Web Services -> Application Development Features -> [X] CGI
</p>
<p>
<img src="https://i.imgur.com/1DCxKl5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/Ldr86Zq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/lG8GC4Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>



<br />

<p> Atfer enabling IIS, we proceed the the installation of
  
-  install the Rewrite Module (rewrite_amd64_en-US.msi)
- install  PHP 7.3.8
-  install VC_redist.x86.exe.
-  install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
</p>
<br />

<p>
<img src="https://i.imgur.com/LHUxNLI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After the installation of MySQL and configuration, we proceed to opening IIS as an administrator and register PHP from within IIS.
</p>
<br />
<p>
<img src="https://i.imgur.com/lstHwll.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/vQ0QzVq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/XLoZfWb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/2oKzQLX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<h2>
<p>Installation of osTicket</h2>
<p>
<p>
Downloading and the Installation osTicket files
Extracting and copying the  “upload” folder to c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”.
</p>
<p>
The next step is openinig IIS, opening PHP and enabling Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll extention that are disabled by default.
</p>
<p>
<img src="https://i.imgur.com/1VoyB4T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/yLXUifL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/unkJkSv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/6eVqytD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<h2>The final step is the installation of HeidiSQL in order to create a Database for our osTicketing system</h2>
<p>
<img src="https://i.imgur.com/hx7oFDX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <p>
<img src="https://i.imgur.com/8a2Lqny.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
    <p>
      <p>
After the installation of HeidiSQL, we setup, configure create an osTicket database. Hence we Continue Setting up osticket in the browser from MySQL, by creating a user name, password and proceed to complete the installation of osTicket system. 
</p>
<img src="https://i.imgur.com/ekwxo5g.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


