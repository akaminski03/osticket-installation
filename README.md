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

- Have an active Microsoft Azure subscription
- Create a Windows 10 Virtual Machine on Azure
- Remote desktop connect to the virtual machine you created
- The steps will all take place from within the virtual machine

<h2>Installation Steps</h2>
<p>
<img src="https://github.com/akaminski03/osticket-prereqs/assets/65532146/ac5c62c0-df3d-4520-a489-0f500bfe8868" height="80%" width="80%" alt="IIS-1"/>
<img src="https://github.com/akaminski03/osticket-prereqs/assets/65532146/7d988c4f-53b2-4d24-9bd4-1527c06aeacf" height="80%" width="80%" alt="IIS-2"/>
<img src="https://github.com/akaminski03/osticket-prereqs/assets/65532146/4501a614-0a25-4aab-b636-c1675866633d" height="80%" width="80%" alt="IIS-3"/>
</p>
<p>
Enable IIS, make sure the above boxes are checked.
</p>
<br />

<p>
  <img src="https://github.com/akaminski03/osticket-prereqs/assets/65532146/90210807-086f-4b98-a3b7-b6d7145676a8" height="80%" width="80%" alt="Installations"/>
</p>
<p>
Download and install all of the software from this <a href="https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">link. 
</p>
<p>
PHP should be installed in C:\PHP
<br>
<br>
The upload folder of osTicket should be extracted into C:\inetpub\wwwroot, and then the upload folder should be renamed to "osTicket"
</p>
<br />

<p>
<img src="https://github.com/akaminski03/osticket-prereqs/assets/65532146/24fe61eb-0c5b-4c1b-ad88-fe19532733f5" height="80%" width="80%" alt="ost-config"/>
</p>
<p>
Rename the file in C:\inetpub\wwwroot\osTicket\include called "ost-sampleconfig.php" to "ost-config.php"
</p>
<br />

<p>
<img src="https://github.com/akaminski03/osticket-prereqs/assets/65532146/fc4312d5-ed2f-4e37-8ce8-612c85af1e55" height="80%" width="80%" alt="ost-permissions"/>
</p>
<p>
Right click on "ost-config.php" and navigate to properties. Go to security, click on advanced, and click on Disable inheritance. Choose Remove all inherited permissions from this object.
</p>
<br />

<p>
<img src="https://github.com/akaminski03/osticket-prereqs/assets/65532146/5aa9d4dd-d65e-4001-aadd-a15730323af8" height="80%" width="80%" alt="ost-permissions2"/>
</p>
<p>
Add a permission to the file by clicking add, Select a principal, typing in everyone, hitting enter and clicking ok. Then enable full control.
</p>
<br />

<p>
<img src="https://github.com/akaminski03/osticket-prereqs/assets/65532146/3811574c-ba40-4700-8fe1-710175f1945e" height="80%" width="80%" alt="osTicket"/>
</p>
<p>
Navigate in a web browser to localhost/osTicket/setup/
</p>
<br />

<p>
<img src="https://github.com/akaminski03/osticket-prereqs/assets/65532146/90eba446-33ff-4d23-adc8-884dc6549254" height="80%" width="80%" alt="IIS Register PHP"/>
</p>
<p>
Run IIS as an administrator, open PHP manager and then Register new PHP version. Use the version of PHP installed in C:\PHP
</p>
<br />

<p>
<img src="https://github.com/akaminski03/osticket-prereqs/assets/65532146/eb895e65-dbd5-4284-bae4-e8623a5eb481" height="80%" width="80%" alt="PHP manager extensions"/>
</p>
<p>
Inside of IIS, navigate to Sites -> Default Web Site -> osTicket. Open PHP manager, and click on Enable or disable an extension. Enable php_imap.dll, php_intl.dll, and php_opcache.dll.
</p>
<br />

<p>
<img src="https://github.com/akaminski03/osticket-prereqs/assets/65532146/e5c4722c-af98-4074-9e5c-2ed98894585f" height="80%" width="80%" alt="HeidiSQL"/>
</p>
<p>
Open HeidiSQL and create a new connection using the username "root" and the password that you chose when setting up mysql.
</p>
<br />

<p>
<img src="https://github.com/akaminski03/osticket-prereqs/assets/65532146/3728e5a0-4888-4e99-9015-d69a6b51655a" height="80%" width="80%" alt="HeidiSQL2"/>
</p>
<p>
Right click on Unnamed and create a new database, name it osTicket.
</p>
<br />

<p>
<img src="https://github.com/akaminski03/osticket-prereqs/assets/65532146/38e4f321-f9ac-4921-bc5b-3645f74497e3" height="80%" width="80%" alt="osTicket install"/>
</p>
<p>
Finish setting up osTicket, using osTicket for the field "MySQL Database:" and the same login that you used for HeidiSQL in the next two boxes. Click install.
</p>
<br />

<p>
<img src="https://github.com/akaminski03/osticket-prereqs/assets/65532146/bfa6f9c2-ab2b-4b68-8500-c8ee5f463ed5" height="80%" width="80%" alt="Delete Setup"/>
</p>
<p>
Navigate back to C:\inetpub\wwwroot\osTicket, and delete the folder called "setup"
</p>
<br />


