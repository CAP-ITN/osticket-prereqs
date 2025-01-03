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
- Have your VM up and running. Download Zip file for osTicket files and proceed to unzip them. After Extracting all the files, you will check off IIS (Internet Information Services), click through WWW (World Wide Web Services), click through Application Development Features, and lastly check off CGI. Install PHP Manager and Rewrite Module. Continue by making a directory, "C:/PHP" to unzip the PHP 7.3.8 Folder into. Continue by installing VC_Redist and MySQL.
</p>
<br />

<p>

![IIS Admin](https://github.com/user-attachments/assets/3f9c8e4b-ebe7-4989-8b03-fbb319ee454b)


</p>
<p>
You will then open up IIS as an Admin, to register the PHP. To make sure that happens, go to PHP Manager and click the php-cgi folder, proceed to stop and start to "reload" IIS. Then we will install osTicket 1.15.8. unzip osTicket 1.15.8 and copy upload folder into c:\inetpub\wwwroot, very IMPORTANT to rename "upload" into "osTicket" verbatim. Then reload IIS.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
