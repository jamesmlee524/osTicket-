<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>
<ol>
    <li>Enable Internet Information Services (IIS)</li>
    <li>Install Web Platform Installer</li>
    <li>Install MySQL and set up user and pass</li>
    <li>Install C++ Redistributable</li>
    <li>Configure permissions and install osTicket</li>
</ol>

<h2>Installation Steps</h2>
<p>
Create a Virtual Machine(VM) on Azure.
Be sure to create a resource.
Name it and then click on Windows 10 for image.
Make sure to create your VM and resource in the same region
Get one thats runs on 2cpus
Click the check box and create the VM.
</p>
<img width="1208" alt="Screenshot 2025-02-11 at 11 22 18 AM" src="https://github.com/user-attachments/assets/ac20c712-f0c7-4266-b27b-e84c58464416" />
<img width="1232" alt="Screenshot 2025-02-11 at 11 22 54 AM" src="https://github.com/user-attachments/assets/dec7f522-b9a7-469c-8dd1-b477395d9c8d" />
<img width="1230" alt="Screenshot 2025-02-11 at 11 24 03 AM" src="https://github.com/user-attachments/assets/82964dad-eead-49c1-bddb-72172b21331c" />

<br />
<br />
<br />
<br />


<p>
Launch the VM (virtual machine) with its public IP address
Open Windows App and create a new VM. Then launch with the credentials that you made when creating the VM. 
</p>
<img width="1225" alt="Screenshot 2025-02-11 at 1 52 55 PM" src="https://github.com/user-attachments/assets/922a38fe-7367-491f-801d-a2c55f2c88af" />
<img width="1164" alt="Screenshot 2025-02-11 at 1 54 10 PM" src="https://github.com/user-attachments/assets/327bc04d-d8e3-4bc0-a66f-a89c45ee640b" />
<img width="1163" alt="Screenshot 2025-02-11 at 1 55 14 PM" src="https://github.com/user-attachments/assets/8ba24a5b-b5b6-40b5-b939-a8c43b359c19" />


<br />
<br />
<br />
<br />

<p>
Within the VM (osticket-vm), download the osTicket-Installation-Files.zip and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files”
</p>
<img width="1536" alt="Screenshot 2025-02-11 at 1 59 33 PM" src="https://github.com/user-attachments/assets/b25f6c6a-6023-4b11-9eed-59f9c20b84f1" />

<p>
<ol>
    <li>Install / Enable IIS in Windows WITH CGI</li>
    <li>From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)</li>
    <li>From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)</li>
</ol>
</p>
<img width="1536" alt="Screenshot 2025-02-11 at 2 33 37 PM" src="https://github.com/user-attachments/assets/ed2cf6d0-0391-4395-ba09-fa97a946bf50" />
<img width="1536" alt="Screenshot 2025-02-11 at 2 35 33 PM" src="https://github.com/user-attachments/assets/eb55f222-5bf0-4ae2-b6a0-c291c3e022ac" />

<p>
Create the directory C:\PHP
From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
</p>
<img width="1536" alt="Screenshot 2025-02-11 at 2 36 45 PM" src="https://github.com/user-attachments/assets/fbd8a6dc-dfa9-47fd-ade6-9f5e74590089" />

unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
<img width="1536" alt="Screenshot 2025-02-11 at 2 37 35 PM" src="https://github.com/user-attachments/assets/ed59c1cd-2aed-471b-8b41-a4564160045d" />

From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.
<img width="1536" alt="Screenshot 2025-02-11 at 2 38 45 PM" src="https://github.com/user-attachments/assets/00f87557-af4f-4a6c-8a20-7888bd6a0c45" />


From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
<img width="1536" alt="Screenshot 2025-02-11 at 2 39 08 PM" src="https://github.com/user-attachments/assets/db0d6fbb-c876-4b9d-bec0-f6f74235c467" />

Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration ->
Username: root
Password: root
<img width="1536" alt="Screenshot 2025-02-11 at 2 39 43 PM" src="https://github.com/user-attachments/assets/4206a482-c694-4b26-b8a1-cbfeb680eeb4" />


Open IIS as an Admin
Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)
Reload IIS (Open IIS, Stop and Start the server)
<img width="1536" alt="Screenshot 2025-02-11 at 2 42 35 PM" src="https://github.com/user-attachments/assets/7af3d630-3fc7-42b5-8889-12859d86a86f" />



Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”

<img width="1536" alt="Screenshot 2025-02-11 at 2 46 22 PM" src="https://github.com/user-attachments/assets/4d7aabfa-0ca4-4ecb-9725-c04580f81df5" />

Reload IIS (Open IIS, Stop and Start the server)
<img width="1536" alt="Screenshot 2025-02-11 at 2 43 27 PM" src="https://github.com/user-attachments/assets/681bb71f-ee75-4db4-ad7b-9a1f5edc94da" />


Go to sites -> Default -> osTicket
On the right, click “Browse *:80”
<img width="1536" alt="Screenshot 2025-02-11 at 2 47 36 PM" src="https://github.com/user-attachments/assets/95414ead-0006-437e-80f2-3ca03046a3dd" />


Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes
<img width="1536" alt="Screenshot 2025-02-11 at 2 50 36 PM" src="https://github.com/user-attachments/assets/4ae4ba4a-3424-4d72-952e-d1e96d3416b0" />


Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All
<img width="1536" alt="Screenshot 2025-02-11 at 2 54 23 PM" src="https://github.com/user-attachments/assets/70ed097c-393b-42b9-ba75-98dfc8aec204" />


Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)

From the “osTicket-Installation-Files” folder, install HeidiSQL.
Open Heidi SQL
Create a new session, root/root
Connect to the session
Create a database called “osTicket”

Continue Setting up osTicket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: root
Click “Install Now!”
<img width="1536" alt="Screenshot 2025-02-11 at 2 55 34 PM" src="https://github.com/user-attachments/assets/462aa19a-2811-450f-b3f6-cd9973cc567c" />


Congratulations, hopefully it is installed with no errors!
Browse to your help desk login page: http://localhost/osTicket/scp/login.php

End Users osTicket URL:
http://localhost/osTicket/ 


<br />
