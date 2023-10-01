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
The upload folder of osTicket should be extracted into C:\inetpub\wwwroot, and then the upload folder shouled be renamed to "osTicket"
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
<img src="https://github.com/akaminski03/osticket-prereqs/assets/65532146/eb895e65-dbd5-4284-bae4-e8623a5eb481" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Inside of IIS, navigate to Sites -> Default Web Site -> osTicket. Open PHP manager, and click on Enable or disable an extension. Enable php_imap.dll, php_intl.dll, and php_opcache.dll.
</p>
<br />
