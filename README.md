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

<p>
<ol>
    <li>Install / Enable IIS in Windows WITH CGI</li>
    <li>From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)</li>
    <li>From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)</li>
</ol>
</p>

<p>
Create the directory C:\PHP
From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
</p>
<br />
