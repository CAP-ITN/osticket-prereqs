<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Requirements and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 Pro</b> (22H2)

<h2>List of Prerequisites</h2>

- Install osTicket zip file, after unzipping the following will appear:
- PHPManagerForIIS (Hypertext Preprocessor)
- Rewrite Module
- VC_redist
- MySQL
- osTicket
- HeidiSQL

<h2>Installation Steps</h2>

<p>
  
![IIS](https://github.com/user-attachments/assets/0e8aaea3-22a9-4e98-86b5-0861e943333a)

</p>
<p>
Create an Azure Virtual Machine (VM): To start, login to your Azure portal and navigate to the Virtual Machines section. Click on "Create" and select "Virtual Machine." Choose Windows 10 as the OS, set the VM name to whatever you'd like, and configure the hardware with 4 vCPUs. For authentication, set the username as Sprinkles and the password as VMLabRules123. Once all settings are confirmed, launch the VM and wait to complete. After the VM is up and running, use Remote Desktop Connection (RDP) to log into the VM with the credentials provided.
</p>
<br />
<p>

![IIS Admin](https://github.com/user-attachments/assets/3f9c8e4b-ebe7-4989-8b03-fbb319ee454b)

</p>
<p>
Prepare the VM for osTicket Installation: Inside the VM, download the osTicket-Installation-Files.zip and extract it to the desktop. The extracted folder should be named osTicket-Installation-Files. Next, install IIS (Internet Information Services) with CGI enabled. To do this, open "Turn Windows Features On or Off," expand World Wide Web Services -> Application Development Features, and check CGI off as well as IIS. Once installed, proceed with installing PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) and the Rewrite Module (rewrite_amd64_en-US.msi) from the osTicket-Installation-Files folder.
</p>
<br />
<p>

![osTicket](https://github.com/user-attachments/assets/70d5b995-80d8-4228-83c0-33685f07a64b)

</p>
<p>
Configure PHP and Install MySQL
Create a directory at C:\PHP and extract PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into this folder. Next, install VC_redist.x86.exe to ensure all required dependencies are available. Proceed to install MySQL 5.5.62 (mysql-5.5.62-win32.msi) using the Typical Setup option. After installation, launch the Configuration Wizard, select Standard Configuration, and set the username and password as root/root. Once configured, MySQL should be ready for use with osTicket.
</p>
<br />

![HeidiSQL](https://github.com/user-attachments/assets/f87d22d9-7877-4d47-970d-e854bf10f509)


</p>
<p>
Set Up IIS and Install osTicket
Open IIS as an Administrator and register PHP by selecting PHP Manager -> C:\PHP\php-cgi.exe. Reload IIS by stopping and starting the server. To install osTicket v1.15.8, extract osTicket-v1.15.8.zip from the osTicket-Installation-Files folder. Copy the upload folder to C:\inetpub\wwwroot, then rename it to osTicket. Reload IIS and navigate to Sites -> Default -> osTicket, then click **Browse *:80 to open osTicket in a browser. If some extensions are missing, go back to IIS, open PHP Manager, enable php_imap.dll, php_intl.dll, and php_opcache.dll, then refresh the osTicket site.
</p>
<br />

![SuccessosTicketInstall](https://github.com/user-attachments/assets/c7eb9aea-4d8b-4608-b3a7-cd4506a924e5)


</p>
<p>
Finalize osTicket Setup and Database Configuration
Rename ost-sampleconfig.php from *C:\inetpub\wwwroot\osTicket\include* to ost-config.php, then update its permissions: disable inheritance, remove all permissions, and add a new permission for Everyone with full control. Continue the osTicket setup in the browser by providing a helpdesk name and default email. Install HeidiSQL, open it, and create a new session using root/root credentials. Inside HeidiSQL, create a new database named osTicket. Complete the osTicket setup in the browser by entering the database details (MySQL Database: osTicket, Username: root, Password: root) and click Install Now! Once installed, access the help desk login page at http://localhost/osTicket/scp/login.php and the end-user portal at http://localhost/osTicket/
</p>
<br />

